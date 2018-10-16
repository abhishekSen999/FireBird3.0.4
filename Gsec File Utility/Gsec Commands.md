Here, we will discuss the various commands in gsec prompt. These are: <br />

> -add <name> [ <parameter> ... ]

<br > This command is used to add new user to the gsec security database. You can optionally add more parameters like first, middle and last names (also the password for the new user)
<br >![Step 1]()

> -delete <name>

<br > This command removes the named user from the database. All details of the users are removed from the security database and cannot be undone unless added as new user.
<br >![Step 2]()

> -modify <name> <parameter> [ <parameter> ... ]

<br > The *<name>* option specifies how the user be known while connecting to FireBird database.


## Parameters

1. **-pw <password>**: This parameter is used to specify the new password for the user. If the password is omitted, the current user will be unable to login to any FireBird databases at all. 
<br >![Step 3]()
<br >![Step 4]()

2. **-fname [ <first name> ]**: This parameter allows you to store the first name of the user in the database. You can delete the first name by not supplying a name.

3. **-mname [ <middle name> ]**: This parameter allows you to store the middle name of the user in the database. You can delete the first name by not supplying a name.

4. **-lname [ <last name> ]**: This parameter allows you to store the last name of the user in the database. You can delete the first name by not supplying a name.

5. **-admin yes | no**: This parameter alloes to specify whether or not the user show be granted **RDB$ADMIN** role i.e. it acts as a SYSDBA user with all permission similar as SYSDBA.

![Step 5]()