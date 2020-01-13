---
title: Database Introduction and Concepts
date: "2017-08-28T21:40:32.169Z"
description: Most computer systems, from the simplest customer management system, to the most complex operations control system, rely on some information being stored, accessed and updated.
---

![database](./database.jpg)

##Purpose of a database
The purpose of a database is to provide a storage for an organisation's data and meet the data access needs of the users it serves. Most organisations will have multiple software applications and databases supporting various parts of the business. The type and structure of the database will be guided by the needs of the business, and of the applications that are being designed to support those needs.

###The main technical requirements for a database system are that it is:

1. Reliable and available (responds to every request)
2. Consistent (always returns the latest data - especially important for multi-user transactional data, such as payment information)
3. Fast and efficient (data is returned in a timely fashion)

###Data storage
Data storage comes in many forms, from flat files to tables and documents. The most common type of data storage is the relational database which uses tables with predefined structures and data types. 

With the exponential growth in data collected by computer systems and connected devices around the world (known as Big Data), other data storage mechanisms have been developed to store large amounts of data in less structured forms. Among these are the NoSQL databases which will be discussed in a later module. One example is a document database, which stores key-value pairs where the key is a unique identifier, and the value is a complex structure called "document".

###Data access

- For relational databases data is accessed using a structured query language which refers to the structure of the data on the database. You will be learning one such query language (T-SQL) in this course. 

- For many big data storage systems, access to the data is provided through an API (Application Programming Interface), using a specific notation for the data objects, the most common being the JavaScript Object Notation (JSON). The API can be called via the same protocol as web pages: HTTP.
The way data can be accessed (read, manipulated) is highly dependent on the type of storage used. 

- More and more organisations, especially but not limited to governmental organisations, offer their data to be used openly by others, either for interpretation via data visualisations, or for use in their own applications. This approach is also used internally within an organisation, to allow different information systems to interact with each other.  

###Data Structure
In relational databases the structure of database tables is very specific and predefined, made up of tables, fields, data types, relationships and more. This structure is called a database schema. There are two parts to this, the logical schema which is the design of the database (the architect's plan), and the physical schema, which is the database actually created on a server (the built house).


### Essential Database Terminology

####Tables, Rows, Columns
In the most common types of databases, the structure in which data is stored is called a table. A table often corresponds to some category of people, things or entities in the real world, for example a Customer table, or an Invoice table. 

A database then, is a collection of data structures (tables) that represent the problem domain under consideration (for example the problem domain "invoicing for plumbing services" would use an "Invoicing" database, with tables for customers, invoices, and possibly plumbing parts and payments, depending on the exact problem specification.)

A table's rows represent one item of data, also called a record, and would correspond to one entity in the real world (for example customer Harry White, or invoice #016-248.) In relational databases these are called tuples.

A table's columns represent the information stored about the entity, for example the customer's firstName, lastName, streetAddress and city. These are also called fields or attributes.

In relational databases, which are the main topic of this course, the formal names for tables, rows and columns are: relations, tuples and attributes. However you will find these equivalent terms used interchangeably.

###Data Types and Constraints
When designing and implementing a database for a client application,  there is a need to follow the client's business rules or requirements. This requires to specify some constraints on what can go in each table and each field.

The simplest type of constraint is to specify the data type of each field. There are general data types such as integer, date, character, text and many more that are very specific. you will learn about these in the Structured Query Language module. For example an invoiceDate field will have a data type of date, a price field will be decimal.

The next type of constraint limits the range of values that are allowed, for example "dateOfBirth must be in the past, and no earlier than 1.1.1905". 

Fields and tables also have to obey more complex business rules that are expressed through table constraints and relationship constraints (for example "you cannot enter an invoice without a customer").
