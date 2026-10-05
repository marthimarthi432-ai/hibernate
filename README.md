# Student Hibernate (Maven + MySQL)

Hibernate 5.6 app that maps a `Student` entity (id, name, email, course) to a MySQL
table `student`, inserts a record, verifies it, updates it, and verifies the update.

## Requirements
- JDK 11+
- Maven 3.6+
- Network access to db01.dbhost.dev:5051

## Run
    mvn clean compile exec:java

The table is created automatically (`hibernate.hbm2ddl.auto=update`).
DB settings are in `src/main/resources/hibernate.cfg.xml`.

## Verify manually in MySQL
    mysql -h db01.dbhost.dev -P 5051 -u user_455a3k5ad -p db_455a3k5ad
    SELECT * FROM student;
