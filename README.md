databases.Here are the most common SQL examples organized by function:Data Query Language (DQL) - Retrieving DataSelect All: Retrieve every column and row from a table.sqlSELECT * FROM customers;
Usa el código con precaución.Select Specific Columns: Fetch only specific details.sqlSELECT first_name, last_name FROM customers;
Usa el código con precaución.Filter Data (WHERE): Limit rows using a condition.sqlSELECT * FROM employees WHERE salary > 50000;
Usa el código con precaución.Sort Data (ORDER BY): Sort results in ascending or descending (DESC) order.sqlSELECT * FROM products ORDER BY price DESC;
Usa el código con precaución.Data Manipulation Language (DML) - Modifying DataInsert Data: Add a new record into a table.sqlINSERT INTO customers (id, first_name, last_name) 
VALUES (1, 'Alice', 'Smith');
Usa el código con precaución.Update Data: Modify existing records.sqlUPDATE employees SET salary = 60000 WHERE id = 1;
Usa el código con precaución.Delete Data: Remove specific records.sqlDELETE FROM customers WHERE id = 1;
Usa el código con precaución.Data Definition Language (DDL) - Structuring DatabasesCreate a Table: Define columns and data types.sqlCREATE TABLE employees (
    id INT PRIMARY KEY,
    first_name VARCHAR(50),
    salary DECIMAL(10,2)
);
Usa el código con precaución.Intermediate Queries - Aggregation & Combining TablesGroup & Aggregate (GROUP BY): Count records matching a category.sqlSELECT department_id, COUNT(*) FROM employees GROUP BY department_id;
Usa el código con precaución.Join Tables (INNER JOIN): Combine rows from two different tables based on a related column.sqlSELECT orders.id, customers.first_name 
FROM orders 
INNER JOIN customers ON orders.customer_id = customers.id;
Usa el código con precaución.If you are working on a project, tell me what database platform you are using (like MySQL or PostgreSQL) and what problem you are trying to solve so I can write the exact query you need.
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
