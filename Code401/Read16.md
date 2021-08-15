# Spring Security Architecture

# Authentication and Access Control

- Application security boils down to two more or less independent problems: authentication (who are you?) and authorization (what are you allowed to do?).

- Sometimes people say “access control” instead of "authorization", which can get confusing, but it can be helpful to think of it that way because “authorization” is overloaded in other places.

## Authentication

```
public interface AuthenticationManager {

  Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
}
```



- An `AuthenticationManager` can do one of 3 things in its `authenticate()` method:

  * Return an `Authentication` (normally with `authenticated=true`) if it can verify that the input represents a valid principal.

  * Throw an `AuthenticationException` if it believes that the input represents an invalid principal.

  * -Return `null` if it cannot decide.


- `AuthenticationException` is a runtime exception.


The most commonly used implementation of `AuthenticationManager` is `ProviderManager`, which delegates to a chain of `AuthenticationProvider` instances. An `AuthenticationProvider` is a bit like an `AuthenticationManager`, but it has an extra method to allow the caller to query whether it supports a given `Authentication` type:

```
public interface AuthenticationProvider {

	Authentication authenticate(Authentication authentication)
			throws AuthenticationException;

	boolean supports(Class<?> authentication);
}
```


![!](https://raw.githubusercontent.com/spring-guides/top-spring-security-architecture/main/images/authentication.png)



## Authorization or Access Control

Once authentication is successful, we can move on to authorization, and the core strategy here is `AccessDecisionManager`. There are three implementations provided by the framework and all three delegate to a chain of `AccessDecisionVoter` instances, a bit like the `ProviderManager` delegates to `AuthenticationProviders`.

```
boolean supports(ConfigAttribute attribute);

boolean supports(Class<?> clazz);

int vote(Authentication authentication, S object,
        Collection<ConfigAttribute> attributes);
```

## Web Security

![!](https://raw.githubusercontent.com/spring-guides/top-spring-security-architecture/main/images/filters.png)


![!](https://raw.githubusercontent.com/spring-guides/top-spring-security-architecture/main/images/security-filters.png)

![!](https://raw.githubusercontent.com/spring-guides/top-spring-security-architecture/main/images/security-filters-dispatch.png)