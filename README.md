QL Server uses Transact-SQL (T-SQL), an extended version of standard SQL developed by Microsoft.The most common SQL Server syntax examples range from basic CRUD (Create, Read, Update, Delete) operations to advanced analytical tools.1. Database and Table ManagementBefore manipulating data, you must define the database structure.Create Database: Initializes a new storage container.sqlCREATE DATABASE CompanyDB;
Usa el código con precaución.Create Table: Defines columns, data types, and primary keys.sqlCREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY IDENTITY(1,1),
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    HireDate DATE DEFAULT GETDATE(),
    Salary DECIMAL(10,2)
);
Usa el código con precaución.2. Basic CRUD OperationsThese commands handle basic data modification and extraction.Insert Data: Adds rows to a table.sqlINSERT INTO Employees (FirstName, LastName, Salary)
VALUES ('John', 'Doe', 60000.00), ('Jane', 'Smith', 75000.00);
Usa el código con precaución.Select Data: Retrieves information based on filtered criteria.sqlSELECT FirstName, LastName, Salary 
FROM Employees 
WHERE Salary > 65000;
Usa el código con precaución.Update Data: Modifies existing records.sqlUPDATE Employees 
SET Salary = Salary * 1.05 
WHERE EmployeeID = 1;
Usa el código con precaución.Delete Data: Permanently removes rows.sqlDELETE FROM Employees 
WHERE EmployeeID = 2;
Usa el código con precaución.3. Aggregation and GroupingThese functions summarize massive amounts of data into readable metrics.Group By & Having: Groups rows and filters the resulting sets.sqlSELECT LastName, AVG(Salary) AS AverageSalary
FROM Employees
GROUP BY LastName
HAVING AVG(Salary) > 50000;
Usa el código con precaución.4. Advanced T-SQL FeaturesSQL Server provides built-in tools for complex queries and execution speed.Common Table Expressions (CTE): Creates a temporary result set for readability.sqlWITH HighEarners AS (
    SELECT EmployeeID, FirstName, Salary
    FROM Employees
    WHERE Salary > 70000
)
SELECT * FROM HighEarners;
Usa el código con precaución.Stored Procedures: Saves reusable SQL code blocks to execute parameters safely.sqlCREATE PROCEDURE GetEmployeeByLastName
    @LName VARCHAR(50)
AS
BEGIN
    SELECT * FROM Employees WHERE LastName = @LName;
END;

-- To run it:
EXEC GetEmployeeByLastName @LName = 'Doe';
Usa el código con precaución.Official Sample Databases
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
