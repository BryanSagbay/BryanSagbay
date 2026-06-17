These queries extract information from your database tables.Select all columns: Retrieves every row and column from a specific table.sqlSELECT * FROM employees;
Usa el código con precaución.Select specific columns: Limits the results to requested attributes for better efficiency.sqlSELECT first_name, last_name, salary FROM employees;
Usa el código con precaución.Filter data with conditions (WHERE): Isolates specific records based on numerical or text logic.sqlSELECT * FROM employees WHERE salary > 70000;
Usa el código con precaución.Combine filters (AND/OR): Joins multiple conditions together for precision filtering.sqlSELECT * FROM employees WHERE salary > 70000 AND department_id = 2;
Usa el código con precaución.Pattern matching (LIKE): Finds specific string structures, such as names starting with "J".sqlSELECT first_name, last_name FROM employees WHERE last_name LIKE 'J%';
Usa el código con precaución.Data Manipulation (DML)These operations allow you to add, modify, or delete database rows.Insert a new record: Adds a single new row into a designated table.sqlINSERT INTO employees (id, first_name, last_name, salary) 
VALUES (101, 'Alice', 'Smith', 85000);
Usa el código con precaución.Update existing records: Modifies data matching a specific rule (always use a WHERE clause to avoid updating everything).sqlUPDATE employees SET salary = 90000 WHERE id = 101;

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
