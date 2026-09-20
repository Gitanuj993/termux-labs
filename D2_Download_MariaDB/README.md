
# About MariaDB
MariaDB is a MySQL-compatible relational database


## Install MariaDB

### Open Termux and run

```txt
pkg update && pkg upgrade
pkg install mariadb
```
 ### Initialize the database

```bash
mariadb-install-db                                    ```
```

## Start the database server

### Use A.
```bash
mysqld_safe &
```
### Use Option B.

```bash
mariadb_safe &
```

Verify Server

```bash
ps aux | grep mysqld
```


> ``&``is used to run it in background


## Open the MySQL-compatible shell

```bash
mariadb -u root
```


Example : You can see Something like

```txt
MariaDB [(none)]>
```

> [!note]
>  Now you can practice SQL.


## Create a dedicated User

```bash
CREATE USER 'anuj'@'localhost' IDENTIFIED BY 'your_pa>
```

### Grant permissions:
                                                      ```bash
GRANT ALL PRIVILEGES ON *.* TO 'anuj'@'localhost';
```

### Apply changes:

```bash
FLUSH PRIVILEGES;
```

### Exit the SQL Shell

```sql
exit ;
```


## Log in as your new user

```bash
mariadb -u anuj -p
```

Enter the password you created.

and use the MariaDB


## Maria DB Hack/Tips

### Clear the Screen                                  Ctrl + L



# If your Device as low storage & Low RAM

Shutdown the server after use

```bash
pkill mariadbd
```


And Whenever you want to use
start the server

```bash
mysqld_safe &
```

Login / Enter

```bash
mariadb -u anuj -p
```

Enter Your Password and Start Practice.


# Thank you
