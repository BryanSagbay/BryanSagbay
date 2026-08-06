Usa el código con precaución.4. Advanced T-SQL FeaturesVariables, conditional logic (CASE statements), and temporary tables help build sophisticated logic.sql-- Declare and use a variable
DECLARE @MinSalary DECIMAL(10,2) = 50000.00;

-- Use a CASE statement for conditional grouping inside a query
SELECT FirstName, LastName, Salary,
       CASE 
           WHEN Salary >= 80000 THEN 'High Tier'
           WHEN Salary >= 50000 THEN 'Mid Tier'
           ELSE 'Entry Tier'
       END AS SalaryBracket
FROM Employees
WHERE Salary > @MinSalary;
Usa el código con precaución.Official Ready-to-Use Sample DatabasesIf you want to practice with pre-configured relational data instead of writing your own script from scratch, download these official sample environments hosted on the Azure Data SQL Samples GitHub Repository:AdventureWorks: The primary, comprehensive operational database (OLTP) modeling a fictional bicycle manufacturing company.Wide World Importers: The standard dataset for SQL Server 2016 and newer, showcasing modern features like JSON and temporal tables.Northwind & Pubs: Lightweight legacy databases containing sample tracking data for order management and book publishing.If you want to continue, let me know:What specific business scenario you are trying to solve (e.g., inventory tracking, user login)?Do you need help with performance tuning (like indexing) or automation (like stored procedures)?I can generate custom-tailored scripts to fit your project.
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
