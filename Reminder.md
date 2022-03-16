### Python
Python is the strong and dunamically typed programming language with easy-to-read syntax. It's interpreted programming language that means Python is being interpreted without compiling program into machine instructions.

### Typing
It means that it's matter what variable types you trying to operate.
It means that Python set variable types during program executing.
There are 2 groups of Python variables. They are mutable and immutable.
Mutuble types are list, dict and set.
Immutuble types are int, float, str, tuple and boolean.
There are some another types in Python like frozen_set, bytes, default_dict etc.

### Closures
It's a function structure with nested function and function what returns nested. The variable what assigned in global function can be used in nested with keyword "nonlocal".

### Decorators
It's the function that wrap the other function and can edit behaviour of wrapped function. You can assign it by setting function we want to decorate to argument of decorator and call it or we can assign it by adding the decorator name with "at" symbol above of function we want to decorate.

### Testing
If we test out application we should follow the main principles of testing. I'd like to tell you about FIRST. It's acronym. It consists of:
- F - FAST - Tests should be as fast as possible. Execution time is important because nobody wants to wait 15 minutes after all tests will completed. 
- I - Isolated - Tests should not depend on another. We can use Mock object to control object behaviour to simulate third-party APIs.
- R - Repeatable - Tests should run in every invironment and result should be the same. 
- S - Self-Validating - Each of you tests should be able to auto-detect if it passed or not.
- T - Thorough - If we write tests we should cover not only the execution of happy paths but also possible errors and negative paths. It helps make our tests more meaningful, more complete and gives us a better understanding of more complex parts of code.

### OOP - Object oriented programming
It's consists of 4 pillars:
- Abstraction - It's the process of selection data from large pull to show only the relevant details to the object.
- Encapsulation - It's the possibility of each object to get a private state inside a class. Other objects  can't access this state directly. They can only invoke a list from public functions.
- Inheriance - It's the ability of one object to acquire some properties of another object.
- Polymorphism - It's gives us a way to use a class exactly like its parent. It means that we can we can override some functions and use it like it's their own.

### SOLID 
It's acronym. There are 5 letter that means their own meaning.
- S - SRP - Single Responsibility Principle - It's mean that each class should has their own job.
- O - OCP - Open/Closed Principle - It's mean that each entity should be closed to modification but can be extended.
- L - LSP - Barbara Liskov Substitution Principle - Every subclass should be substitutable for thier base or parent class
- I - ISP - Interface Segregation Principle - No client should be forced to depend on methods it does not use. It means that class should implement methods that it will use.
- D - DIP - Dependency Inversion Principle - High-level module shouldn't depends on low-level module.

### REST
It's acronym for Representational State Transfer. It have it's own 6 guiding constraits. If you follow the first 5 of them you application may be called RESTful. There are:
- Client-server - Application should be separated by client and server parts. 
    + If we use it we can impove scalability of our application and portability for user
- Stateless - It means that server shouldn't save any state of user activity and each request must contains all of the information necessary to understand the request.
    + Client may save all information needed.
- Cachable - You should use caching everywhere it's possible and required.
    + If a response is cacheble user can receive cached value without calculating a huge amount of information.
- Uniform Interface - It's about identificaion of resources in the internet via URL (Uniform Resourse Locator) and URI (Uniform Resourse Identifier) and HTTP methods. It should include resource identifier, the response the server returns include enough information that client can modify the resource. Each request to the API should contain all the information to understand the response. 
- Layered System - Between the cliend who send the requests and the server who sends the response back there might be a number of servers in the middle.
    + For example it can contain security layer, caching layer and load-balancing layer.
- Code on demand - This is optional constaint that allow user to request code from the server.

### HTTP
It's acronym of Hyper Text Transfer Protocol that allow to send requests and receive responses via HTTP methods. They might be idemponent if server state can't be changed after several similiar requests like GET, HEAD, PUT, DELETE and the other safe methods. Also I can list non idemponent methods they are CONNECT, PATCH and POST.
HTTP request consists of 3 parts: 
- Starting line that include http method, the request path and http version
- Headers
- Body

