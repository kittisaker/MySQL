# MySQL : Chapter 1 Using AND, OR, NOT, IN, BETWEEN and LIKE logical operaters

https://www.coursera.org/learn/database-structures-and-management-with-mysql/home/week/1

## Set Enviroment
Use XAMPP, and open shell

```shell
mysql -u root
show databases;
```

### Step 1: Create Database
```shell
CREATE DATABASE TestDB;
```

### Step 2: Select Database
```shell
USE TestDB;
```

### Step 3: Create Table
```shell
CREATE TABLE TestTable (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    city VARCHAR(50)
);
```

### Step 4: Insert Data
```shell
INSERT INTO TestTable (name, age, city) VALUES 
('Alice', 30, 'New York'),
('Bob', 25, 'Los Angeles'),
('Charlie', 35, 'Chicago'),
('David', 28, 'Miami'),
('Eve', 32, 'New York');
```

## AND
```shell
SELECT * FROM TestTable WHERE age > 25 AND city = 'New York';
```

## OR
```shell
SELECT * FROM TestTable WHERE city = 'Chicago' OR city = 'Miami';
```

## NOT
```shell
SELECT * FROM TestTable WHERE NOT city = 'Los Angeles';
```

## IN
```shell
SELECT * FROM TestTable WHERE name IN ('Alice', 'Bob', 'Eve');
```

## BETWEEN
```shell
SELECT * FROM TestTable WHERE age BETWEEN 25 AND 30;
```

## LIKE
```shell
SELECT * FROM TestTable WHERE name LIKE 'D%';
```

---