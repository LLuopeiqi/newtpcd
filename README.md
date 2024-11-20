# ..
# Bug Detection Database
## About tpcd.sql
+ The newtpcd.sql file is the database initialization script used for bug detection in this project.
+ It contains the necessary table structures and sample data to replicate issues and verify fixes during development and testing.
## How to Use newtpcd.sql
This document provides guidance on using the `tpcd.sql` database file in various database management systems.

---

### 1. MySQL

#### Steps

1. **Create a database:**

   ```sql
   create database tpcd;
   ```

2. **Import data:**
   Run the following command in the terminal:

   ```bash
   mysql -u root -p tpcd < tpcd_back.sql
   ```

---

### 2. TiDB

#### Steps

1. **Access the database:**
   Run the following command in the terminal:

   ```bash
   mysql --comments --host 127.0.0.1 --port 4000 -u root -p
   ```

2. **Set username and password:**
   After connecting, execute the following command (replace `your_password` with your desired password):

   ```sql
   SET PASSWORD FOR 'root'@'%' = 'your_password';
   ```

3. **Create a database:**

   ```sql
   create database tpcd;
   ```

4. **Import data:**
   Run the following command in the terminal:

   ```bash
   mysql -h 127.0.0.1 -P 4000 -u root -p tpcd < tpcd.sql
   ```

---

### 3. MariaDB

#### Steps

1. **After starting the database, create a database:**

   ```sql
   create database tpcd;
   ```

2. **Import data:**
   Run the following command in the terminal:

   ```bash
   mariadb -u root -p tpcd < tpcd.sql
   ```

---

### 4. OceanBase

#### Steps

1. **After the initial login, create a database:**
   Log in to the OceanBase client and execute the following command:

   ```sql
   create database tpcd;
   ```

2. **Import data:**
   Use the `source` command to import the data (replace `your_path` with the actual path to the file):

   ```sql
   source your_path/tpcd.sql;
   ```

---

### Notes

- Ensure you have sufficient permissions to perform the import.
- Verify that the `tpcd.sql` file path is correct.


