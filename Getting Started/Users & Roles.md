We now have a database, but its not good to have all database under SYSDBA account. 
<br >**For example**: We are running multiple databases beloging to different people, so we wish to have their own respective database for each group, with no rights to view other databases. *Another Scenario* may be we need a proxy user able to access all databases, but does not have all the superuser rights of **SYSDBA**

<br >In this section we will create a new database user, and assign viweing and updating rights to the account.

<br >To create a new user we will user **gsec** prompt with SYSDBA user and then create new user with username *TestAdmin* <br >

> add TestAdmin -pw testadmin -fname First -lname Administrator

<br >![Step 1](https://github.com/krishna1401/FireBird3.0.4/blob/master/Getting%20Started/UR1.PNG)

<br >*Note*: uid & gid are used on some POSIX systems to enter the Unix userid and groupid(Default 0).

<br >Next, we open the database, create a *firstdbadmin* ROLE for the database, assign the appropriate rights to that role, then add *TestAdmin* to the role.<br >

> CREATE ROLE firstdbadmin;
<br >

> GRANT SELECT, UPDATE, INSERT, DELETE ON sales_catalog TO ROLE firstdbadmin;
<br >

> GRANT firstdbadmin TO TestAdmin;
<br >

> quit;

<br >![Step 2](https://github.com/krishna1401/FireBird3.0.4/blob/master/Getting%20Started/UR2.PNG)

<br >We will now test our database with the new user *testadmin*. Login isql prompt with *testadmin* user.<br >

> isql firstdb.fdb -user TestAdmin -password testadmin -role firstdbadmin
<br >

> DELETE FROM sales_catalog;
<br >

> INSERT INTO sales_catalog VALUES('001', 'Aluminum Wok', 'Chinese wok');
<br >

> INSERT INTO sales_catalog VALUES('002', 'Microwave Oven', '300W Microwave oven');
<br >

> SELECT * FROM sales_catalog;

<br >![Step 3](https://github.com/krishna1401/FireBird3.0.4/blob/master/Getting%20Started/UR3.PNG)

<br > To test the Role play of user we will create a new table *test_role* with **SYSDBA** and will try to access it using **testadmin**.<br >
**Create table using SYSDBA** <br > 
> isql firstdb.fdb -user SYSDBA -password newpass
<br >

> CREATE TABLE test_role(item varchar(10) primary key not null);
<br >

> INSERT INTO test_role VALUES('101');
<br >

> INSERT INTO test_role VALUES('10');
<br >
> SELECT * FROM test_role;
<br >

> quit;

<br>**Access table using testadmin**<br >
> isql firstdb.fdb -user TestAdmin -password testadmin
<br >

> SELECT * FROM test_role

<br >![Step 4](https://github.com/krishna1401/FireBird3.0.4/blob/master/Getting%20Started/UR4.PNG) 

<br >*Note*: To exit the sql prompt, simply type **quit;** and press **ENTER**