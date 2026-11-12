SQL (Structured Query Language) is the standard programming language used to manage and manipulate data in relational databases. 

GeeksforGeeks
 +1
SQL commands are divided into different categories based on what they do. Below are code examples for the most common SQL tasks, assuming a database containing a table named customers. 

Indeed
 +2
1. Reading Data (Data Query Language - DQL)
These commands are used to look up and pull information out of a database table. 

Indeed
 +1
Select everything: Retrieve all rows and all columns from a table.
sql
SELECT * FROM customers;
Usa el código con precaución.
Filter results: Retrieve only specific columns for customers living in a specific city.
sql
SELECT first_name, last_name 
FROM customers 
WHERE city = 'New York';
Usa el código con precaución.
Sort results: Retrieve customers and sort them alphabetically by their last name. 

LearnSQL.com
 +1
sql
SELECT * FROM customers 
ORDER BY last_name ASC;
Usa el código con precaución.
2. Modifying Data (Data Manipulation Language - DML)
These commands are used to add, edit, or delete the actual rows of data inside your tables. 

Indeed
Insert data: Add a brand new customer to the table.
sql
INSERT INTO customers (first_name, last_name, city) 
VALUES ('Alice', 'Smith', 'Chicago');
Usa el código con precaución.
Update data: Change existing information (e.g., updating a customer's city).
sql
UPDATE customers 
SET city = 'Los Angeles' 
WHERE customer_id = 4;
Usa el código con precaución.
Delete data: Remove a specific record from the database. 

YouTube
·Data Geek is my name
 +3
sql
DELETE FROM customers 
WHERE customer_id = 4;
Usa el código con precaución.
3. Creating & Designing Tables (Data Definition Language - DDL)
These commands build, alter, or destroy the actual structure of the database (like creating tables and columns) rather than the data itself. 

Indeed
Create a table: Set up a brand new table layout with defined column types.
sql
CREATE TABLE customers (
    customer_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    city VARCHAR(50)
);
Usa el código con precaución.
Delete a table: Permanently remove an entire table structure and all its data. 

Indeed
 +1
sql
DROP TABLE customers;
Usa el código con precaución.
4. Advanced Analysis (Aggregations & Joins)
SQL shines when combining data or calculating summaries across thousands of records. 

YouTube
·Super SQA | QA Automation
 +1
Aggregate function: Count how many customers live in each city.
sql
SELECT city, COUNT(customer_id) 
FROM customers 
GROUP BY city;
Usa el código con precaución.
Join tables: Combine data from a customers table and an orders table using a shared ID to see who placed what order. 

LearnSQL.com
 +3
sql
SELECT customers.first_name, orders.order_date, orders.total_amount
FROM customers
INNER JOIN orders ON customers.customer_id = orders.customer_id;
Usa el código con precaución.
<div align="center">
<!-- TYPING ANIMATION -->
        <a href="https://github.com/BryanSagbay"> <img
                src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=800&color=A78BFA&center=true&vCenter=true&width=600&lines=Software+Engineer;MSc+Artificial+Intelligence;Full+Stack+Developer;Always+building+something+new+%E2%9A%A1"
                alt="Typing SVG" />
        </a>
    </div>
        <br />
    <div align="center">
        <!-- BADGES -->
        <a href="https://www.linkedin.com/in/bryan-sagbay-1b9912267/" target="_blank">
            <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0A66C2"
                alt="LinkedIn" />
        </a>
        <img
            src="https://komarev.com/ghpvc/?username=BryanSagbay&style=for-the-badge&color=7c3aed&label=PROFILE+VIEWS" />
        <img
            src="https://img.shields.io/github/followers/BryanSagbay?style=for-the-badge&color=5b21b6&labelColor=1e1b4b&label=FOLLOWERS" />
    </div>
    <br>
    <br>
    <div align="center">
        <a href="https://skillicons.dev">
            <img
                src="https://skillicons.dev/icons?i=python,java,js,react,angular,flutter,postgres,mysql,mongodb,firebase&theme=dark" />
        </a>
        <a href="https://skillicons.dev">
            <img
                src="https://skillicons.dev/icons?i=redis,tensorflow,pytorch,sklearn,opencv,docker,vercel,git,github,linux&theme=dark" />
        </a>
    </div>
    <!-- FOOTER -->
    <img width="100%"
        src="https://capsule-render.vercel.app/api?type=waving&height=100&color=0:00d2ff,50:3a7bd5,100:9333ea&descAlignY=100&descAlign=100&fontAlign=50&animation=blink&section=footer" />
</div>
