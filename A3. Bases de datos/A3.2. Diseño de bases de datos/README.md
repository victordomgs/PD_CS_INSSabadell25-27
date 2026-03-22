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

### A3.2.3 Describir los diferentes tipos de datos utilizados en las bases de datos relacionales

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

### A3.2.4 Construir tablas para bases de datos relacionales

La definición adecuada de las tablas en una base de datos sustenta el diseño de los diagramas ERD apropiados y garantiza la integridad de los datos.

Considerando un sistema de gestión escolar, este podría incluir las siguientes tablas:
* **STUDENT** (StudentID, FirstName, LastName, DateOfBirth, Email)
* **CLUB** (StudentID, ClubTitle, TeacherName)
* **TEACHER** (TeacherClub, Location)

#### Tabla: STUDENT
| StudentID | FirstName | LastName | DateOfBirth | Email |
| :--- | :--- | :--- | :--- | :--- |
| 101 | Fatema | Kada | 02/01/2010 | f.kada@email.com |
| 105 | Alexandru | Buchidau | 05/11/2009 | a.buchidau@email.com |
| 202 | Kada | Hussein | 07/25/2011 | k.hussein@email.com |

En la tabla **STUDENT**, el `StudentID` actúa como **clave primaria** para identificar de forma única cada registro de la tabla.

#### Tabla: CLUB
| StudentID | ClubTitle | TeacherName |
| :--- | :--- | :--- |
| 105 | Robótica | Bobby Williams |
| 202 | Taekwondo | Dima White |
| 101 | Robótica | Bobby Williams |
| 105 | Artes y Oficios | Jane Doe |

En la tabla **CLUB**, el `StudentID` es una **clave foránea** (ya que es una clave primaria en la tabla STUDENT). Sin embargo, ninguno de los campos de esta tabla puede actuar por sí solo como clave primaria, ya que todos tienen duplicados. En este caso, se podría establecer la clave primaria como una **clave compuesta**, formada por los atributos `StudentID` y `ClubTitle`. Por otro lado, se podría añadir un nuevo atributo `ClubdID` para que actúe como clave primaria.

En caso de que sea necesario que un único campo actúe como clave primaria, es posible combinar datos de varios atributos en uno solo para que actúe como una **clave concatenada**.

#### Tabla: TEACHER
| TeacherClub (TeacherName + ClubTitle) | Location |
| :--- | :--- |
| Jane Doe Artes y Oficios | L101 |
| Bobby Williams Robótica | H203 |
| Dima White Taekwondo | B353 |

En la tabla **TEACHER**, la clave primaria es una **clave concatenada**, formada a partir de los atributos `TeacherName` y `ClubTitle`.

<br>

## A3.2.5 Explicar la diferencia entre las formas normales

La normalización de datos representa el proceso de organizar los datos en una base de datos relacional de manera que se reduzca la redundancia y se mejore la integridad de los datos. La redundancia se reduce ya que cada elemento de datos solo aparece en una ubicación de la base de datos. Esto puede disminuir la posibilidad de que ocurran anomalías de actualización y hace un uso más eficiente de la memoria.

La normalización da lugar a tablas más pequeñas con menos información en cada fila, lo que conlleva una reducción de las transferencias de entrada/salida (I/O); así, la CPU puede trabajar a plena capacidad al reducirse la probabilidad de que sus actividades se suspendan. La normalización se logra a través de una serie de etapas llamadas "formas normales", donde cada forma normal tiene requisitos específicos para que la tabla sea considerada normalizada en ese nivel.

* **Normalización:** el proceso de organizar los datos en una base de datos relacional para reducir la redundancia y mejorar la integridad de los datos.
* **Primera forma normal:** el estado de una base de datos relacional en el que las entidades no contienen grupos repetidos de atributos.
* **Atómico:** cada atributo de una tabla contiene valores indivisibles (valores que no pueden desglosarse en subvalores más detallados).

### Primera forma normal (1NF)

En la primera forma normal, la tabla:
* Tiene una clave primaria (**primary key**).
* No incluye atributos duplicados de la misma tabla.
* No incluye grupos repetidos de atributos.

Por lo tanto, es necesario crear tablas separadas para cada grupo de datos relacionados, identificando cada registro mediante el uso de la clave primaria —ya sea un solo atributo o un conjunto de ellos (clave compuesta o compuesta)— y asegurar que las entidades no contengan grupos repetidos de atributos.

