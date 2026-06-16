SELECT 
    d.nombre_departamento,
    er.nombre AS empleado,
    er.salario
FROM EmpleadosRanking er
JOIN departamentos d ON er.id_departamento = d.id
-- Filtramos para obtener solo los 3 primeros de cada departamento
WHERE er.ranking_salario <= 3
ORDER BY d.nombre_departamento, er.ranking_salario ASC;
Usa el código con precaución.Ejemplo 2: Análisis financiero y segmentación de clientes (CASE y GROUP BY)Esta consulta agrupa a los clientes y etiqueta sus comportamientos, calculando el total gastado y categorizándolos en tiempo real (por ejemplo: 'VIP', 'Regular', 'Nuevo').sqlSELECT 
    c.id_cliente,
    c.nombre,
    SUM(f.monto_total) AS gasto_acumulado,
    COUNT(f.id_factura) AS total_compras,
    -- Clasificación dinámica según el volumen de compras
    CASE 
        WHEN SUM(f.monto_total) > 10000 THEN 'VIP'
        WHEN SUM(f.monto_total) BETWEEN 5000 AND 10000 THEN 'Regular'
        ELSE 'Nuevo/Ocasional'
    END AS categoria_cliente,
    MAX(f.fecha_emision) AS ultima_compra
FROM clientes c
LEFT JOIN facturas f ON c.id_cliente = f.id_cliente
WHERE f.fecha_emision >= DATE_SUB(CURRENT_DATE, INTERVAL 1 YEAR)
GROUP BY 
    c.id_cliente, 
    c.nombre
HAVING SUM(f.monto_total) > 1000
ORDER BY gasto_acumulado DESC;

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
