Microsoft SQL Server uses Transact-SQL (T-SQL), which extends standard SQL with additional features like error handling, declaring variables, and string manipulation.Below is a comprehensive guide featuring essential T-SQL queries, ranging from basic database operations to advanced data analysis techniques.Database and Table Operations1. Create a DatabaseCreates a new database instance container.sqlCREATE DATABASE CompanyDB;
GO
Usa el código con precaución.2. Create a Table with ConstraintsCreates a table named Employees with automated primary keys, text constraints, and basic validation.sqlUSE CompanyDB;
GO

CREATE TABLE Employees (
    EmployeeID INT IDENTITY(1,1) PRIMARY KEY,
    FirstName NVARCHAR(50) NOT NULL,
    LastName NVARCHAR(50) NOT NULL,
    Email VARCHAR(100) UNIQUE,
    Salary DECIMAL(10,2) CHECK (Salary > 0),
    HireDate DATE DEFAULT GETDATE()
);
GO
Usa el código con precaución.Data Manipulation Language (DML)3. Insert RecordsAdds single or multiple rows into a table.sqlINSERT INTO Employees (FirstName, LastName, Email, Salary)
VALUES 
('Alice', 'Smith', 'alice.smith@example.com', 65000.00),
('Bob', 'Jones', 'bob.jones@example.com', 55000.00),
('Charlie', 'Brown', 'charlie.brown@example.com', 72000.00);
Usa el código con precaución.4. Update RecordsModifies data safely using filtering criteria.sqlUPDATE Employees
SET Salary = Salary * 1.05
WHERE EmployeeID = 1;
Usa el código con precaución.5. Delete RecordsRemoves records based on specific parameters.sqlDELETE FROM Employees
WHERE EmployeeID = 2;
Usa el código con precaución.Data Querying & Analysis6. Basic Select with Filtering and SortingFinds records matching unique criteria and organizes the resulting data.sqlSELECT EmployeeID, FirstName, LastName, Salary
FROM Employees
WHERE Salary >= 60000
ORDER BY LastName ASC;
Usa el código con precaución.7. Inner JoinCombines records across multiple tables by linking their keys.sql-- Assumes a second table 'Departments' exists with DepartmentID
SELECT E.FirstName, E.LastName, D.DepartmentName
FROM Employees E
INNER JOIN Departments D ON E.DepartmentID = D.DepartmentID;
Usa el código con precaución.8. Aggregate Data with Group ByCalculates group metrics and applies filters to the grouped results.sqlSELECT DepartmentID, COUNT(*) AS EmployeeCount, AVG(Salary) AS AverageSalary
FROM Employees
GROUP BY DepartmentID
HAVING AVG(Salary) > 50000;
Usa el código con precaución.Advanced T-SQL Features9. Common Table Expressions (CTE) & Window FunctionsCalculates running analytical operations across data subsets without grouping rows.sqlWITH RankedEmployees AS (
    SELECT FirstName, LastName, Salary, DepartmentID,
           ROW_NUMBER() OVER (PARTITION BY DepartmentID ORDER BY Salary DESC) AS SalaryRank
    FROM Employees
)
SELECT FirstName, LastName, Salary, DepartmentID
FROM RankedEmployees
WHERE SalaryRank = 1; -- Returns the highest paid employee in each department
Usa el código con precaución.10. Stored Procedure with VariablesSaves modular, parameterized code inside the database engine for optimized reuse.sqlCREATE PROCEDURE GetEmployeeByEmail
    @EmailAddress VARCHAR(100)
AS
BEGIN
    SET NOCOUNT ON;
    
    SELECT EmployeeID, FirstName, LastName, Salary
    FROM Employees
    WHERE Email = @EmailAddress;
END;
GO

-- To execute the procedure:
EXEC GetEmployeeByEmail @EmailAddress = 'alice.smith@example.com';
Usa el código con precaución.Official Ready-Made Sample DatabasesIf you are looking for ready-made sample schemas populated with dummy data for deep practice, testing, or benchmarking, Microsoft officially maintains several open-source databases:AdventureWorks: The standard, classic fictional bicycle manufacturing company database used for OLTP, data warehousing, and lightweight scenarios.WideWorldImporters: A modern wholesale grocery distributor database showcasing newer SQL Server engine features like JSON parsing, temporal tables, and In-Memory OLTP.Northwind and Pubs: Legacy, highly simplified database scripts built for older application tutorials.Would you like help writing a specific type of query, such as database performance tuning scripts, JSON data processing, or handling try-catch error blocks?
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
