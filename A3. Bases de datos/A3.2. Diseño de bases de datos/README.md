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

- Uso de los índices descritos anteriormente para una recuperación rápida de datos.
- Particionamiento de tablas grandes como "Orders" por OrderID para mejorar el rendimiento de las consultas.

<br>

## A3.2.2 Construir diagramas de entidad-relación (ERD)

Un **diagrama de entidad-relación (ERD)** es una representación visual de las entidades en la base de datos y la relación entre ellas.

> [!IMPORTANT]  
> **Diagrama de entidad-relación:** una representación visual de las entidades en una base de datos y la relación entre ellas.

Además de proporcionar una visión clara de la estructura de la base de datos, los ERD facilitan la comunicación entre las partes interesadas (stakeholders); actúan como documentación para el diseño de la base de datos; apoyan el desarrollo y mantenimiento futuro; y garantizan la integridad y consistencia de los datos mediante restricciones y relaciones bien definidas.

Para el sistema de ventas con las entidades Productos, Pedidos y Clientes, el ERD se vería así:

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A3.%20Bases%20de%20datos/images/Figura%201.png" alt="BBDD" width="650" height="auto"/>
    <p><em>Figura 1: Modalidad de relaciones. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

La **modalidad en los ERD** se refiere al número mínimo de instancias de una entidad que pueden estar asociadas con una instancia de otra entidad. Define si la participación de una entidad en una relación es opcional (0) o obligatoria (1).

- **Modalidad:** el número mínimo de instancias de una entidad que pueden estar asociadas con una instancia de otra entidad.
- **Cardinalidad:** el número máximo de veces que una instancia en una entidad puede estar asociada con instancias en la entidad relacionada.

Consideremos un ejemplo que involucra datos sobre pacientes y sus historiales médicos en un sistema sanitario. La mayoría de los pacientes tendrán historiales médicos asociados, pero los pacientes nuevos o los recién nacidos podrían no tener ningún historial todavía; por lo tanto, este es un tipo de relación opcional.

Por otro lado, si consideramos una plataforma de comercio electrónico, cada pedido debe estar asociado a un cliente (no puedes convertirte en cliente a menos que realices un pedido), por lo que ese es un tipo de relación obligatoria.

La **cardinalidad** de las relaciones se refiere a la naturaleza y el alcance de las relaciones entre entidades en un ERD. Especifica el número de instancias de una entidad que pueden o deben estar asociadas con cada instancia de otra entidad.

La cardinalidad describe el lado de "muchos" de la relación y se puede definir como:

- Uno a uno (1:1)
- Uno a muchos (1:N)
- Muchos a uno (N:1)
- Muchos a muchos (M:N)

Por ejemplo, consideremos un sistema de gestión escolar que incluye las entidades "STUDENT" y "CLUB".

- La entidad STUDENT tiene como atributos: StudentID, FirstName, LastName, Email.
- La entidad CLUB tiene como atributos: ClubID, Title, TeacherID, Location.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A3.%20Bases%20de%20datos/images/Figura%202.png" alt="BBDD" width="450" height="auto"/>
    <p><em>Figura 2: Relación entre entidades. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>
  
La relación entre las dos entidades puede representarse como "un club tiene muchos estudiantes".

- Cardinalidad: un estudiante puede inscribirse en varios clubes (uno a muchos).
- Modalidad: un club debe tener al menos un estudiante inscrito (obligatorio para los clubes); un estudiante podría no inscribirse en ningún club (opcional para los estudiantes).

Comprender tanto la cardinalidad como la modalidad es esencial para modelar con precisión las relaciones y restricciones en una base de datos, asegurando que refleje eficazmente los requisitos del mundo real y las reglas de negocio.

<br>

### A3.2.3 Tipos de datos utilizados en bases de datos relacionales

| Tipo de dato para atributos | Descripción |
| :--- | :--- |
| **CHARACTER** | Texto de longitud fija. |
| **VARCHAR(n)** | Texto de longitud variable (donde *n* indica el número máximo de caracteres). |
| **INTEGER** | Número entero. |
| **REAL** | Número con parte decimal. |
| **DATE** | Fecha en formato AAAA-MM-DD. |
| **TIME** | Hora en formato HH:MM:SS. |
| **BOOLEAN** | Verdadero (True) o Falso (False). |

