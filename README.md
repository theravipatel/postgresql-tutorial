## 1) Introduction of PostgreSQL
- PostgreSQL is an ORDBMS [`Open-Source Object-Relational Database Management System`]. It is used to store data securely; supporting best practices, and allow recovering them when the request is processed.
- PostgreSQL is initially introduced on 8th July 1996 at the University of California.
- It is the first DBMS, which perform MVCC [Multi-Version Concurrency Control] feature.
- It is written in C programming language.
- PostgreSQL is cross-platform and runs on various operating systems such as Microsoft Windows, UNIX, FreeBSD, Mac OS X, Solaris, HP-UX, LINUX, and so on.
- PostgreSQL is also pronounced as Post-gress-Q-L, which is developed by the PostgreSQL Global Development Group (a worldwide team of volunteers), any organization or other private entity does not control it.
- PostgreSQL will offer us the facility to add custom functions with the help of various programming languages such as Java, C, and C++, etc. In this, we can describe our functional languages, index types and data types, and we can also create a custom plugin to increase the reliability of our needs.
- The PostgreSQL follow the transaction along with the ACID (Atomicity, Consistency, Isolation, and Durability) properties.

## 2) Feature of PostgreSQL
- Free to download
- Compatible on several `Operation Systems`
- Compatible with various `Programming Languages`
- It supports `Data Integrity` which includes the following:
    - Primary Keys
    - UNIQUE, NOT NULL
    - Foreign Keys
    - Explicit Locks, Advisory Locks
    - Exclusion Constraints
- It supports various `Features of SQL` which include the followings:
    - MVCC (Multi-Version Concurrency Control).
    - Multiple Indexing such as Multicolumn, Partial, B-tree, and expressions.
    - SQL sub-selects.
    - Complex SQL queries.
    - Streaming Replication
    - Transactions, Nested Transactions through Savepoints.
    - Just-in-time compilation of expressions
    - Table partitioning
- It support various `Data Types` such as:
    - Structured: Array, Date and Time, UUID (Universally Unique Identifier), Range.
    - Primitives: String, Integer, Boolean, Numeric.
    - Customizations: Custom Types, Composite.
    - Geometry: Polygon, Circle, Line, Point,
    - Document: XML, JSON/JSONB, Key-value.
- It is `Highly Extensible` in several phases which are as following:
    - It supports procedural Languages such as Perl, PL/PGSQL, and Python, etc.
    - JSON/SQL path expressions
    - Stored procedures and functions.
    - For tables, it supports a customizable storage interface.
    - It is compatible with foreign data wrappers, which connect to further databases with a standard SQL interface.
- It is safe because it follows several `Security` aspects, which are as follows:
    - PostgreSQL provides a robust access control system.
    - It includes several Authentications such as Lightweight Directory Access Protocol(LDAP), Generic Security Service Application Program Interface (GSSAPI), SCRAM-SHA-256, Security Support Provider Interface (SSPI), Certificate, and so on.
    - PostgreSQL supports Column and row-level security.
- It is `Highly Reliable` and also provide disaster recovery such as:
    - Active standbys, PITR (Point in time recovery)
    - It supports WAL (Write-ahead Logging)
    - Tablespaces
    - It supports different types of Replication like Synchronous, Asynchronous, and Logical.
- It supports `Internationalization`, which means that the international character sets include ICU collations, accent-insensitive and case-sensitive collations, and full-text searches.
- In PostgreSQL, a table can be set to `inherit` their characteristics from a "parent" table.
- It is compatible with `ANSI-SQL2008`.
- PostgreSQL will help us to improve the functionality of `Server-Side programming`.
- We can install several `extensions` to add additional functionality to PostgreSQL.

