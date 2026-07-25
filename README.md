SQL (Structured Query Language) is the standard language used to manage, manipulate, and retrieve data from relational databases. Below is a structured guide featuring essential SQL command examples categorized by their use case.Data Retrieval (DQL)These queries pull information out of database tables without changing any underlying data.Select All Columns: Retrieves every column and row from a table.sqlSELECT * FROM employees;
Usa el código con precaución.Select Specific Columns: Limits the output to only chosen fields for better performance.sqlSELECT first_name, salary FROM employees;
Usa el código con precaución.Filter with WHERE: Returns records matching a strict conditional statement.sqlSELECT * FROM employees WHERE salary > 70000;
Usa el código con precaución.Sort with ORDER BY: Organizes results alphabetically or numerically in descending (DESC) or ascending order.sqlSELECT * FROM employees ORDER BY hire_date DESC;
Usa el código con precaución.Data Modification (DML)These statements allow you to add, modify, or erase data values stored inside your tables.Insert Records: Adds a completely new row of data to the table.sqlINSERT INTO employees (first_name, last_name, salary) 
VALUES ('John', 'Doe', 65000);
Usa el código con precaución.Update Records: Overwrites existing table cells using a filter to target specific rows.sqlUPDATE employees SET salary = 68000 WHERE employee_id = 101;
Usa el código con precaución.Delete Records: Permanently removes rows matching the criteria.sqlDELETE FROM employees WHERE status = 'Terminated';
Usa el código con precaución.Aggregation & GroupingUse these queries to calculate math summaries like sums, averages, and counts across multiple rows.Group and Count: Counts how many records belong to each individual group.sqlSELECT department_id, COUNT(*) FROM employees GROUP BY department_id;
Usa el código con precaución.Filter Groups with HAVING: Filters grouped data blocks after aggregation occurs.sqlSELECT department_id, AVG(salary) 
FROM employees 
GROUP BY department_id 
HAVING AVG(salary) > 60000;
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