### Relational and non-Relational databases
Relational databases based on relations of tables by keys. Non-Relational databases store data in json-like files (not in tables) and don't have any relations.

### Keys
There are 2 groups of keys: Simple and Composite keys. Simple keys are primary key, foreign key and reverse foreign key. In Django you can access to reverse foreign key by assigning "related_name" parameter. 

### DML & DDL
DML is the acronym of Data Manipulation Language. It's group of operators to manipulate with data. It's operators such as SELECT, INSERT, UPDATE and DELETE.
DDL is the acronym of Data Definition Language. It's group of operation to define data. It's operators such as CREATE, ALTER and DROP.

### Index
It is the special tables which can be used by search engine of database for to speed up receiving data. There are clustered and non-clustered indexies. clustered index is faster that non-clustered index. Clustered index data is the main data, but for non-clustered index it's the copy of data. Table can have only one clustered index. 

### Transaction
It's the couple of operations that executing one-by-one and if at least operation in will be failed transaction will be cancelled and rolled back. The main concepts of transaction listed in ACID. It's acronym.
ACID is the acronym of:
- A - Atomicity - It guarantees that every transaction will be saved whole and if at least one operation was failed all transaction will be cancelled and rolled back.
- C - Consistency - It means that every transaction will follow all constraits and rules defined. It guarantees that every tranaction save only valid results.
- I - Isolation - Transactions are often executed concurrently and result of one shouldn't depends on the other one. Levels of transactions may helps to attain it.
- D - Durability - It's guarantees that if we received success of transaction it shouldn't be cancelled by system crash or other failures.

### Transaction Levels
There are 4 transaction levels what I remember. They are:
- READ UNCOMMITED - dirty read is not allowed in postgres, but non-repeateble read, phantom read and serialization anomaly are allowed
- READ COMMITED - same to read uncommited - default level in PG
- REPEATABLE READ - dirty read, nonrepeateble read and phantom read are not allowed. Default level in MySQL.
- SERIALIZABLE - dirty read, nonrepeateble read, phantom read and serialization anomaly are not allowed, bacause tables will blocked during the first transaction executing.

dirty read - A transaction reads data written by a concurrent uncommitted transaction. - not allowed in PG

lost update - Occurs when two transaction reads the same data and then try to update it with a different value. One of it will be lost

nonrepeatable read - A transaction re-reads data it has previously read and finds that data has been modified by another transaction (that committed since the initial read).

phantom read - A transaction re-executes a query returning a set of rows that satisfy a search condition and finds that the set of rows satisfying the condition has changed due to another recently-committed transaction. It's about INSERT and DELETE methods

serialization anomaly - The result of successfully committing a group of transactions is inconsistent with all possible orderings of running those transactions one at a time.

### The first Normalization Form
- The attributes of each table should be simple and consists scalar values.

### The second Normalization Form
- Database is in the first normalizaion form
- Each table describes an entity and the other fields should be moved to another tables

### The third Normalization Form
- Database is in the second normalization form
- The non keyable values which can reference to serveral row should be moved out.

### The Boyсe Codde Normalization Form
- Database is in the third normalization form
- The part of composite key shouldn't depends on not keyable column.
- If there aren't composite keys in our database we can consider that our database is in the Boyce-Codde narmalization form.

### Constraits - NOT NULL, UNIQUE, PRIMARY KEY, FOREIGN KEY etc.

### Django - It's the Python web framework that allow us to create the big e-commerse applications as fast as possible. Django follows MVT or MTV scheme of data division. It's the same to MVC.
- M - Model - It's the single, difinitive source of information about our data. It's a class in which we define all required fields we need.
- V - View - It's the object which takes a request and returns a reponse. There're two possible types of views. They are function-based view and class-based views.
- T - Template - It's a text documents that consists of html tags and django tags which interpreted by django template engine. 
- S - Serializer - It's the objects that takes on input queryset and model instances then it can be converted it to native Python datatypes and easy-rendered to JSON. XML and other content types. 