## 3) Advantages and Disadvantages of PostgreSQL
- Advantages:
    - PostgreSQL is easy to use; that why we do not require much training.
    - It requires low maintenance management for enterprise as well as embedded usage.
    - PostgreSQL manages data in a relational database as it is very powerful and robust.
    - We can quickly get the source code of PostgreSQL as it is freely available in an open-source license, and we can immediately implement, change according to our requirements.
    - It can execute dynamic web-application and website as the LAMP stack option.
    - PostgreSQL is a highly risk-tolerant database.

- Disadvantages:
    - PostgreSQL does not support the various open-source applications as compared to MySQL.
    - In this, creating replication is a bit complex.
    - It is not maintained by one company.
    - PostgreSQL speed performance is not as good as compare to further tools.
    - It is a bit slow as compared to MySQL.
    - Sometimes, the installation process is not easy for the learner.

## 4) Download and Install PostgreSQL
- To download PostgreSQL, Go to the Official website (https://www.postgresql.org/) of PostgreSQL and download setup as per OS.
- Note that during installation, it will ask for password to set which will required everytime when accessing database.

## 5) Connect to a PostgreSQL Database Server
- We can connect the PostgreSQL database server using:
    - `pgAdmin 4`: It is an in-built Graphical User Interface (GUI)
    - `SQL Shell (PSQL)`: It is a terminal-based front-end application.
- Default configuration will be:
    - `Host Server`: localhost
    - `Database`: postgres
    - `Port`: 5432
    - `Username`: postgres
    - `Password`: [which created during installation]
- Note that while writing a command in `SQL Shell (PSQL)`, we should make sure that the specified command would end with a `Semicolon (;)`.

## 6) SQL Shell (PSQL) commands list
- `Connect to a database` - Same host database:
```
psql -d <db-name> -U <username> -W

// -W - forces psql to ask for the user password before connecting to the database
``` 
- `Connect to a database` - Different host database:
```
psql -h <db-address> -d <db-name> -U <username> -W
```
- `Connect to a database` - Different host database with SSL mode:
```
psql "sslmode=require host=<db-address> dbname=<db-name> user=<username>"
```
- `List all databases`: Return with all databases and their name, owner, encoding, access privileges, and other information
```
\l
```
- `Switch to another database`:
```
\c <db-name>
```
- `List database tables`: Return with table's schema, name, type, owner 
```
\dt
```
- `Describe a table`: 
```
\d <table-name>

// Returns all the columns, their types, collection, whether they are nullable or not, and their configured default value.
```
```
\d+ <table-name>

// Returns extra information such as storage, compression, stats target, and a description.
```
- `List all schemas`: Returns the name of the schemas and their owners.
```
\dn
```
- `List users and their roles`:
```
\du
```
- `Retrieve a specific user`:
```
\du <username>
```
- `List all functions`: Rreturns all functions and schema they belong to, names, result data type, argument data types, type
```
\df
```
- `List all views`:
```
\dv
```
- `Execute the last command again`:
```
\g
```
- `Display command history`:
```
\s
```
- `Save the command history to a file`:
```
\s <file-name>
```
- `Save query results to a file`:
```
\o <file-name>

// To stop saving results to the file, you need to run the [\o] command again without the file name.
```
- `Run commands from a file`: 
    - Create a txt file with the following content:
    ```
    \l
    \dt
    \du
    ```
    - Now run following command to run above command from file:
    ```
    \i <file-name>
    ```
- `Know all available psql commands`:
```
\?
```
- `Get help`:
```
\h
```
- `Edit command in your own editor`:
```
\e
```
- `Switch from aligned to non-aligned column output`:
```
\a
```
- `Switch the output to HTML format`:
```
\H
```
- `Quit psql`:
```
\q
```

## 7) Create Database using pgAdmin 4
- Open pgAdmin 4 -> Servers -> PostgreSQL 15 -> Databases -> right click on it and enter DB info in create database window.
- Syntax to create a database:
```
CREATE DATABASE database_name
    WITH
        [OWNER =  role_name]
        [TEMPLATE = template]
        [ENCODING = encoding]
        [LC_COLLATE = collate]
        [LC_CTYPE = ctype]
        [TABLESPACE = tablespace_name]
        [ALLOW_CONNECTIONS = true | false]
        [CONNECTION LIMIT = max_concurrent_connection]
        [IS_TEMPLATE = true | false ]
```
- Parameters:
    - `OWNER`: Assign a role that will be the owner of the database. If you omit the OWNER option, the owner of the database is the role that you use to execute the CREATE DATABASE statement.
    - `TEMPLATE`: Specify the template database from which the new database is created. By default, PostgreSQL uses the template1 database as the template database if you don’t explicitly specify the template database.
    - `ENCODING`: Determine the character set encoding in the new database.
    - `LC_COLLATE`: Specify the collation order (LC_COLLATE) that the new database will use. This parameter affects the sort order of string in the queries that contain the ORDER BY clause. It defaults to the LC_COLLATE of the template database.
    - `LC_CTYPE`: Specify the character classification that the new database will use. It affects the classification of character e.g., lower, upper, and digit. It defaults to the LC_CTYPE of the template database
    - `TABLESPACE`: Specify the tablespace name for the new database. The default is the tablespace of the template database.
    - `CONNECTION LIMIT`: Specify the maximum concurrent connections to the new database. The default is -1 i.e., unlimited. This parameter is useful in the shared hosting environments where you can configure the maximum concurrent connections for a particular database.
    - `ALLOW_CONNECTIONS`: The allow_connections parameter is a boolean value. If it is false, you cannot connect to the database.
    - `TABLESPACE`: Specify the tablespace that the new database will use. It defaults to the tablespace of the template database.
    - `IS_TEMPLATE`: If the IS_TEMPLATE is true, any user with the CREATEDB privilege can clone it. If false, only superusers or the database owner can clone it.

- Example:
```
CREATE DATABASE blog
    WITH
    OWNER = postgres
    ENCODING = 'UTF8'
    LC_COLLATE = 'English_United States.1252'
    LC_CTYPE = 'English_United States.1252'
    TABLESPACE = pg_default
    CONNECTION LIMIT = -1
    IS_TEMPLATE = False;

COMMENT ON DATABASE blog
    IS 'Test comment';
```

## 8) Create Database Command Line (SQL Shell)
- Open the SQL shell and Connect with server by using default configuration (To use default config, just enter without writing anything except for password)
- Now run following command to create database with default configuration:
```
CREATE DATABASE blog;
```

## 9) Delete/Drop Database
- Using pgAdmin 4, right click on database and click on `Delete/Drop Database`
- Using SQL Shell, run below command:
```
DROP DATABASE [ IF EXISTS] database_name;
```
- Note that using SQL Shell, we need to first select different/default database to delete/drop our database.

## 10) Alter Database
- Changing attributes of a database
```
ALTER DATABASE database_name [ [WITH] option ]

//where option can be:
    ALLOW_CONNECTIONS allowconn
    CONNECTION LIMIT connlimit
    IS_TEMPLATE istemplate
```
- Rename the database
```
ALTER DATABASE database_name
RENAME TO new_name;
```
- Change the owner of the database
```
ALTER DATABASE database_name
OWNER TO new_owner | current_user | session_user;
```

## 11) Data Types
- `Boolean`: **boolean** or **bool**. Three possible values: true, false or null
- `Character`: **CHAR(n)**, **VARCHAR(n)**, and **TEXT**
- `Numeric`: **SMALLINT**, **INT**, **SERIAL**, **float(n)**, **real** or **float8**, **numeric(p,s)** 
- `Temporal`: **DATE**, **TIME**, **TIMESTAMP**, **TIMESTAMPTZ**, **INTERVAL**
- `UUID (Universally Unique Identifiers)`: **UUID**
- `Array`: Every data type has its own companion array type e.g. **INT[]**, **CHAR[]**, **TEXT[]** etc... 
- `JSON`: **JSON**, **JSONB**
- `hstore`:
    - It used to store key-value pairs in a single value
    - To use **hstore** data type, We need to enable the hstore extension
- `Special Type`:
    - **box** a rectangular box.
    - **line** – a set of points.
    - **point** a geometric pair of numbers.
    - **lseg** a line segment.
    - **polygon** a closed geometric.
    - **inet** an IP4 address.
    - **macaddr** a MAC address.

## 12) Create Table
- Using pgAdmin 4 -> Select our Database -> Schemas -> Public -> right click and click on create table
- Using SQL Shell as follow:
- Syntax:
```
CREATE TABLE [IF NOT EXISTS] table_name (
   column1 datatype(length) column_contraint,
   column2 datatype(length) column_contraint,
   column3 datatype(length) column_contraint,
   table_constraints
);
```
- Constraints: NOT NULL, UNIQUE, PRIMARY KEY, CHECK, FOREIGN KEY
- Example:
```
CREATE TABLE accounts (
	user_id serial PRIMARY KEY,
	username VARCHAR ( 50 ) UNIQUE NOT NULL,
	password VARCHAR ( 50 ) NOT NULL,
	email VARCHAR ( 255 ) UNIQUE NOT NULL,
	created_on TIMESTAMP NOT NULL,
    last_login TIMESTAMP 
);

CREATE TABLE account_roles (
  user_id INT NOT NULL,
  grant_date TIMESTAMP,
  PRIMARY KEY (user_id),
  FOREIGN KEY (user_id)
      REFERENCES accounts (user_id)
);
```

## 13) Drop/Delete Table
- Syntax:
```
DROP TABLE table_name;
```

## 14) Show table - To get the table information of a database
- Syntax:
```
SELECT 
    * 
FROM 
    pg_catalog.pg_tables  
WHERE
    schemaname != 'pg_catalog'  
    AND schemaname != 'information_schema';  
```

## 15) Describe Table - To find the information on columns of a table
- Syntax:
```
SELECT 
    * 
FROM 
    information_schema.COLUMNS  
WHERE 
    TABLE_NAME = 'table_name';
```

## 16) Alter table - To change the current table structure
- To add a new column to a table:	
```
ALTER TABLE table_name ADD COLUMN new_column_name TYPE;
```

- To delete an existing column:
```
ALTER TABLE table_name DROP COLUMN column_name;
```

- To modify the column's default value:	
```
ALTER TABLE table_name ALTER COLUMN column_name [SET DEFAULT value | DROP DEFAULT];
```

- To add a constraint.	
```
ALTER TABLE table_name ADD CONSTRAINT constraint_name constraint_definition;
```

- To rename column:	
```
ALTER TABLE table_name RENAME COLUMN column_name TO new_column_name;
```

- To rename a table:
```
ALTER TABLE table_name RENAME TO new_table_name;
```

- To add the CHECK constraint:	
```
ALTER TABLE table_name ADD CHECK expression;
```

- To change the NOT NULL constraint:	
```
ALTER TABLE table_name ALTER COLUMN column_name [SET NOT NULL| DROP NOT NULL];
```

## 16) Truncate Table - To delete all records from huge tables quickly
- Syntax:
```
TRUNCATE TABLE table_name [ RESTART IDENTITY | CONTINUE IDENTITY ] [ CASCADE | RESTRICT ] 
```
- Options:
    - `CASCADE`: This option automatically truncates all tables, which contains the foreign-key references to other tables, or any tables added to the collection due to CASCADE.
    - `RESTART IDENTITY`: It repeatedly restarts orders owned by columns of the truncated tables.
    - `CONTINUE IDENTITY`: It does not change the values of orders, and it is the default option.
    - `RESTRICT`: It is also a default option, which can decline to truncate if other tables contain the foreign-key references of tables, which are not mentioned in the command.


## 17) Create Temporary Table
- It presents at the time of a database session and automatically drops at the end of an operation or a session.
- Syntax:
```
CREATE TEMPORARY/TEMP TABLE temp_table_name(column_details); 
```

## 18) Column Alias - To give a temporary name to the column in the particular query operation.
- Syntax:
```
SELECT column_name AS alias_name FROM table_name; 
SELECT column_name alias_name FROM table_name;
SELECT expression AS alias_name FROM table_name;  
```

## 19) Sequence
- It is a generator used to create a progressive number that can help to produce a single primary key automatically and synchronize the keys across various rows or tables.
- We can use `currval()`, `setval()`, and `nextval()` functions to operate on the sequence once the sequence has been generated.
- `Create Sequence`:
```
CREATE SEQUENCE [ IF NOT EXISTS ] sequence_name
    [ AS { SMALLINT | INT | BIGINT } ]
    [ INCREMENT [ BY ] increment ]
    [ MINVALUE minvalue | NO MINVALUE ] 
    [ MAXVALUE maxvalue | NO MAXVALUE ]
    [ START [ WITH ] start ] 
    [ CACHE cache ] 
    [ [ NO ] CYCLE ]
    [ OWNED BY { table_name.column_name | NONE } ]
```
- Example:
- Creating a sequence associated with a table column:
```
CREATE SEQUENCE order_item_id
    START 5
    INCREMENT 5
    OWNED BY order_details.item_id;
```
- Insert data into `order_details` table:
```
INSERT INTO 
    order_details(order_id, item_id, item_text, price)
VALUES
    (100, nextval('order_item_id'), 'DVD Player', 100),
    (100, nextval('order_item_id'), 'Android TV', 550),
    (100, nextval('order_item_id'), 'Speaker', 250);
```

- `List all sequences in a database`:
```
SELECT
    relname sequence_name
FROM 
    pg_class 
WHERE 
    relkind = 'S';
```

- `Delete sequence`:
```
DROP SEQUENCE [ IF EXISTS ] sequence_name [, ...] 
[ CASCADE | RESTRICT ];
```

## 20) Upsert – insert or update data if the new row already exists in the table
- Syntax:
```
INSERT INTO table_name (column_list) 
    VALUES (value_list)
    ON CONFLICT target action;
```
- In this statement, the `target` can be one of the following:
    - `(column_name)` – a column name.
    - `ON CONSTRAINT constraint_name` – where the constraint name could be the name of the UNIQUE constraint.
    - `WHERE predicate` – a WHERE clause with a predicate.
- In this statement, the `action` can be one of the following:
    - `DO NOTHING` – means do nothing if the row already exists in the table.
    - `DO UPDATE SET column_1 = value_1, .. [WHERE condition]` – update some fields in the table.
- Example:
```
INSERT INTO customers (name, email)
    VALUES ('Microsoft','hotline@microsoft.com') 
    ON CONFLICT ON CONSTRAINT customers_name_key 
    DO NOTHING;

OR

INSERT INTO customers (name, email)
    VALUES ('Microsoft','hotline@microsoft.com') 
    ON CONFLICT (name) 
    DO NOTHING;

OR

INSERT INTO customers (name, email)
    VALUES ('Microsoft','hotline@microsoft.com') 
    ON CONFLICT (name) 
    DO UPDATE SET email = EXCLUDED.email || ';' || customers.email;
```

## 21) Schema - Create/Alter/Drop Schemas, Set Privileges
- Schema is a namespace that contains named database objects such as:
    - Views
    - Indexes
    - Sequences
    - Datatypes
    - Operators
    - Functions
    - Tables
    - Stored Procedures
    - Other relations
- Schemas allow us to organize database objects e.g., tables into logical groups to make them more manageable.
- Schemas enable multiple users to use one database without interfering with each other.
- A database can have one or more schemas, whereas each schema exists for only one database, and two schemas can contain different objects, which share a similar name.
- PostgreSQL automatically creates a schema called `public` for every new database. Whatever object you create without specifying the schema name, PostgreSQL will place it into this public schema.
- So if we create tables without describing any schema names then those tables are automatically placed into the `public schema` by default.
- Schema operations:
    - `CREATE SCHEMA`: To create a new schema
    ```
    CREATE SCHEMA schema_name;
    ```
    - `ALTER SCHEMA`: To rename a schema or change its owner
    ```
    ALTER SCHEMA schema_name RENAME TO new_name;
    ALTER SCHEMA schema_name OWNER TO { new_owner | CURRENT_USER | SESSION_USER};
    ```
    - `DROP SCHEMA`: To drop/delete a schema
    ```
    DROP SCHEMA [IF EXISTS] schema_name1 [,schema_name2,...] [CASCADE | RESTRICT];
    ```
- Example:
```
// Create Schema
CREATE SCHEMA sales;

// Create Table without specifying schema
CREATE TABLE staff(
    staff_id SERIAL PRIMARY KEY,
    first_name VARCHAR(45) NOT NULL,
    last_name VARCHAR(45) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE
);

// Create Table with schema
CREATE TABLE sales.staff(
    staff_id SERIAL PRIMARY KEY,
    first_name VARCHAR(45) NOT NULL,
    last_name VARCHAR(45) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE
);
```

- To add the new schema to the search path, you use the following command:
```
SET search_path TO your_schema_name, public;

// After this command, new table creation without specifying schema will be 
// in the 'your_schema_name' instead of 'public' 
```

- Schemas and Privileges: 
    - Users can only access objects in the schemas that they own. It means they cannot access any objects in the schemas that do not belong to them.
    - To allow users to **access/create** the objects in the schema that they do not own, user need to have grant privileges of the schema as follow:
        - `USAGE`: To access of the objects in the schema
        ```
        GRANT USAGE ON SCHEMA schema_name TO user_name;
        ```
        - `CREATE`: To create an object in the schema
        ```
        GRANT CREATE ON SCHEMA schema_name TO user_name; 
        ```
    - We can revoke that privilege if we do not want to access
    ```
    REVOKE CREATE ON SCHEMA schema_name FROM user_name;
    ```

## 22) Fetch Clause
- It is used to retrieve a portion of rows returned by a query.
- It is similar to `LIMIT` clause but the difference is that `LIMIT` is not following a SQL-standard.
- Syntax:
```
OFFSET start { ROW | ROWS }
FETCH { FIRST | NEXT } [ row_count ] { ROW | ROWS } ONLY
```
- `ROW is the synonym for `ROWS`, `FIRST` is the synonym for `NEXT`. So we can use them interchangeably.
- `start` is an integer that must be zero or positive. By default, it is zero if the `OFFSET clause` is not specified.
- `row_count` is 1 or greater. By default, the default value of row_count is 1.
- Example:
```
SELECT
    *
FROM
    category
ORDER BY
    name
OFFSET 5 ROWS 
FETCH FIRST 5 ROW ONLY; 
```

## 23) Exists Condition
- It is used to evaluate the existing rows in a `subquery` and returns `true` if the subquery returns several records.
- It is used with `WHERE clause`.
- It can combine with the `SELECT`, `INSERT`, `UPDATE`, and `DELETE` queries.
- Syntax:
```
WHERE [NOT] EXISTS (subquery); 
```
- Example:
```
SELECT 
    first_name,
    last_name
FROM 
    customer c
WHERE EXISTS
    (
        SELECT 
            1
        FROM 
            payment p
        WHERE 
            p.customer_id = c.customer_id AND amount > 11
    )
ORDER BY 
    first_name,
    last_name;
```
- **Note**: Usually, the SELECT command begins with SELECT * rather than a column name or list of expressions. Here, we are using the SELECT 1in its place of SELECT *, which helps us to enhance the query's performance in PostgreSQL.