# Reading 11: Mongo and Mongoose

## SQL vs NoSQL
| SQL | NoSQL |
| --- | ----- |
|  Relational Databases (RDBMS) | Non-Relational or Distributed Database |
| Table Based Databases | Document Based, Key-Value Pairs, Graph Databases or Wide-Column Stores |
| Predefined Schema | Dynamic Schema for Unstructured Data |
| Vertically Scalable | Horizontally Scalable |
|  Scaled by Increasing the Horse-Power of the Hardware | Scaled by Increasing the Databases Servers in the Pool of Resources to Reduce the Load |
| MySql, Oracle, Sqlite, Postgres and MS-SQL | MongoDB, BigTable, Redis, RavenDb, Cassandra, Hbase, Neo4j and CouchDb |
| Good Fit for the Complex Query Intensive Environment | Not Good Fit for Complex Queries |


## What kind of data is a good fit for an SQL database?
  - Complex Query Intensive Environment

## Give a real world example.
  - Oracle Express Edition, MS-SQL Server Express Edition, MySQL Community Edition

## What kind of data is a good fit a NoSQL database?
  -  Database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data
  -  Highly preferred for large data set

## Give a real world example.
  - MongoDB, CouchDB, Redis

## Which type of database is best for hierarchical data storage?
  - NoSQL
  
## Which type of database is best for scalability?
  - SQL

## What does SQL stand for?
  - Structured Query Language
## What is a realational database?
  - A type of database that stores and provides access to data points that are related to one another

## What type of structure does a relational database work with?
  - The relational model means that the logical data structures—the data tables, views, and indexes—are separate from the physical storage structures. This separation means that database administrators can manage physical data storage without affecting access to that data as a logical structure. For example, renaming a database file does not rename the tables stored within it

## What is a ‘schema’?
  - Logical configuration of all or part of a relational database. It can exist both as a visual representation and as a set of formulas known as integrity constraints that govern a database

## What is a NoSQL database?
  -  Databases that store data in a format other than relational tables

## How does it work?
  - Each type of NoSQL database would be designed with a specific customer situation in mind, and there would be technical reasons for how each kind of database would be organized. The simplest type to describe is the document database, in which it would be natural to combine both the basic information and the customer information in one JSON document. In this case, each of the SQL column attributes would be fields and the details of a customer’s record would be the data values associated with each field

## What is inside of a Mongo database?
  - stores data records as documents (specifically BSON documents) which are gathered together in collections. A database stores one or more collections of documents.

## Which is more flexible - SQL or MongoDB? and why.
  - MongoDB: it has the ability to handle large amounts of unstructured data quickly. Higher scalability.
 
## What is the disadvantage of a NoSQL database?
 - Schema-less, No or very few Relations, Data is typically merged or nested in few collections,  
