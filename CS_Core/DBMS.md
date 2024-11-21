## Transactions and concurrency control
- **Trancasction**
  - it is a single logical unit of work that access and possibly alters the contents of a database.
  - It uses read and write operations to manage data.
  - **ACID Propertiese** - A transaction should follow these properties to ensure db consistency before and after a transaction.
    - **Atomicity**
      - Entiner transaction is executed or nothing none of it is.
      - No partial execution
      - **Abort** if transaction is abborted then any changes to the db are not visible
      - **commit** if transaction is committed then changes are visible
    - **Consistency** Valid state maintenanceintegrity constraints must be maintained so that the db remains consistent before and after the transaction. It ensures the correctness of the db.
    - Example: Referring to the previous example, the total amount before and after the transaction must be the same. If initially, Account X has £500 and Account Y has £200, then:
    - Total before transaction T = £500 + £200 = £700
    - Total after transaction T = £400 + £300 = £700
    - The database remains consistent. If T1 completes but T2 fails, the transaction T is incomplete, causing inconsistency.
    - **Isolation** Transactions do not affect each other
      - Isolation ensures that multiple transactions can occur concurrently without causing database inconsistency.
      - Transactions operate independently without interference.
      - Changes made in a particular transaction are not visible to other transactions until those changes are written to memory or committed.
    - **Durability** Permanent changes after commitment
      - Durability guarantees that once a transaction has been completed, its updates and modifications are stored on disk and persist even in the case of a system failure.
      - These updates become permanent and are stored in non-volatile memory.
    - Advantages of ACID Properties in DBMS:
      - Data Consistency: Maintains consistent and accurate data after transaction execution.
      - Data Integrity: Ensures that changes to the database are permanent.
      - Concurrency Control: Manages multiple transactions occurring simultaneously, preventing interference.
      - Recovery: Enables the system to recover data up to the point of failure.
    - Disadvantages of ACID Properties in DBMS:
      - Performance: This can cause performance overhead due to additional processing.
      - Scalability: This may pose scalability challenges in large distributed systems.
      - Complexity: Implementation can increase system complexity and require significant resources.
# DBMS
- Data inconsistency - updates remain unchanged
- Data redundancy - duplication
- consistency - A transaction must transition the database from one valid state to another, maintaining data integrity according to defined rules (e.g., constraints, triggers). 
- concurrency:- Allows multiple users to access data simultaneously
- concurrency control:- how a user can access data, for ex:- if a read operation is there then multiple users can see the data, for write only one user can access it
- data integrity:- ensures accuracy and consistency of the data.
- A DBMS should have:-
  - Data Integrity: Ensure data accuracy and consistency.
  - Security: Provide mechanisms to protect data from unauthorized access.
  - Scalability: Handle increasing amounts of data and users efficiently.
  - Performance: Enable fast data retrieval and processing.
  - Backup and Recovery: Support data recovery in case of failures.
  - Concurrency: Allows multiple users to access data simultaneously without conflicts.
  - Flexibility: Support various data types and structures.
  - Ease of Use: Provide user-friendly interfaces and query tools.
  - Data Independence: Separate the application logic from the physical storage of data.
  - Transaction Management: Maintain database consistency through ACID properties (Atomicity, Consistency, Isolation, Durability)
    - Atomicity: A transaction must be treated as a single, indivisible unit. Either all its operations are completed, or none are applied.
    - Consistency: A transaction must transition the database from one valid state to another, maintaining data integrity according to defined rules (e.g., constraints, triggers). 
    - Isolation: Transactions should execute independently, without interference. The result should be as if each transaction were executed sequentially. 
    - Durability: Once a transaction is committed, its changes are permanent, even in case of system failure (e.g., power outage). 
## Introduction to DBMS
### Data, Information, Database, and File system
- **Data** is a collection of raw facts from which meaning or knowledge can be extracted.
- **Information** extracted knowledge from the data is known as information
- **Database** is a structured collection of data in a way that allows retrieval, updating, and manipulation of information.
- **File system**
  - Os uses this type of system to manage data. For example, hard drives and USB drives.
  - Disadvantages:-
    - Data security
    - Data inconsistency
    - Poor memory utilization
    - data redundancy

### DBMS:- Database management system
- It is a software application(interface) between database and user, designed to efficiently **store(organize), retrieve(search), manipulate(update, add, delete), and manage** large volumes of data with **access control, concurrency control, data integrity**.
 
