Microsoft SQL Server uses Transact-SQL (T-SQL), which extends standard SQL with proprietary features like variables, error handling, and string processing. Below is a structured compilation of essential SQL Server coding examples and official sample databases.Basic Data Manipulation (CRUD)1. Create a TableCreates a new table named Employees with an auto-incrementing primary key.sqlCREATE TABLE Employees (
    EmployeeID INT IDENTITY(1,1) PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Email VARCHAR(100) UNIQUE,
    HireDate DATE DEFAULT GETDATE(),
    Salary DECIMAL(10,2)
);
Usa el código con precaución.2. Insert DataInserts a new record into the Employees table.sqlINSERT INTO Employees (FirstName, LastName, Email, Salary)
VALUES ('Jane', 'Doe', 'jane.doe@example.com', 65000.00);
Usa el código con precaución.3. Select DataRetrieves specific columns for active or high-earning employees.sqlSELECT EmployeeID, FirstName, LastName, Salary 
FROM Employees 
WHERE Salary >= 50000.00 
ORDER BY LastName ASC;
Usa el código con precaución.4. Update DataModifies existing records based on a conditional filter.sqlUPDATE Employees 
SET Salary = Salary * 1.05 
WHERE EmployeeID = 1;
Usa el código con precaución.5. Delete DataRemoves data safely using a WHERE clause.sqlDELETE FROM Employees 
WHERE EmployeeID = 1;
Usa el código con precaución.Intermediate & Advanced QueriesInner JoinCombines rows from two tables based on a related column.sqlSELECT e.FirstName, e.LastName, d.DepartmentName
FROM Employees e
INNER JOIN Departments d ON e.DepartmentID = d.DepartmentID;
Usa el código con precaución.Aggregation and GroupingCalculates the total salary spent per department, filtering for groups exceeding $100,000.sqlSELECT DepartmentID, SUM(Salary) AS TotalBudget
FROM Employees
GROUP BY DepartmentID
HAVING SUM(Salary) > 100000.00;
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
