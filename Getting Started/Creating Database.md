Now, we are going to create our own database and perform simple SQL insert query over it.

To create our database, we will need to use the isql tool. Firebird saves its databases under discrete files, and, by convention, the extension is **.fdb**. 
*Note*: .fdb extension is just a convention, and that you can save the database as any extension you wish.

We will first create our database using SYSDBA user in the Firebire directory itself. We will run the isql tool and execute the **CREATE DATABASE** command as follows:
> CREATE DATABASE 'firstdb.fdb' USER 'sysdba' PASSWORD 'newpass';