- Application
- Need, advantages, disadvantages
- Data Abstraction
  - It is hiding unnecessary complexities from the user
  - 3 levels of abstraction i.e. view level, logical level, physical level
    - **View level** This is the highest level of data abstraction. It describes the interaction between users and the database system, focusing on what users can see and access.
    - **Logical Level** This is the middle level of the 3-level data abstraction architecture. It describes what data is stored in the database and how it is structured.
    - **Physical Level** This is the lowest level of data abstraction. It describes how data is stored in a database, providing details about complex data structures.
- Database Architecture
  - Levels/ Data abstraction
    - show what is needed and high other complexities
    -  Physical Level/ Internel Level
      - physical storage of data
      - responsible for storing and retrieving data from storage devices like ssd or hdd.
      - Data compression, indexing and storage allocation is implemented here 
    -  Logical Level/ Conceptual Level
      - overall organization of data in the db and relationships between them is here
      - it defines the schema which includes tables, attributes and their relationships   
    -  View Level/ Externel Level
      - deals with how user access the data in db
      - allows user to view data in a way that makes sense to them
      - provides view interfaces to the tb 
  - 2-tire
    - database - user
  - 3-tire
    - database - DBMS - user
      - more secure, more scalability, more users can interact with this 
#### Types of databases
- Relational Databases
- Object Oriented Databases
- NoSQL Databases
- Hierarchical Databases
- Network Databases



## Data Models
- It is an abstract way to represent how data is structured and organized within a db.
- It shows logical arrangement of data and connections between different data components.
- It is used for undeerstanding and designing of databases.
### Types of Data Models
- **Hierarchical Data Model**
- **Network Data Model**
- **Relational Data Model**
  - The relational model organizes data into tables (known as relations) with rows and columns. It is the most common data model and is based on set theory, using Structured Query Language (SQL) for data manipulation.
- **Entity Relationship Model (ER Model)**
  - The ER model is used to design relational databases by representing data as entities (objects), attributes (properties of entities), and the relationships connecting these entities.
- **Object Oriented Data Model**
- **NoSQL Data Models**

















# Mind-Map
- Introduction
  - What is a database
  - what is DBMS
  - need for DBMS
  - File management vs DBMS
  - DB Tier-2/Tier-3 Architecture
  - Data Abstraction in DBMS
    - 3 levels of data abstraction
- Types of DBMS
  - Relational
  - NoSQL
  - Object-Oriented
  - Hierarchical
  - Network
- Database Design
  - Schema
  - ER Model (Entity-Relationship)
  - Relational Model
    - Keys
      - Primary Key
      - Foreign Key
      - Composite Key
      - Candidate Key
  - Normalization
  - Denormalization
- Transactions
  - ACID Properties
    - Atomicity
    - Consistency
    - Isolation
    - Durability
  - Concurrency Control
    - Locking: Shared and Exclusive
    - Deadlock Handling
    - Multiversion Concurrency Control (MVCC)
- Indexing
  - Types
    - Primary
    - Secondary
    - Clustered
    - Non - clustered
  - Data Structures
    - B-Tree
    - Hash Index
- Database Storage
  - Disk Storage: HDD, SSD
  - File Organization
    - Heap Files
    - Sorted Files
    - Hashed Files
  - Buffer Management
    - Caching
    - Page Replacement
- Backup and Recovery
- Backup Types
  - Full Backup
  - Incremental Backup
  - Differential Backup
- Recovery Techniques
  - Log-based Recovery
  - Checkpoints
  - Shadow Paging
- Distributed Databases
- Characteristics: Multiple locations
- Replication: Copying data across servers
- Sharding: Partitioning data
- CAP Theorem
  - Consistency
  - Availability
  - Partition Tolerance
- Security
  - User Authentication
  - Authorization
  - Encryption
  - Data Masking
  - SQL Injection Prevention
- Databases
  - SQL Databases
  - NoSQL DataBases
    - Document Store (MongoDB)
    - Key-Value Store (Redis)
    - Column Family Store (Cassandra)
    - Graph Database (Neo4j)

# 1. Types of DBMS
## 1.1 Mind Map
- Relational
- NoSQL
- Object-Oriented
- Hierarchical
- Network
## 1.2 Relational


# 3. Database Design
- Database design defines how data will be stored, organized, and managed in a database. It ensures data is structured efficiently and can be accessed and manipulated effectively.
- **Data Model:** Collection of conceptual tools for describing data, data relationships, data semantics, and consistency constraints. 
## Mind Map
- Schema
- ER Model (Entity-Relationship)
- Normalization
- Denormalization
- Keys
  - Primary Key
  - Foreign Key
  - Composite Key
