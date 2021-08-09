# Baeldung: Spring Request Mapping =>


1- **`@RequestMapping` Basics** -> 

  - `@RequestMapping` — by Path 

    ```
	@RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
    @ResponseBody
	
    public String getFoosBySimplePath() {
    return "Get some Foos";
    }
	```

  - `@RequestMapping` — the HTTP Method -> 

    ```
	@RequestMapping(value = "/ex/foos", method = POST)
    @ResponseBody
    public String postFoos() {
    return "Post some Foos";
    }
	```

2- **RequestMapping and HTTP Headers ->** 

  - `@RequestMapping` With the headers Attribute -> 

  ```
   @RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)
   @ResponseBody
   public String getFoosWithHeader() {
    return "Get some Foos with Header";
   }
  ```

  - `@RequestMapping` Consumes and Produces -> 

  ```
  @RequestMapping(
  value = "/ex/foos", 
  method = GET, 
  headers = "Accept=application/json")
  @ResponseBody
  public String getFoosAsJsonFromBrowser() {
    return "Get some Foos with Header Old";
  }
  ```

3- **RequestMapping With Path Variables ->**  

  - Single `@PathVariable`

    ```
	@RequestMapping(value = "/ex/foos/{id}", method = GET)
    @ResponseBody
    public String getFoosBySimplePathWithPathVariable(
    @PathVariable("id") long id) {
    return "Get a specific Foo with id=" + id;
    }
	```

	- If the name of the method parameter matches the name of the path variable exactly, then this can be simplified by using `@PathVariable` with no value:


	```
	@RequestMapping(value = "/ex/foos/{id}", method = GET)
    @ResponseBody
    public String getFoosBySimplePathWithPathVariable(
    @PathVariable String id) {
    return "Get a specific Foo with id=" + id;
    }
	```

  - Multiple `@PathVariable` 

  ```
  @RequestMapping(value = "/ex/foos/{fooid}/bar/{barid}", method = GET)
  @ResponseBody
  public String getFoosBySimplePathWithPathVariables
  (@PathVariable long fooid, @PathVariable long barid) {
    return "Get a specific Bar with id=" + barid + 
      " from a Foo with id=" + fooid;
  }
  ```
  
  - `@PathVariable` With Regex

  ```
  @RequestMapping(value = "/ex/bars/{numericId:[\\d]+}", method = GET)
  @ResponseBody
  public String getBarsBySimplePathWithPathVariable(
  @PathVariable long numericId) {
    return "Get a specific Bar with id=" + numericId;
  }
  ```


<br>
<hr>
<br>

# Baeldung: Comparing repositories => 

**- CrudRepository :**

```

public interface CrudRepository<T, ID extends Serializable>
  extends Repository<T, ID> {

    <S extends T> S save(S entity);

    T findOne(ID primaryKey);

    Iterable<T> findAll();

    Long count();

    void delete(T entity);

    boolean exists(ID primaryKey);
}

```

  - save() -> save an Iterable of entities. Here, we can pass multiple objects to save them in a batch

  - findOne() -> get a single entity based on passed primary key value

  - findAll() -> get an Iterable of all available entities in database

  - count() -> return the count of total entities in a table

  - delete() -> delete an entity based on the passed object

  - exists() -> verify if an entity exists based on the passed primary key value



