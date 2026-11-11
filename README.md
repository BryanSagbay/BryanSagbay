

Querio
sql
SELECT department_id, SUM(salary) AS total_payroll
FROM employees
GROUP BY department_id
HAVING SUM(salary) > 500000;
Usa el código con precaución.
6. Combine Tables (JOIN)
Merges rows from two or more tables based on a related column between them. 

Querio
sql
SELECT orders.order_id, customers.customer_name, orders.order_date
FROM orders
INNER JOIN customers ON orders.customer_id = customers.customer_id;
Usa el código con precaución.
7. Modify Data (UPDATE)
Changes existing records in a table. Always ensure you use a WHERE clause, or you will update every row in the database! 

JS Mastery Pro
sql
UPDATE employees 
SET salary = salary * 1.05 
WHERE performance_rating = 'Excellent';
Usa el código con precaución.
8. Use Subqueries
Nests a query inside another query to perform complex, multi-step filtering. 

JS Mastery Pro
sql
SELECT first_name, salary 
FROM employees 
WHERE salary > (SELECT AVG(salary) FROM employees);
Usa el código con precaución.
9. Organize with CTEs (WITH)
Common Table Expressions (CTEs) create a temporary, named result set that makes complex queries much easier to read and maintain. 

Medium
·DataNest
 +1
sql
WITH HighEarners AS (
    SELECT employee_id, first_name, salary
    FROM employees
    WHERE salary > 100000
)
SELECT * FROM HighEarners WHERE salary < 150000;
Usa el código con precaución.
10. Sequential Ranking (ROW_NUMBER())
A powerful window function used to assign a sequential integer to each row within a partition of your data. 

YouTube
·techTFQ
 +1
sql
SELECT employee_id, department_id, salary,
       ROW_NUMBER() OVER (PARTITION BY department_id ORDER BY salary DESC) as salary_rank
FROM employees;
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
