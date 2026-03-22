<h1 align="center">A3.2 Diseño de bases de datos</h1>
<div align="center">

</div>

## Contenido:

- [A3.2.1 Describir el esquema de una base de datos](#a321-describir-el-esquema-de-una-base-de-datos)
- [A3.2.2 Construir diagramas de entidad-relación (ERD)](#a322-construir-diagramas-de-entidad-relación-erd)
- [A3.2.3 Describir los diferentes tipos de datos utilizados en las bases de datos relacionales](#a323-describir-los-diferentes-tipos-de-datos-utilizados-en-las-bases-de-datos-relacionales)
- [A3.2.4 Construir tablas para bases de datos relacionales](#a324-construir-tablas-para-bases-de-datos-relacionales)
- [A3.2.5 Explicar la diferencia entre las formas normales](#a325-explicar-la-diferencia-entre-las-formas-normales)
- [A3.2.6 Construir una base de datos normalizada hasta 3FN para diversos escenarios de la vida real](#a326-construir-una-base-de-datos-normalizada-hasta-3fn-para-diversos-escenarios-de-la-vida-real)
- [A3.2.7 Evaluar la necesidad de desnormalizar bases de datos](#a327-evaluar-la-necesidad-de-desnormalizar-bases-de-datos)

<br>

## A3.2.1 Describir el esquema de una base de datos

El **esquema de la base de datos** es una arquitectura que muestra cómo se organizan los datos y cómo se gestionan las relaciones entre ellos. Proporciona una visión lógica de la base de datos.

> [!IMPORTANT]  
> - **Esquema de la base de datos:** Una arquitectura que muestra cómo se organizan los datos y cómo se gestionan las relaciones entre ellos.
> - **Esquema conceptual:** Un modelo abstracto que describe la estructura de los datos sin considerar cómo se implementarán físicamente.


Existen diferentes tipos de esquemas de bases de datos:

- **Esquema conceptual:** Un modelo abstracto que describe la estructura de los datos sin considerar cómo se implementarán físicamente.
- **Esquema lógico:** Un diseño detallado de la estructura de las tablas (campos y tipos de datos), relaciones entre tablas y restricciones.
- **Esquema físico:** Representa la implementación del esquema lógico en un SGBD (sistema de gestión de bases de datos) específico, mostrando cómo se almacenan, indexan o acceden los datos.

El uso de esquemas de bases de datos mejora:

- **Organización de los datos:** Proporciona una estructura clara para almacenar y organizar la información.
- **Seguridad de los datos:** Define permisos de usuario y vistas para proteger la información.
- **Integridad de los datos:** Utiliza reglas y restricciones para mantener la precisión y consistencia de los datos.
- **Rendimiento:** Mediante el uso de consultas (queries).
- **Escalabilidad:** Permite realizar cambios en la base de datos sin interrumpir las aplicaciones actuales.

El SGBD controla la creación, el mantenimiento y el uso de una base de datos, y actúa como mediador entre las aplicaciones de manejo de datos y el sistema operativo. El SGBD ofrece funciones como consultas a la base de datos, formularios, informes y gráficos para visualizar los datos.

### Esquema conceptual

El **esquema conceptual** es una representación de alto nivel de la base de datos, definiendo su estructura y organización. Es un modelo abstracto que oculta detalles como la implementación de las estructuras de datos o el almacenamiento físico. Define las entidades, atributos y las relaciones entre entidades.

Un método común para implementar el esquema conceptual es mediante el uso de diagramas de entidad-relación (ERD).

Por ejemplo, consideremos un sistema de ventas con la siguiente estructura:

**Entidades:** 

- Products 
- Orders
- Customers

**Atributos:**

- En Products: (ProductID, ProductName, Price)
- En Orders: (OrderID, OrderDate)
- En Customers: (CustomerID, CustomerName, EmailAddress)

**Relaciones:**

- El "customer" realiza una "order".
- Una "order" incluye uno o más "products".

El esquema conceptual es un modelo con detalles insuficientes para construir una base de datos real.

### Esquema lógico

El **esquema lógico** es un modelo que define la estructura de la base de datos, incluyendo entidades, atributos, tipos de datos, restricciones, claves y relaciones. Es un diseño que no tiene en cuenta los requisitos de un sistema de gestión de bases de datos (SGBD) específico.

El esquema lógico se deriva del esquema conceptual mediante:

- La conversión de las entidades en tablas detalladas.
- La definición de los atributos especificando los tipos de datos y restricciones para cada campo de la tabla.
- El establecimiento de claves primarias y foráneas.
- La definición de relaciones entre las tablas mediante el uso de las claves.
- La normalización de la base de datos para minimizar la redundancia de datos.
- La garantía de la integridad de los datos.

> [!IMPORTANT]  
> **Esquema lógico:** un diseño detallado de la estructura de las tablas (campos y tipos de datos), relaciones entre tablas y restricciones.

En el ejemplo anterior:

#### Tablas:

Products
- ProductID: INTEGER (PRIMARY KEY)
- ProductName: VARCHAR
- Price: REAL

Orders
- OrderID: INTEGER (PRIMARY KEY)
- OrderDate: DATE
- CustomerID: INTEGER (FOREIGN KEY)
- ProductID: INTEGER (FOREIGN KEY)

Clientes
- CustomerID: PRIMARY KEY
- CustomerName: VARCHAR
- EmailAddress: VARCHAR, UNIQUE

#### Relaciones:

- Un "customer" realiza una o más "orders" (uno a muchos).
- Una "order" incluye uno o más "products" (uno a muchos).

### Esquema físico

El **esquema físico** incluye detalles específicos de los dispositivos de almacenamiento, métodos de acceso, indexación, particionamiento, vistas y configuración de la base de datos en el soporte de almacenamiento. Traduce el esquema lógico en una implementación que se ajusta a los requisitos de un sistema de gestión de bases de datos específico.

> [!IMPORTANT]  
> **Esquema físico:** una implementación del esquema lógico en un SGBD específico, que muestra cómo se almacenan, indexan o acceden los datos.

En el ejemplo anterior:

#### Tablas:

Products
- ProductID: INT PRIMARY KEY AUTO_INCREMENT
- ProductName: VARCHAR(100) NOT NULL
- Price: REAL NOT NULL

INDEX on ProductName for faster access based on the product name

Orders
- OrderID: INT PRIMARY KEY AUTO_INCREMENT
- OrderDate: DATE NOT NULL
- CustomerID: INT FOREIGN KEY NOT NULL
- ProductID: INT FOREIGN KEY NOT NULL
  
INDEX on CustomerID and ProductID for faster joins

Customers
- CustomerID: INT PRIMARY KEY AUTO_INCREMENT
- LastName: VARCHAR(100) NOT NULL
- FirstName: VARCHAR(100) NOT NULL
- EmailAddress: VARCHAR(100) NOT NULL UNIQUE

INDEX on LastName for faster access based on the last name

#### Parámetros de almacenamiento:

Uso de los índices descritos anteriormente para una recuperación rápida de datos.
Particionamiento de tablas grandes como "Pedidos" por ID_Pedido para mejorar el rendimiento de las consultas.
