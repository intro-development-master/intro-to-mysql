# Intro to MySQL

MySQL is an open-source relational database management system (RDBMS). MySQL is a central component of the (Linux, Apache, MySQL, Pertl/PHP/Python) LAMP open-source web application stack (and other AMP stacks).

Many popular website use MySQL.  They include:

* Google
* Facebook
* Twitter
* Flickr
* YouTube

## User Interfaces

* [MySQL Workbench](https://www.mysql.com/products/workbench/) - The Official Integrated Environment for MySQL
* [Adminer](https://www.adminer.org/) - Formally phpMinAdmin
* [phpMyAdmin](https://www.phpmyadmin.net/) - Usually packaged with LAMP

## Command-line Interfaces

CLIs are usually packaged with `mysql`.  It is the main interace for MySQL

## Tutorial

### Creating a Database

To create a database, use the command `mysql -u root -p` -> `create database TUTORIALS;`.  A password prompt will then be displayed.

The above command will create a database named `TUTORIALS`.

### Dropping a Database

To drop a database, use the command `mysql -u root -p` -> `drop database TUTORIALS;`.  A password prompt will then be displayed.

The above command will drop a database named `TUTORIALS`.  A confirmation message will be displayed.  Once confirmed, the database will be dropped.

### Selecting a Database

To select a database, use the command `use TUTORIALS`.  You must be logged in to select a database.

All subsequent commands will be performed on `TUTORIALS`.

**NOTE:** All database names, table names, table field names are case sensitive.

### Data Types

For a comprehensive list, please refer to the [documentation](https://www.tutorialspoint.com/mysql/mysql-data-types.htm).

### Creating Tables

SQL syntax to create a MySQL table: `CREATE TABLE table_name (column_name column_type);`

In the `TUTORIALS` table, it would look as followed:

```sql
CREATE TABLE tutorials_tbl(
    tutorial_id INT NOT NULL AUTO_INCREMENT,
    tutorial_title VARCHAR(100) NOT NULL,
    tutorial_author VARCHAR(40) NOT NULL,
    submission_date DATE,
    PRIMARY KEY ( tutorial_id )
);
```

### Dropping Tables

SQL syntax to drop a MySQL table: `DROP TABLE table_name;`

In the `TUTORIALS` table, it would look as followed: `DROP TABLE tutorials_tbl`

### Inserting Data

SQL syntax to create a MySQL table: `INSERT INTO table_name (field1, field2, field3) VALUES (value1, value2, value3);`

In the `TUTORIALS` table, it would look as followed:

```sql
INSERT INTO tutorials_tbl(
    tutorial_title,
    tutorial_author,
    submission_date
) VALUES ("Learn Java", "John Doe", NOW());
```

**NOTE:** `tutorial_id` isn't included since we set the table to `AUTO_INCREMENT`.

### Selecting Data

SQL syntax to drop a MySQL table: 

```sql
SELECT field1, field2, field3
FROM table_name1, table_name1,
[WHERE Clause]
[LIMIT N][OFFSET M];
```

In the `TUTORIALS` table, it would look as followed: 

```sql
SELECT tutorial_title, tutorial_author, submission_date
FROM tutorials_tbl,
```

**NOTE:** You can use the `*` wildcard to select all columns.