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

* **Recuperar registros mostrando columnas específicas:**
```sql
SELECT field1, field2, field3...
FROM table_name;
