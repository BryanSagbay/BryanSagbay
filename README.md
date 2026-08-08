
CREATE DATABASE CompanyDB;
GO

-- Switch to the new database context
USE CompanyDB;
GO

-- 2. Create a Department table
CREATE TABLE Departments (
    DepartmentID INT IDENTITY(1,1) PRIMARY KEY, -- Auto-incrementing primary key
    DepartmentName VARCHAR(50) NOT NULL,
    Location VARCHAR(100) DEFAULT 'Main Campus'
);

-- 3. Create an Employees table with a Foreign Key
CREATE TABLE Employees (
    EmployeeID INT IDENTITY(1,1) PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Email VARCHAR(100) UNIQUE,
    HireDate DATE DEFAULT GETDATE(), -- Defaults to current system date
    Salary DECIMAL(10, 2),
    DepartmentID INT FOREIGN KEY REFERENCES Departments(DepartmentID)
);
Usa el código con precaución.Data Manipulation Language (DML)These commands handle data insertions, modifications, and deletions.sql-- 1. Insert multiple rows of data
INSERT INTO Departments (DepartmentName, Location)
VALUES ('Engineering', 'Building A'),
       ('Human Resources', 'Building B'),
       ('Marketing', 'Building A');

INSERT INTO Employees (FirstName, LastName, Email, Salary, DepartmentID)
VALUES ('John', 'Doe', 'john.doe@company.com', 85000.00, 1),
       ('Jane', 'Smith', 'jane.smith@company.com', 92000.00, 1),
       ('Alice', 'Johnson', 'alice.j@company.com', 65000.00, 2);

-- 2. Update existing data securely
UPDATE Employees
SET Salary = Salary * 1.05
WHERE DepartmentID = 1; -- 5% raise for Engineering

-- 3. Delete specific records
DELETE FROM Employees
WHERE EmployeeID = 3;
Usa el código con precaución.Querying Data (Advanced Selects)SQL Server offers advanced querying mechanisms like JOIN op
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