## 3.1 Schema
- **Definition:** A schema is the blueprint or structure of a database. It defines the tables, fields (columns), and relationships between them.
  - A schema is the structure or layout of the entire database. It defines how the database is organized, what tables it contains, what fields are in each table, and how they are related. Essentially, it's the blueprint of the database.
  - **Tables** in a schema represent real-world entities, while columns (also called fields or attributes) represent the properties of those entities.


## 3.2 ER Model
### Mind Map
- Components of an ER Diagram
  - Entity
    - Strong Entity
    - Weak Entity
  - Attributes
    - Simple
    - Composite
    - Multi-Valued
    - Derived
  - Relationships
    - One to one Relationship
    - one to many Relationship
    - many to one Relationship
    - many to many Relationship
  - Cardinality and Participation
    - Cardinality
      - One to one, one to many, many to one, many to many
    - Participation
      - Total Participation
      - Partial Participation
### 1. Entity
- An entity in an ER diagram represents a real-world object or concept that has significance in the system and can be stored in the database. Entities are represented by rectangles.
- Types of Entities:
  - Strong Entity:
    - Can exist independently and has a primary key that uniquely identifies it.
    - Example: A Customer in an online shopping system is a strong entity because it can be uniquely identified using a customer_id.
  - Weak Entity:
    - Cannot exist without being related to another entity. It relies on a strong entity for its existence and is identified using a partial key along with the primary key of the strong entity.
    - Example: An OrderItem in a shopping system is a weak entity because it cannot exist without an Order. The OrderItem is identified by combining order_id and item_id.
- Entity Example:
  - Entities: Customer, Order
  - Customer can have attributes like customer_id, name, email.
  - Order can have attributes like order_id, order_date.
### 2. Attributes
- Attributes are properties or characteristics of an entity. They are represented by ovals connected to their respective entities with lines.
- Types of Attributes:
  - Simple Attribute: Holds a single value for an entity (e.g., name, email).
  - Composite Attribute: Can be divided into smaller sub-parts (e.g., an address can be broken down into street, city, zip_code).
  - Multi-valued Attribute: Can hold multiple values for an entity (e.g., a phone_numbers attribute can hold more than one value).
  - Derived Attribute: A value that can be calculated from other attributes (e.g., age can be derived from birthdate).
- Attribute Example:
  - For the Customer entity:
  - Simple Attributes: name, email, customer_id.
  - Composite Attribute: address (can be split into street, city, zip_code).
  - Multi-valued Attribute: phone_numbers (a customer may have multiple phone numbers).
### 3. Relationships
- A relationship is an association between two or more entities. Relationships are represented by diamonds in ER diagrams. The entities involved in the relationship are connected to the diamond with lines.
- Types of Relationships:
  - One-to-One (1:1): One entity instance in a table is related to exactly one entity instance in another table. Example: Each Person has one Passport, and each Passport is assigned to one Person.
  - One-to-Many (1: M): One entity instance in a table is related to many entity instances in another table. Example: One Customer can place multiple Orders, but each order belongs to only one customer.
  - Many-to-One (M:1): Many instances of one entity are associated with one instance of another entity. Example: Many Orders may be placed by the same Customer.
  - Many-to-Many (M: M): Many instances of an entity are associated with many instances of another entity. Example: Many Students can enroll in many Courses, and many Courses can have many Students.
- Relationship Example:
  - Entities: Customer, Order.
  - Relationship: Places (A Customer places an Order).

### 4. Cardinality and Participation
- Cardinality
  - Cardinality defines the number of instances of one entity that can or must be associated with each instance of another entity in a relationship. Participation determines whether all instances of an entity must participate in a relationship.
  - Cardinality Examples:
    - One-to-One (1:1): Each Employee has one Workstation.
    - One-to-Many (1:M): A Customer can place multiple Orders.
    - Many-to-One (M:1): Many Orders are linked to one Customer.
    - Many-to-Many (M:M): Students enroll in multiple Courses, and Courses have many Students.
- Participation Types:
  - Total Participation: Every instance of the entity must be involved in the relationship. Example: Every Order must be placed by a Customer, so the Order has total participation in the Places relationship.
  - Partial Participation: Only some instances of the entity may be involved in the relationship. Example: Not every Customer places an Order, so the Customer has partial participation in the Places relationship.
  
