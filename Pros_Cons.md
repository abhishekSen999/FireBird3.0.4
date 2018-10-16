Here, we will define the reasons to migrate an existing database to Firebird, and reasons not to.

## Why migrate to Firebird
1. It is open source.
1. It is free.
1. It can run on many platforms, including Microsoft Windows, Linux, Solaris and MacOS X. 
1. It has an OLAP Analysis service built into it and facility for native full-text search (this is available as an add-on to Firebird).
1. For UNIX-like environment, Firebird can have its security integrated with the operating system.

## Why not migrate to Firebird
1. There is no Integrated Replication Support(has be installed as add-on).
1. There is no concept of Temporary Tables.
1. The integration with other database systems through OLE DB as in MS SQL is not possible in Firebird. 
1. It does not have the ability to work with XML directly as in MS SQL that supports partitioned views for better performance on tables which span several servers.
