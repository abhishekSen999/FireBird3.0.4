# FireBird
> Firebird is an open source SQL relational database management system that "runs on **Linux, Microsoft Windows, MacOSX, and several Unix platforms.**"

## Features
Some main features of firebird are listed below:
### Full support for stored procedures and triggers
Stored procedures & triggers are prepared SQL codes that can be save and reused multiple times. Triggers are special procedures that automatically execute when an event occurs in the database server.

### Full ACID compliant trasactions
ACID are the set of properties of database transactions intended to guarantee validity even in the event of errors, power failure, etc. These properties are as follows:
1. **Atomicity**: It guarantees that each transaction is treated as a single "unit", which either succeeds completely, or fails completely i.e. there is no state when the transaction is left partially executed.
2. **Consistency**: It ensures that transaction can only bring the database from one valid state to another, maintaning database invariants(any data written on database must be valid according to defined rules on the database)
3. **Isolation**: It ensures the concurrent execution of transactions leave the database in the same state that would have been obtained if the transactions were executed sequentially.
4. **Durability**: It guarantees that once a transaction have been committed, it will remain committed even in the case of system failure.

### Referential Integrity
It is the property of data stating references within it are valid. Referential Integrity Rule states that any column in the base table declared as foreign key can contain either a **null value** or only values from a parent's table **primary key or candidate key**.

### Mutli Generational Architecture
MGA (Multi Generational Architecture) is based on the concept of **readers don't block writers and writers don't block readers**. It creates mutiple version of records kept in database as long as any one transaction needs it. Each transaction has it's different view of the consistent database at any moment.

### Support for External Functions
User Defined Functions in SQL Server is a programming construct that accepts parameters, performs task on accepted parameters, and returns a type of result.

### Incremental Backup
It maintains successive copies of the data containing only the portion that has changed since the preceding backup copy. During the full recovery all the incremental backups and last full backup are needed until the point of restoration.

> Note: Differenct between UDF & Procedure (https://stackoverflow.com/questions/2039936/difference-between-stored-procedures-and-user-defined-functions)

## Awards
1. **2007** SourceForge Community Choice Award: Best Project for enterprise, Best user support.
2. **2009** SourceForge Community Choice Award: Best Project for enterprise. Finalist on Best Project and Best Project for Government.