---
title: "CSL362: Database Management System - Concepts, Terms and Data Models"
date: 2019-01-18
categories: [CSL362]
---
{% include lib/mathjax.html %}

## Course Contents
1. Concepts and Terms
2. Data models (ER model and Relationship model)
3. Database language (SQL : high level, Relational algebra : low level)
4. Normalization Theory
5. Database storage and indexing
6. Query processing and optimization
7. Transaction processing (Concurrency and Recovery)

The points 1 - 4 cover the uses of DBMS, i.e. developing a database application whereas 5 - 7 cover the implementational issues.

### Concepts - What is a DBMS?
It is a colletion of **inter-related data** (database) and a **set of programs** to access these data. <br>
These set of programs generally involve the foll. functionalities:
- Storage
- Retrieval
- Additional 
    - Consistency of data
    - Security of data

### Concepts - Why DBMS?
The limitations of a *file-processing* approach to store and process data which involves many programmers, are:
1. **Data Redundancy** and **inconsistency**
2. **New functional requirements** if are to be added, it is cumbersome
3. **Data integrity** problems: when consistency constraints are not satisfied
4. **Atomicity problem**: Either **all** or **none** situation. If partial execution of write queries due to some issues, can cause an inconsistency.
5. **Concurrent access anomalies**: <br>
For e.g. in a course registration database, for a particular course A, maximum 50 students can register. If currently, 49 students are registered and 2 students register **simultaneously** for course A, the code snippet 
```
    if (courseRegistrations < 50) {
        courseRegistrations += 1;
    }
```
can lead to inconsistency and show that only 50 students have registered but actually 51 are registered.

### Terms
#### Database Schema
The overall design of the database is called the **database schema**.

For e.g.:

Employee_Code | Name | Address | ... 

These fields are a part of the schema. Also, the constraints that Employee_Code is **char(6)** and is a **primary key**, i.e. consistency constraints are part of the schema.

#### Database Instance (State)
The collection of information stored in the database at a particular point of time is called an instance of the database. 

For e.g. : The rows of an employe table.


Employee_Code | Name | Address | ... 
E_01 | XYZ | ABC | ...
E_02 | ...  | ...  | ...  
.  | .  |  . |
.  | .  |  . |
.  | .  |  . |
E_500 | ... | ... | ...

- Typically, database state is changed frequently but schema is not changed so frequently.

#### Database Language
1. **Data Definition Language (DDL)** - This is used to change the schema. e.g: CREATE TABLE.
2. **Data Manipulation Language (DML)** - This includes SELECT, INSERT, UPDATE, etc.

- DBMS typically have **metadata** and **database**. The metadata is the schema or system catalog or data dictionary. It is actually data about the data.
- In a SQL command, **SELECT A from T1**, the existence of the table T1 is actually checked from the metadata.
- Every write statement changes the state of the database.

#### Data Abstraction
1. **View Level** - It includes different views and the users above which can see those views. 
2. **Logical Level** - It describes what data are stored, the index, constraints, i.e. schema. DDL statements are executed at this level. Database Designers and Administrators generally work at this level.
3. **Physical Level** - It describes how the data are actually stored? Database developers generally work at this level.

- Every user must not have complete access of the database.

### Data Models
The main emphasis is on ER models and how they map into relational models which is the practical point of view.

#### Entity - Relationship Model (ER Model)
It is consisting of a collection of basic objects called **entities** and **relationships** among these objects.
<br>
An ER model is expressed via an **ER diagram**. The following terms are to be understood first:
1. **Entity**: It is a "thing" or "object" in the real-world that is distinguishable from all other objects. An entity is characterized by a set of attributes and their values. Examples for entities include Students, Courses, Bank account, etc. A Student entity can have ID, Name, ... as its attributes.
2. **Entity Type**: It defines a collection of entities that have the same attributes.
3. **Entity Set**: The collection of all entities of an entity type at a particular point of time is called an entity set.

Since typing handwritten notes takes a lot of time, directly read handwritten notes for remaining part of this lecture [here](https://drive.google.com/file/d/14gIELshg8bWgOJboeMQxRikeIdiNvNF9/view?usp=sharing). (Pages 6-11)