En 1NF, los datos de cada campo deben ser **atómicos**. Esto significa que cada atributo contiene valores indivisibles. Por ejemplo, un atributo llamado `TeacherName` en la tabla `TEACHER` no es un campo atómico, ya que podría dividirse en dos atributos diferentes llamados `LastName` y `FirstName`. Una vez hecho esto, los campos son atómicos. La atomicidad garantiza que cada celda de la tabla contenga un solo valor, no estructuras complejas como arrays o listas.

La **dependencia funcional** es una relación que existe entre atributos, donde un conjunto de atributos (el determinante) determina el valor del otro conjunto (el dependiente). Normalmente, esta es una relación entre el atributo de la clave primaria y un atributo que no es clave. Por ejemplo, en la tabla `STUDENT`, el `StudentID` (clave primaria y determinante) determina los valores de `FirstName`, `LastName`, `DateOfBirth` y `Email` (los dependientes). Esto significa que, dado el valor del `StudentID`, puedes encontrar los demás detalles, pero no viceversa.

* **Dependencia funcional:** relación entre atributos donde un conjunto (determinante) determina el valor de otro (dependiente).
* **Dependencia funcional completa:** cuando los atributos dependientes son determinados por la totalidad de los atributos determinantes.
* **Dependencia funcional parcial:** cuando los atributos dependientes son determinados solo por una parte de los atributos determinantes.
* **Dependencia transitiva:** tipo de dependencia funcional que ocurre cuando un atributo no primo depende de otro atributo no primo, en lugar de la clave primaria.
* **Segunda forma normal (2NF):** estado en el que las entidades están en 1NF y cualquier atributo que no sea clave depende de la clave primaria.
* **Tercera forma normal (3NF):** estado en el que las entidades están en 2NF y todos los atributos que no son clave son independientes entre sí.

### Segunda forma normal (2NF)

En la segunda forma normal (2NF):
* Las entidades están en 1NF.
* Cualquier atributo que no sea clave tiene una **dependencia funcional completa** de la clave primaria; no existen dependencias parciales.

La dependencia de clave parcial ocurre en una tabla que tiene una clave compuesta como clave primaria y uno o más atributos que no son clave dependen solo de un subconjunto de dicha clave compuesta. Por ejemplo, en la tabla `CLUB`, el atributo `TeacherName` depende de `ClubTitle`, pero no de `StudentID`. Como la clave primaria en esta tabla es compuesta (`ClubTitle` y `StudentID`), el `TeacherName` debería haber dependido funcionalmente de ambos campos para cumplir con la 2NF.

### Tercera forma normal (3NF)

En la tercera forma normal (3NF):
* Las entidades están en 2NF.
* Todos los atributos que no son clave son independientes (se eliminan las columnas que no dependen funcionalmente de forma completa de la clave primaria); la tabla no contiene dependencias no clave.

La dependencia transitiva ocurre cuando un atributo no primo depende de otro atributo no primo. Si la tabla `CLUB` fuera como la siguiente, la clave primaria sería `ClubID`:

| ClubID | ClubTitle | TeacherID | TeacherLastName |
| :--- | :--- | :--- | :--- |
| 105 | Robotics | 1 | Williams |
| 202 | Taekwondo | 2 | White |
| 105 | Robotics | 1 | Williams |
| 106 | Arts and Crafts | 4 | Doe |

El `ClubTitle` depende totalmente de `ClubID`; sin embargo, el `TeacherLastName` depende de `TeacherID`, el cual no es una clave primaria. Para resolver esto, la tabla debe dividirse en dos:

**CLUBDETAILS**
| ClubID | ClubTitle | TeacherID |
| :--- | :--- | :--- |
| 105 | Robotics | 1 |
| 202 | Taekwondo | 2 |
| 106 | Arts and Crafts | 4 |

**TEACHERDETAILS**
| TeacherID | TeacherFirstName | TeacherLastName |
| :--- | :--- | :--- |
| 1 | Bobby | Williams |
| 2 | Dima | White |
| 4 | Jane | Doe |

#### Problemas de normalización
Los problemas pueden incluir duplicación de datos, datos faltantes y preocupaciones de dependencia (dependencias de datos, de claves compuestas, transitivas y multievaluadas).

