The default system administration account has the user name **SYSDBA** and the case-sensitive password *masterkey*.

The administrative tools available with the software are:
1. **gsec**: This is a security administrator, used to create, modify & delete users, change passwords, etc.
2. **isql**: This is a interactive SQL tool used to run and verify SQL queries.

## gsec Security Administrator
You first need to run gsec as SYSDBA to access, modify, add or delete the user informations. To invoke it, execute the following command in your terminal:
> gsec -user SYSDBA -password masterkey
To view the current user type **display** command in the GSEC prompt
![Step 1](https://github.com/krishna1401/FireBird3.0.4/blob/master/Getting%20Started/A1.png)
> It's better to change the password for SYSDBA as its the global password. To change it, we modify SYSDBA account using the following command:
> modify SYSDBA -pass newpass
![Step 2](https://github.com/krishna1401/FireBird3.0.4/blob/master/Getting%20Started/A2.png)
**Note**: First 8 characters of the password are validated as password i.e. password123 = password234 (as first 8 character *password* is same in both the case)

## isql Interactive SQL Processor
Isql is analogous to *psql* for *PostgreSQL* and *SQL\*Plus* for *Oracle*. You can type normal SQL commands and get query results from the database.

Firebird comes with an example **EMPLOYEE** database, and we will use this database to test our SQL commands. To begin, execute the following command:
> isql D:\Firebird_3_0\examples\empbuild\EMPLOYEE.FDB
This will open an isql prompt with EMPLOYEE database. We will try few more simple SQL queries to try the SQL command prompt.
> SELECT emp_no, full_name, job_code, job_country FROM employee;
![Step 3](https://github.com/krishna1401/FireBird3.0.4/blob/master/Getting%20Started/A3.png)
> show tables;
![Step 4](https://github.com/krishna1401/FireBird3.0.4/blob/master/Getting%20Started/A4.png)

*Note*: To exit the sql prompt, simply type **quit;** and press **ENTER**