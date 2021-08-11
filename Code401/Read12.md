# Working with Relationships in Spring Data REST


<br>

# Types of Relationships

**A.** One-One Relationship **(1-1 Relationship)**

**B.** One-Many Relationship **(1-M Relationship)**

**C.** Many-Many Relationship **(M-M Relationship)**

<br>
<br>


## 1- One-to-One Relationship

- One-to-One (1-1) relationship is defined as the relationship between two tables where both the tables should be associated with each other based on only one matching row. This relationship can be created using Primary key-Unique foreign key constraints.

- With One-to-One Relationship in SQL Server, for example, a person can have only one passport. 

<br>

![!](https://www.tech-recipes.com/wp-content/uploads/2015/09/One_to_One_Relationship_SQL_Server.png)

<br>
<br>

## 2- One-to-Many Relationship

- The **One-to-Many** relationship is defined as a relationship between two tables where a row from one table can have multiple matching rows in another table. This relationship can be created using Primary key-Foreign key relationship.

- In the **One-to-Many** Relationship in SQL Server, for example, the address can be for more that one person.

![!](https://i.stack.imgur.com/jv1Gv.png)

<br>
<br>

## 3- Many-to-Many Relationship

- A **many-to-many** relationship occurs when multiple records in a table are associated with multiple records in another table.

- For example, a **many-to-many** relationship exists between customers and products: customers can purchase various products, and products can be purchased by many customers.

![!](https://i.stack.imgur.com/KXdHU.png)

<br>
<br>

## How we implement those relationships using spring? 

## 1- One-to-One Relationship

- Define two entity classes Library and Address having a one-to-one relationship, using the `@OneToOn`e annotation. 

```

@Entity
public class Library {

    @Id
    @GeneratedValue
    private long id;

    @Column
    private String name;

    @OneToOne
    @JoinColumn(name = "address_id")
    @RestResource(path = "libraryAddress", rel="address") // this annotation is optional and can be used to customize the endpoint.
    private Address address;
    
    // standard constructor, getters, setters
}

@Entity
public class Address {

    @Id
    @GeneratedValue
    private long id;

    @Column(nullable = false)
    private String location;

    @OneToOne(mappedBy = "address")
    private Library library;

    // standard constructor, getters, setters
}


```

- The association name defaults to the property name and can be customized using the rel attribute of @RestResource annotation:

```

@OneToOne
@JoinColumn(name = "secondary_address_id")
@RestResource(path = "libraryAddress", rel="address")
private Address secondaryAddress;

```

- The Repositories

> Expose these entities as resources, let's create two repository interfaces for each of them, by extending the CrudRepository interface:


```
public interface LibraryRepository extends CrudRepository<Library, Long> {}
public interface AddressRepository extends CrudRepository<Address, Long> {}
```

- Creating the Resources

```
curl -i -X POST -H "Content-Type:application/json" 
  -d '{"name":"My Library"}' http://localhost:8080/libraries
```

> Before we create an association, sending a GET request to this endpoint will return an empty object.

```
curl -i -X POST -H "Content-Type:application/json" 
  -d '{"location":"Main Street nr 5"}' http://localhost:8080/addresses
```



<br>
<br>
<br>
<br>

# Integration Testing in Spring