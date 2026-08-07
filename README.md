FirstName, LastName, Salary, DepartmentID
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
