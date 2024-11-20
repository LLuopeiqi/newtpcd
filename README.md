# Bug Detection Database
## About newtpcd.sql
+ The newtpcd.sql file is the database initialization script used for bug detection in this project.
+ It contains the necessary table structures and sample data to replicate issues and verify fixes during development and testing.
## How to Use newtpcd.sql
1、Ensure you have MySQL installed on your system.

2、Import the newtpcd.sql file into your MySQL database:

```mysql -u [username] -p [database_name] < newtpcd.sql```

+ Replace [username] with your MySQL username.
+ Replace [database_name] with the name of the database you want to import into.
3、Once imported, the database will include all the necessary tables and data for bug detection.
