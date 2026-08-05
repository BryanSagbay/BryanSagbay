Usa el código con precaución.Update Rows: Edits existing field variables safely via filtered conditional tags.sqlUPDATE Employees
SET Salary = Salary * 1.05
WHERE HireDate < '2025-01-01';
Usa el código con precaución.Delete Rows: Purges specific row instances matching targeted search criteria.sqlDELETE FROM Employees
WHERE EmployeeID = 2;
Usa el código con precaución.Querying DataExtract tailored insights from your database structures:Basic Select: Pulls specified column details using clean sorting layouts.sqlSELECT FirstName, LastName, Salary
FROM Employees
WHERE Salary >= 60000
ORDER BY LastName ASC;
Usa el código con precaución.Inner Join: Connects multiple relational targets across mapped key attributes.sqlSELECT E.FirstName, E.LastName, D.DepartmentName
FROM Employees E
INNER JOIN Departments D ON E.DepartmentID = D.DepartmentID;
Usa el código con precaución.Aggregation: Bundles data arrays into calculated analytical outcomes.sqlSELECT DepartmentID, AVG(Salary) AS AverageSalary, COUNT(*) AS Headcount
FROM Employees
GROUP BY DepartmentID
HAVING COUNT(*) > 5;
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
