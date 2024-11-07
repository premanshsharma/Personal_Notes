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
- Data Models
  - Relational Model: Tables (Relations), Attributes (Column), Tuples (Rows)
  - Hierarchical Model: Parent-child Relationships
  - Network Model: Many to Many Relationships, One to Many Relationships, Many to one Relationships, one to one Relationships
  - Object-Oriented Model: Objects, Classes, Inheritance
  - NoSQL Models: Documents-Based, Key-Value, Column-Family, Graph-Based
- Database Design
  - Schema
  - ER Model (Entity-Relationship)
  - Normalization
  - Denormalization
  - Keys
    - Primary Key
    - Foreign Key
    - Composite Key
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
