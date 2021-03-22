# Go CRUD
---
## Database set up
This project is using MySql as the persistent layer for storing employee info. The following user, database and table need to
exist before running the backend service:
- Create user `gocrud`
    ```mysql
    CREATE USER gocrud@'localhost' IDENTIFIED BY 'password';
    ```
    - Grant privilage:
        ```mysql
        GRANT ALL PRIVILEGES ON *. * TO gocrud@'localhost';
        ```
- Create database `gocrud_db`
    ```mysql
    CREATE DATABASE gocrud_db;
    ```
- Create `employee` table
    ```mysql
    CREATE TABLE `employee` (`id` int(6) unsigned NOT NULL AUTO_INCREMENT,`name` varchar(30) NOT NULL,`city` varchar(30) NOT NULL,PRIMARY KEY (`id`)) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=latin1;
    ```

## Start service
```sh
go build main.go
go run main.go
```