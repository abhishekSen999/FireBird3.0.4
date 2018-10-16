Now, we are going to create our own database and perform simple SQL insert query over it. 
<br >To create our database, we will need to use the isql tool. Firebird saves its databases under discrete files, and, by convention, the extension is **.fdb**. 
<br >**Note**: .fdb extension is just a convention, and that you can save the database as any extension you wish.

We will first create our database using SYSDBA user in the Firebire directory itself. We will run the isql tool and execute the **CREATE DATABASE** command as follows:<br >
> CREATE DATABASE 'firstdb.fdb' USER 'sysdba' PASSWORD 'newpass';

<br >This will create a file called **firstdb.fdb** inside the current directory. The databse is owned by SYSDBA. We will create a simple Sales catalog table and fill it with some data.
<br >**Note**: If you are not familiar with SQL please follow the link (https://www.tutorialspoint.com/sql/)
<br >**Note**: Before using the database we always need to connect to the database

> CREATE TABLE sales_catalog (item_id varchar(10) not null primary key, item_name varchar(40) not null, item_desc varchar(50));
<br >

> INSERT INTO sales_catalog VALUES('001','Aluminium Wok', 'Chinese wok used for stir fry dishes');
<br >

> INSERT INTO sales_catalog VALUES('002', 'Chopsticks extra-long', '60-cm chopsticks');
<br >

> INSERT INTO sales_catalog VALUES('003', 'Claypot', 'Pot for stews');
<br >

> INSERT INTO sales_catalog VALUES('004', 'Charcoal Stove', 'For claypot dishes');
<br >

> SELECT * FROM sales_catalog;

<br >![Step 1](https://github.com/krishna1401/FireBird3.0.4/blob/master/Getting%20Started/CD1.PNG)

<br >**Note**: While opening isql prompt always specify the user to define the operations you need to perform i.e. default user cannot modify the tables in the database.

<br >**Note**: To exit the sql prompt, simply type **quit;** and press **ENTER**