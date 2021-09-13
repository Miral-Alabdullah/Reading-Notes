# Amazon Cognito
  
  - The Amplify Auth category provides an interface for authenticating a user, it provides the necessary authorization to the other Amplify categories.

  - Amazon Cognito lets you add user sign-up, sign-in, and access control to your web and mobile apps quickly and easily.

  - Amazon Cognito provides authentication, authorization, and user management for your web and mobile apps. Your users can sign in directly with a user name and password, or through a third party such as Facebook, Amazon, Google or Apple.
  
  -The two main components of Amazon Cognito are user pools and identity pools. User pools are user directories that provide sign-up and sign-in options for your app users. Identity pools enable you to grant your users access to other AWS services. You can use identity pools and user pools separately or together.


## Features of Amazon Cognito

  * User pools

    - A user pool is a user directory in Amazon Cognito. With a user pool, your users can sign in to your web or mobile app through Amazon Cognito, or federate through a third-party identity provider (IdP).

      **-User pools provide:**
      
        1- Sign-up and sign-in services.
        
        2- A built-in, customizable web UI to sign in users.
        
        3- Social sign-in with Facebook, Google, Login with Amazon, and Sign in with Apple, and through SAML and OIDC identity providers from your user pool.
        
        4-User directory management and user profiles.
        
        5- Security features such as multi-factor authentication (MFA), checks for compromised credentials, account takeover protection, and phone and email verification.
        
        6- Customized workflows and user migration through AWS Lambda triggers.

<br>

  * Identity pools

    - With an identity pool, your users can obtain temporary AWS credentials to access AWS services, such as Amazon S3 and DynamoDB. Identity pools support anonymous guest users.

      **-Identity pools provide:**
      
        1- Amazon Cognito user pools.
        
        2- Social sign-in with Facebook, Google, Login with Amazon, and Sign in with Apple.
        
        3- OpenID Connect (OIDC) providers.
        
        4-SAML identity providers.
        
        5- Developer authenticated identities.

<br>

## Configure Auth Category

  ```
  - amplify add auth

  - amplify push
  ```

## Dependencies must be added to build.gradle

  ```
  dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
    }
  ```