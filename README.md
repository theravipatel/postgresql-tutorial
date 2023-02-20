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