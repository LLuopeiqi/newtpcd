# Bug Detection Database
## About tpcd.sql
+ The newtpcd.sql file is the database initialization script used for bug detection in this project.
+ It contains the necessary table structures and sample data to replicate issues and verify fixes during development and testing.
## How to Use newtpcd.sql
1、Ensure you have MySQL installed on your system.

2、Import the newtpcd.sql file into your MySQL database:
  ```mysql -u [username] -p [database_name] < newtpcd.sql```

+ Replace [username] with your MySQL username.
+ Replace [database_name] with the name of the database you want to import into.
3、Once imported, the database will include all the necessary tables and data for bug detection.

## About `schema.sql`
The `schema.sql` file is an exported schema of the `newtpcd.sql` database.  
It contains the structure of all tables, including their definitions such as column names, data types, constraints, and relationships.

### Purpose
- This file is useful for understanding the database structure without needing to inspect the full database (`newtpcd.sql`) with data.
- It can also be used to create a fresh instance of the database schema when no data is required.

### How to Use `schema.sql`
1. Ensure you have MySQL installed on your system.
2. Import the `schema.sql` file into your database:
   ```bash
   mysql -u [username] -p [database_name] < schema.sql

+ Replace [username] with your MySQL username.
+ Replace [database_name] with the name of the database where you want to apply the schema.
+ This will create the database tables and relationships without inserting any data.
### Important Notes
+ schema.sql is generated from newtpcd.sql and reflects its table structure.
+ For a fully functional database with data, use newtpcd.sql instead.
# 如何使用tpcd.sql
## MySQL
首先创建对应数据库: `create database tpcd;`
随后在命令行 进行导入 : mysql -u root -p tpcd < tpcd_back.sql
## TiDB
进入数据库 : mysql --comments --host 127.0.0.1 --port 4000 -u root -p
启动后,先设置新的用户名密码 : SET PASSWORD FOR 'root'@'%' = 'your_password';
创建数据库 : create database tpcd;
导入数据 mysql -h 127.0.0.1 -P 4000 -u root -p tpcd < tpcd.sql
## MariaDB
启动数据库以后:
首先创建对应数据库: `create database tpcd;`
随后在命令行 进行导入: mariadb -u root -p tpcd < tpcd.sql 
## OceanBase
首次登录以后,创建数据库
随后导入数据 : source your_path/tpcd.sql
