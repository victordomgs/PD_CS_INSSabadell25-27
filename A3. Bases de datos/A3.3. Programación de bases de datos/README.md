<h1 align="center">A3.3 Programación de bases de datos</h1>
<div align="center">

</div>

## Contenido:

- [A3.3.1 Describir la diferencia entre los tipos de lenguajes de datos dentro del lenguaje de consulta estructurado (SQL)](#a331-describir-la-ferencia-entre-los-tipos-de-lenguajes-de-datos-dentro-del-lenguaje-de-consulta-estructurado-sql)
- [A3.3.2 Construir consultas entre dos tablas en SQL](#a332-construir-consultas-entre-dos-tablas-en-sql)
- [A3.3.3 Explicar cómo se puede utilizar SQL para actualizar datos en una base de datos](#a333-explicar-cómo-se-puede-utilizar-sql-para-actualizar-datos-en-una-base-de-datos)

<br>

## A3.3.1 Describir la diferencia entre los tipos de lenguajes de datos dentro del lenguaje de consulta estructurado (SQL)

Los tipos de lenguajes de datos incluyen el **lenguaje de definición de datos (DDL)** y el **lenguaje de manipulación de datos (DML)**.

### Lenguaje de definición de datos (DDL)
El lenguaje de definición de datos (DDL) se utiliza para crear, modificar y eliminar estructuras de datos de una base de datos relacional.

| Instrucciones SQL DDL | Explicación |
| :--- | :--- |
| **CREATE** | Crea un nuevo objeto de base de datos (tabla, vista, índice). |
| **PRIMARY KEY** | Establece un campo como clave primaria. |
| **FOREIGN KEY ... REFERENCES ...** | Establece un campo como clave foránea especificando el campo y la tabla con la que está asociado. |
| **ALTER** | Cambia la estructura de un objeto de base de datos existente: altera la estructura de una tabla añadiendo o eliminando columnas o añadiendo restricciones. |
| **DROP** | Elimina objetos de la base de datos (tablas, índices, vistas). |

> [!IMPORTANT]  
> **Lenguaje de definición de datos:** lenguaje que se utiliza para crear, modificar y eliminar estructuras de datos de una base de datos relacional.

#### Sentencias CREATE

```sql
-- Creando una base de datos
CREATE DATABASE HOSPITAL;

-- Creando una tabla
CREATE TABLE Employees (
EmployeeID INT,
DepartmentID INT PRIMARY KEY,
LastName VARCHAR(20)
);

-- Creando una vista
CREATE VIEW EmployeeDetails AS
SELECT EmployeeID, LastName
FROM Employees
JOIN Departments ON Employees.DepartmentID =
Departments.DepartmentID;

-- Creando un índice
CREATE INDEX idx_last_name ON Employees(LastName);

-- Añadir una clave primaria
ALTER TABLE Employees
ADD PRIMARY KEY (EmployeeID);

-- Añadir una clave foránea
ALTER TABLE Employees
ADD FOREIGN KEY DepartmentID REFERENCES
Department(DepartmentID);

-- Añadir una columna
ALTER TABLE Employees
ADD Email VARCHAR(25);

-- Eliminar una columna
ALTER TABLE Employees
DROP COLUMN Email;

-- Añadir una restricción
ALTER TABLE Employees
ADD CONSTRAINT FK_DepartmentID
FOREIGN KEY (DepartmentID) REFERENCES
Departments(DepartmentID);

-- Eliminar una tabla
DROP TABLE Employees;

-- Eliminar un índice
DROP INDEX idx_last_name;

-- Eliminar una vista
DROP VIEW EmployeeData;
```

### Lenguaje de manipulación de datos (DML)

Los lenguajes de manipulación de datos se utilizan para añadir, modificar, eliminar y recuperar datos almacenados en bases de datos relacionales.

| Instrucciones SQL DML | Explicación |
| :--- | :--- |
| **SELECT** | Recupera datos de una o más tablas. |
| **INSERT** | Añade registros a una tabla. |
| **DELETE** | Elimina registros de una tabla. |
| **UPDATE** | Modifica registros existentes en una tabla. |

**Lenguaje de manipulación de datos:** lenguaje que se utiliza para añadir, modificar, eliminar y recuperar datos almacenados en bases de datos relacionales.

#### Sentencias SELECT

```sql
-- Recuperar registros mostrando columnas específicas
SELECT field1, field2, field3...
FROM table_name;

-- Recuperar registros mostrando atributos que coinciden con un criterio dado
SELECT field1, field2, ...
FROM table_name
WHERE condition;

-- Recuperar todos los registros
SELECT * FROM table_name;

-- Recuperar registros comprobando si campos específicos cumplen criterios determinados
SELECT * FROM table_name WHERE condition;
```

<br>

## A3.3.2 Construir consultas entre dos tablas en SQL

### JOIN en una sentencia SELECT

Incluir un **JOIN** en una sentencia **SELECT** permite agregar datos de múltiples tablas. Por ejemplo, considerando las tablas `Employees` y `Department`, el siguiente script recupera el gasto salarial agrupado por departamento.

```sql
SELECT Employees.DepartmentName,
SUM(Employees.Salary) AS TotalSalary
FROM Employees
JOIN Department ON Employees.DepartmentID = Department.DepartmentID
GROUP BY Department.DepartmentName;
```

### DISTINCT en una sentencia SELECT

Cuando se desea recuperar registros únicos e ignorar duplicados, se utiliza la palabra clave **DISTINCT**.

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

### Cláusula HAVING frente a cláusula WHERE

La cláusula **HAVING** se utiliza para filtrar grupos de registros creados por la cláusula **GROUP BY**. Por ejemplo, para recuperar el ID del departamento y el salario promedio por departamento donde dicho promedio sea superior a 10,000.

La cláusula **WHERE** se utiliza para filtrar registros antes de la agrupación, mientras que la cláusula **HAVING** se utiliza para filtrar grupos después de la agregación.

```sql
SELECT DepartmentID, Salary
FROM Employees
GROUP BY DepartmentID
HAVING Salary > 10000;
```

### Operadores relacionales

| Operador | Ejemplo |
| :--- | :--- |
| **Igual a (=)** | `SELECT * FROM Employees WHERE DepartmentID = 1;` |
| **No igual a (<>)** | `SELECT * FROM Employees WHERE DepartmentID <> 1;` |
| **Mayor que (>)** | `SELECT * FROM Employees WHERE Salary > 10000;` |
| **Menor que (<)** | `SELECT * FROM Employees WHERE Salary < 10000;` |
| **Mayor o igual que (>=)** | `SELECT * FROM Employees WHERE Salary >= 10000;` |
| **Menor o igual que (<=)** | `SELECT * FROM Employees WHERE Salary <= 10000;` |

#### Filtrado y combinación de condiciones

| Operador | Ejemplo |
| :--- | :--- |
| **BETWEEN** (rango) | `SELECT * FROM Employees WHERE Salary BETWEEN 50000 AND 100000;` |
| **IN** (lista de valores) | `SELECT * FROM Employees WHERE DepartmentID IN (1, 2, 3);` |
| **IS NULL** (nulos) | `SELECT * FROM Employees WHERE ManagerID IS NULL;` |
| **IS NOT NULL** (no nulos) | `SELECT * FROM Employees WHERE ManagerID IS NOT NULL;` |
| **Lógicos (AND, OR)** | `SELECT * FROM Employees WHERE (DepartmentID = 5 AND Salary > 50000) OR (DepartmentID = 1 AND Salary > 10000);` |

#### Coincidencia de patrones (Pattern matching)
* **LIKE** filtra valores basados en un patrón.
* **%** se utiliza para cualquier secuencia de caracteres (cero o más).
* **_** se utiliza para un único carácter.

```sql
-- Recuperar registros que empiezan con la letra 'D'
SELECT * FROM Employees WHERE LastName LIKE 'D%';

-- Recuperar registros que terminan con la letra 'd':
SELECT * FROM Employees WHERE LastName LIKE '%d';

-- Patrón específico (empieza con 'D', sigue un carácter, luego 'm' y después cualquier secuencia)
SELECT * FROM Employees WHERE LastName LIKE 'D_m%';

-- Registros compuestos exactamente por tres caracteres
SELECT * FROM Employees WHERE LastName LIKE '_ _ _';
```

### Ordenación de datos (Ordering)

```sql
-- Por un solo campo
SELECT * FROM Employees ORDER BY LastName;

-- Ascendente
SELECT * FROM Employees ORDER BY LastName ASC;

-- Descendente
SELECT * FROM Employees ORDER BY LastName DESC;

-- Múltiples campos
SELECT * FROM Employees ORDER BY DepartmentID, Salary DESC;
```

<br>

## A3.3.3 Explicar cómo se puede utilizar SQL para actualizar datos en una base de datos

### A3.3.3 Consultas de actualización en SQL

| Sentencia SQL | Explicación | Ejemplo |
| :--- | :--- | :--- |
| **INSERT** | Añade nuevos registros. | `INSERT INTO table_name (field1, field2, ...) VALUES (value1, value2, ...);` |
| **DELETE** | Elimina registros. | `DELETE FROM table_name WHERE condition;` |
| **UPDATE** | Modifica registros. | `UPDATE table_name SET field1 = value1, field2 = value2, ... WHERE condition;` |

Las columnas indexadas optimizan el rendimiento de las consultas, pero la actualización de datos en dichas columnas puede impactar negativamente en el rendimiento. Cuando se realiza una actualización en una columna indexada, el índice también debe actualizarse, lo que puede ralentizar la operación. Además, las actualizaciones de índices pueden provocar el bloqueo de otras transacciones que necesiten acceder a un registro específico. 

Para superar estos desafíos, puedes:
* **Procesar las actualizaciones por lotes (batching):** para reducir el número de veces que el índice necesita ser modificado.
* **Reconstruir o reorganizar índices con frecuencia:** para reducir la fragmentación.
* **Usar índices parciales o filtrados:** para limitar el alcance del índice únicamente a los registros más relevantes.
