# Database  
**What are the different subsets of SQL?**  
Data Definition Language (DDL) – It allows you to perform various operations on the database such as CREATE, ALTER, and DELETE objects.  
Data Manipulation Language(DML) – It allows you to access and manipulate data. It helps you to insert, update, delete and retrieve data from the database.  
Data Control Language(DCL) – It allows you to control access to the database. Example – Grant, Revoke access permissions.  

**What is an ACID transaction?**  
In the context of transaction processing, the acronym ACID refers to the four key properties of a transaction: atomicity, consistency, isolation, and durability.  

Atomicity  
All changes to data are performed as if they are a single operation. That is, all the changes are performed, or none of them are.  
For example, in an application that transfers funds from one account to another, the atomicity property ensures that, if a debit is made successfully from one account, the corresponding credit is made to the other account.  
Consistency  
Data is in a consistent state when a transaction starts and when it ends.  
For example, in an application that transfers funds from one account to another, the consistency property ensures that the total value of funds in both the accounts is the same at the start and end of each transaction.  
Isolation  
The intermediate state of a transaction is invisible to other transactions. As a result, transactions that run concurrently appear to be serialized.  
For example, in an application that transfers funds from one account to another, the isolation property ensures that another transaction sees the transferred funds in one account or the other, but not in both, nor in neither.  
Durability
After a transaction successfully completes, changes to data persist and are not undone, even in the event of a system failure.  
For example, in an application that transfers funds from one account to another, the durability property ensures that the changes made to each account will not be reversed.  

**What do you mean by denormalization?**  
Denormalization refers to a technique which is used to access data from higher to lower forms of a database. It helps the database managers to increase the performance of the entire infrastructure as it introduces redundancy into a table. It adds the redundant data into a table by incorporating database queries that combine data from various tables into a single table.  

**What are Entities and Relationships?**  
*Entities*:  A person, place, or thing in the real world about which data can be stored in a database. Tables store data that represents one type of entity. For example – A bank database has a customer table to store customer information. The customer table stores this information as a set of attributes (columns within the table) for each customer.  

*Relationships*: Relation or links between entities that have something to do with each other. For example – The customer name is related to the customer account number and contact information, which might be in the same table. There can also be relationships between separate tables (for example, customer to accounts).

**What is Normalization and what are the advantages of it?**  
Normalization in SQL is the process of organizing data to avoid duplication and redundancy. Some of the advantages are:  

- Better Database organization
- More Tables with smaller rows
- Efficient data access
- Greater Flexibility for Queries
- Quickly find the information
- Easier to implement Security
- Allows easy modification
- Reduction of redundant and duplicate data
- More Compact Database
- Ensure Consistent data after modification   

**Explain different types of Normalization**
There are many successive levels of normalization. These are called normal forms. Each consecutive normal form depends on the previous one.The first three normal forms are usually adequate.  

- First Normal Form (1NF) – No repeating groups within rows
- Second Normal Form (2NF) – Every non-key (supporting) column value is dependent on the whole primary key.
- Third Normal Form (3NF) – Dependent solely on the primary key and no other non-key (supporting) column value.