Elegir el tipo de dato correcto es fundamental para garantizar una indexación eficiente. Por ejemplo, utilizar `CHARACTER(8)` para datos de longitud fija como un *UserID* es más eficiente que utilizar `VARCHAR(8)`, ya que esto puede generar un tiempo adicional durante la ejecución de las consultas debido al almacenamiento de longitud variable. 

Además, el tipo de dato indica el tipo de operaciones permitidas. Por ejemplo, si almacenas la cantidad y el precio como texto de longitud fija, para realizar cálculos necesitarás convertir el texto a valores de tipo *integer* o *real* en la aplicación antes de poder usar los datos.

Otro aspecto del uso de tipos de datos adecuados es la capacidad de almacenar los datos en el campo correspondiente de la base de datos. Si el tipo de dato de entrada no coincide con el tipo de dato del atributo en la base de datos, el intento de inserción arrojará errores.

La **consistencia de datos** garantiza que los usuarios tengan acceso a información actualizada y precisa, donde todas las copias o instancias sean iguales en todos los sistemas y tablas de la base de datos. El uso de diferentes tipos de datos para referirse al mismo atributo en diferentes plataformas (base de datos y sistema de aplicación) provocará problemas, como la imposibilidad de realizar operaciones específicas del tipo de dato requerido, o actualizaciones y consultas incorrectas.

<br>

### A3.2.4 Construcción de tablas para bases de datos relacionales

La definición adecuada de las tablas en una base de datos sustenta el diseño de los diagramas ERD apropiados y garantiza la integridad de los datos.

Considerando un sistema de gestión escolar, este podría incluir las siguientes tablas:
* **ESTUDIANTE** (ID_Estudiante, Nombre, Apellido, FechaNacimiento, Email)
* **CLUB** (ID_Estudiante, TituloClub, NombreProfesor)
* **PROFESOR** (ClubProfesor, Ubicacion)

#### Tabla: ESTUDIANTE
| ID_Estudiante | Nombre | Apellido | FechaNacimiento | Email |
| :--- | :--- | :--- | :--- | :--- |
| 101 | Fatema | Kada | 02/01/2010 | f.kada@email.com |
| 105 | Alexandru | Buchidau | 05/11/2009 | a.buchidau@email.com |
| 202 | Kada | Hussein | 07/25/2011 | k.hussein@email.com |

En la tabla **ESTUDIANTE**, el `ID_Estudiante` actúa como **clave primaria** para identificar de forma única cada registro de la tabla.

#### Tabla: CLUB
| ID_Estudiante | TituloClub | NombreProfesor |
| :--- | :--- | :--- |
| 105 | Robótica | Bobby Williams |
| 202 | Taekwondo | Dima White |
| 101 | Robótica | Bobby Williams |
| 105 | Artes y Oficios | Jane Doe |

En la tabla **CLUB**, el `ID_Estudiante` es una **clave foránea** (ya que es una clave primaria en la tabla ESTUDIANTE). Sin embargo, ninguno de los campos de esta tabla puede actuar por sí solo como clave primaria, ya que todos tienen duplicados. En este caso, se podría establecer la clave primaria como una **clave compuesta**, formada por los atributos `ID_Estudiante` y `TituloClub`. Por otro lado, se podría añadir un nuevo atributo `ID_Club` para que actúe como clave primaria.

En caso de que sea necesario que un único campo actúe como clave primaria, es posible combinar datos de varios atributos en uno solo para que actúe como una **clave concatenada**.

#### Tabla: PROFESOR
| ClubProfesor (NombreProfesor + TituloClub) | Ubicacion |
| :--- | :--- |
| Jane Doe Artes y Oficios | L101 |
| Bobby Williams Robótica | H203 |
| Dima White Taekwondo | B353 |

En la tabla **PROFESOR**, la clave primaria es una **clave concatenada**, formada a partir de los atributos `NombreProfesor` y `TituloClub`.