- ![image](https://github.com/user-attachments/assets/d04f239b-38ba-4c0d-b75f-7d07c0a0b176)


## 3.3 Relational Model
- It structures data into tables (also called relations), where each table is made up of rows (tuples) and columns (attributes). This model forms the basis of most modern databases (like MySQL, PostgreSQL, and Oracle) and provides a straightforward way to organize and manipulate data.

### 3.3.1 Basic Concepts of the Relational Model
- Relation (Table): A relation is essentially a table in the database. It consists of rows and columns. Each relation represents a set of related data. For example, a "Student" table would store data related to students.
- Tuple (Row): A tuple is a single row in a table, representing one record or data entry. Example: A single row in a "Student" table may represent one student’s details (like student_id, name, email).
- Attribute (Column): An attribute is a column in a table, representing a property of the entity that the table stores. Example: In the "Student" table, attributes might include student_id, name, email, etc.
- Domain: A domain is a set of permissible values for a given attribute. It defines the type and range of data that can be entered in that column.
Example: The domain of the age attribute in a "Student" table might be integers between 1 and 120.
### 3.3.2 Characteristics of a Relational Table
- Each row is unique: No two rows in a table are identical, ensuring that each tuple can be uniquely identified.
- The order of rows does not matter: The relational model does not rely on the order of rows; they can be displayed in any order without affecting the integrity of the data.
- The order of columns does not matter: The order of attributes in the table does not matter. As long as the data is associated with the correct column, the table remains valid.
- All values are atomic: Each attribute in a table contains a single value. This is known as the atomicity property, which means that a field should not contain multiple values (e.g., a single cell should not hold multiple email addresses).
### 3.3.3 Keys in the Relational Model
- Keys are crucial in the relational model because they ensure data integrity and help establish relationships between tables.
- Type of Keys
  - Primary Key: A primary key is an attribute (or set of attributes) that uniquely identifies each tuple (row) in a relation (table). Example: In a "Student" table, the student_id is the primary key because each student has a unique ID.
  - Foreign Key: A foreign key is an attribute in one table that refers to the primary key of another table. This establishes a relationship between the two tables. Example: An order table might have a customer_id that references the primary key customer_id in the "Customer" table. This ensures that each order is linked to an existing customer.
  - Candidate Key: A candidate key is an attribute (or set of attributes) that could potentially serve as the primary key. If a table has multiple candidate keys, one is selected as the primary key.
  - Composite Key: A composite key is a combination of two or more attributes that, together, uniquely identify a tuple. Example: In a "Course_Registration" table, where no single attribute can uniquely identify a row, a combination of student_id and course_id might serve as the composite key.
### 3.3.4. Relationships Between Tables
- In the relational model, relationships between tables are established using foreign keys. These relationships allow the data in one table to be connected to data in another.
- Types of Relationships:
  - One-to-One (1:1): Each row in one table is related to only one row in another table. Example: A "Person" table and a "Passport" table where each person has only one passport.
  - One-to-Many (1:M): One row in one table is related to multiple rows in another table. Example: A "Customer" can place multiple "Orders", but each order belongs to only one customer.
  - Many-to-Many (M:M): Rows in one table are related to multiple rows in another table, and vice versa. Example: A "Student" can enroll in many "Courses", and each "Course" can have many "Students". This relationship is typically modeled using a third table (called a junction or associative table), such as "Student_Course".
### 3.3.5. Integrity Rules
- To maintain the consistency and accuracy of data, the relational model enforces certain integrity constraints:
- **Entity Integrity:**
  - Ensures that the primary key of a table is unique and not null. This ensures that each record in a table can be uniquely identified.
  - Example: A "Student" table’s primary key student_id cannot have duplicates or null values.
- **Referential Integrity:**
  - Ensures that a foreign key value in one table must match a primary key value in another table, or it must be null.
  - Example: If a customer_id in the "Order" table references a customer_id in the "Customer" table, it must match an existing customer or be null.

### 3.3.6 Advantages of the Relational Model
- Simplicity: Easy to understand and use with clearly defined tables, columns, and relationships.
- Data Integrity: Enforces strict rules (like primary and foreign keys) to ensure data accuracy.
- Flexibility: Can handle complex relationships between data and allows easy querying through SQL.
- Normalization: Supports normalization to remove redundancy and improve data integrity.
- Scalability: Well-suited for scaling large databases with millions of records.

## 4. Normalization