Las **dependencias multievaluadas** ocurren cuando dos atributos en una tabla son independientes entre sí, pero ambos dependen de un tercero. Por ejemplo, un fabricante de coches produce dos colores (`black` y `grey`) de cada modelo cada año. Los atributos `Colour` y `ManufacturingYear` dependen de `CarModel`, pero son independientes entre sí. Esto es clave para alcanzar la **cuarta forma normal (4NF)**, que aborda redundancias no resueltas por las formas normales anteriores.

<br>

## A3.2.6 Construir una base de datos normalizada hasta 3FN para diversos escenarios de la vida real

Consideremos un sistema de gestión de bibliotecas que almacena los datos en una tabla llamada `BOOKS`:

| BookID | AuthorID | Author | Title | Pages | ProofReader |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 101 | Boris Brown | History of AI | 353 | Amanda |
| 2 | 102 | Chris Joe | The Great G | 200 | Hamilton |
| 3 | 19 | Danny Bill | Big Tonny | 190 | Juan |
| 5 | 101 | Boris Brown | Amazing Future | 399 | Amanda |

Normalizar esta base de datos a **3NF** implica:

#### 1. Normalizar a 1NF:
* Establecer `BookID` como la clave primaria.
* Dividir el autor en dos atributos diferentes: `AuthorFirstName` y `AuthorLastName`.

| BookID | AuthorID | AuthorFirstName | AuthorLastName | Title | Pages | ProofReader |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 101 | Boris | Brown | History of AI | 353 | Amanda |
| 2 | 102 | Chris | Joe | The Great G | 200 | Hamilton |
| 3 | 19 | Danny | Bill | Big Tonny | 190 | Juan |
| 5 | 101 | Boris | Brown | Amazing Future | 399 | Amanda |

#### 2. Normalizar a 2NF:
* Las entidades están en 1NF.
* No existen dependencias parciales.

`AuthorFirstName` y `AuthorLastName` dependen de `AuthorID`, mientras que `Title`, `Pages` y `ProofReader` dependen de la clave primaria (`BookID`). Por lo tanto, necesitamos dividir esta tabla de la siguiente manera:

**BOOKS**
| BookID | AuthorID | Title | Pages | ProofReader |
| :--- | :--- | :--- | :--- | :--- |
| 1 | 101 | History of AI | 353 | Amanda |
| 2 | 102 | The Great G | 200 | Hamilton |
| 3 | 19 | Big Tonny | 190 | Juan |
| 5 | 101 | Amazing Future | 399 | Amanda |

**AUTHOR**
| AuthorID | AuthorFirstName | AuthorLastName |
| :--- | :--- | :--- |
| 101 | Boris | Brown |
| 102 | Chris | Joe |
| 19 | Danny | Bill |

#### 3. Normalizar a 3NF:
* Las entidades están en 2NF.
* No existen dependencias transitivas.

El campo `ProofReader` tiene valores repetidos y no es necesariamente dependiente de forma funcional completa del `BookID`. Por lo tanto, para eliminar las dependencias no transitivas, puedes crear una nueva tabla para los correctores (*proof readers*).

**BOOKS**
| BookID | AuthorID | Title | Pages |
| :--- | :--- | :--- | :--- |
| 1 | 101 | History of AI | 353 |
| 2 | 102 | The Great G | 200 |
| 3 | 19 | Big Tonny | 190 |
| 5 | 101 | Amazing Future | 399 |

**AUTHOR**
| AuthorID | AuthorFirstName | AuthorLastName |
| :--- | :--- | :--- |
| 101 | Boris | Brown |
| 102 | Chris | Joe |
| 19 | Danny | Bill |

**PROOFREADERS**
| ProofReaderID | ProofReader |
| :--- | :--- |
| 100 | Amanda |
| 222 | Hamilton |
| 123 | Juan |

Ahora, necesitas vincular la tabla `BOOKS` con la tabla `PROOFREADERS`, por lo que se crea una nueva tabla de unión.

**BOOKS_PROOFREADERS**
| BookID | ProofReaderID |
| :--- | :--- |
| 1 | 100 |
| 2 | 222 |
| 3 | 123 |
| 5 | 100 |

> **¡Consejo de experto!**
> La normalización de bases de datos puede ser un concepto difícil de asimilar. Tómate el tiempo necesario para practicar; puedes utilizar ejercicios de exámenes anteriores o crear tus propias tablas para este propósito.
