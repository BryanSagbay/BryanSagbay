
Microsoft SQL Server utilizes Transact-SQL (T-SQL) to manage and manipulate relational databases.Below are fundamental, practical examples categorized by everyday database operations.1. Data Definition Language (DDL)These commands define and alter your database structures.sql-- Create a new database
CREATE DATABASE CompanyDB;
GO

-- Switch context to the new database
USE CompanyDB;
GO

-- Create a table with constraints
CREATE TABLE Employees (
    EmployeeID INT IDENTITY(1,1) PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Email VARCHAR(100) UNIQUE,
    HireDate DATE DEFAULT GETDATE(),
    Salary DECIMAL(10,2)
);
GO
Usa el código con precaución.2. Data Manipulation Language (DML)Use these statements to add, modify, delete, and view your records.sql-- Insert multiple records
INSERT INTO Employees (FirstName, LastName, Email, Salary)
VALUES 
('Jane', 'Doe', 'jane.doe@example.com', 65000.00),
('John', 'Smith', 'john.smith@example.com', 55000.00),
('Alice', 'Johnson', 'alice.j@example.com', 72000.00);

-- Query data using filtering and sorting
SELECT EmployeeID, FirstName, LastName, Salary
FROM Employees
WHERE Salary > 60000
ORDER BY LastName ASC;

-- Update specific data records
UPDATE Employees
SET Salary = 68000.00
WHERE EmployeeID = 1;

-- Delete a specific record
DELETE FROM Employees
WHERE EmployeeID = 2;
Usa el código con precaución.3. Aggregation and GroupingAggregate functions allow you to perform calculations on sets of rows.sql-- Calculate the average salary and total staff size
SELECT 
    COUNT(EmployeeID) AS TotalEmployees,
    AVG(Salary) AS AverageSalary,
    MAX(Salary) AS HighestSalary
FROM Employees;
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
