<h1 align="center">A3.1. Fundamentos de bases de datos
<div align="center">

</div>

## Contenido:

- [A3.1.1 Explicar las características, beneficios y limitaciones de una base de datos relacional](#A311-explicar-las-caracteríssticas-beneficios-y-limitaciones-de-una-base-de-datos-relacional)   

<br>

## A3.1.1 Explicar las características, beneficios y limitaciones de una base de datos relacional

### Características

Una base de datos se refiere a una colección organizada de información o datos estructurados a los que se puede acceder de diferentes maneras. Normalmente, una base de datos se almacena electrónicamente para permitir la rápida recuperación y manipulación de los datos. Existen diferentes tipos de bases de datos, pero el enfoque aquí será en las bases de datos relacionales.

- **Base de datos:** una colección organizada de información o datos estructurados a los que se puede acceder de diferentes maneras.
- **Tabla:** una estructura de filas y columnas para almacenar un grupo de datos similares.
- **Entidad:** un objeto animado o inanimado del cual se pueden almacenar datos que lo describan; por ejemplo: una persona, una silla o un avión.
- **Tupla:** una instancia de una entidad; una fila en una tabla.
- **Registro:** una instancia de una entidad; una fila en una tabla.
- **Atributo:** un elemento de dato o una característica de una entidad; una columna en una tabla.

Las bases de datos relacionales se han utilizado predominantemente desde 1980. Los datos en una base de datos relacional se organizan como un conjunto de tablas compuestas por columnas y filas.

### Tablas

La tabla se utiliza para describir entidades. Una entidad se refiere a una cosa viva o no viva sobre la cual se pueden guardar datos descriptivos, como una persona, una silla o un avión.

Cada fila, también llamada tupla, incluirá un registro o una instancia de una entidad; por ejemplo, una persona específica, una silla específica o un avión específico. Cada columna, también llamada "campo" o atributo, incluirá un dato o característica de la entidad, como la edad o el nombre de una persona, el color de una silla, el modelo de un avión, etc.

Considera el siguiente ejemplo:

#### AEROPLANE (AVIÓN)
| Model | Manufacturer | PhysicalClassEngine | NoOfEngines |
| :--- | :--- | :--- | :--- |
| Rockwell Commander 112 | Rockwell | Piston | 1 |
| Airbus A319 Neo | Airbus | Jet | 2 |
| Boeing 747-100 | Boeing | Jet | 4 |
| Boeing 777-8 | Boeing | Jet | 2 |
| Airbus A400M Atlas | Airbus | Turboprop | 4 |
| Boeing 747-100 | Boeing | Jet | 4 |

En el ejemplo anterior, el nombre de la tabla es AEROPLANE (esta es la entidad) y hay seis registros o tuplas (filas en la tabla, excluyendo el encabezado) y cuatro atributos o campos (columnas).

### Clave primaria (Primary key)

Si se desea identificar de forma única un registro en esta tabla, se debe añadir un campo adicional. Esto es necesario ya que todos los campos actuales tienen valores repetidos, por lo que no pueden usarse para identificar un registro con precisión. Es posible que una compañía tenga dos aviones del mismo tipo, fabricados por la misma empresa, con el mismo tipo de motor, etc.

Por lo tanto, al añadir un campo extra para identificar únicamente cada registro, la tabla se vería así:

#### AEROPLANE
| PlaneID | Model | Manufacturer | PhysicalClassEngine | NoOfEngines |
| :--- | :--- | :--- | :--- | :--- |
| **A01** | Rockwell Commander 112 | Rockwell | Piston | 1 |
| **A02** | Airbus A319 Neo | Airbus | Jet | 2 |
| **A03** | Boeing 747-100 | Boeing | Jet | 4 |
| **A04** | Boeing 777-8 | Boeing | Jet | 2 |
| **A05** | Airbus A400M Atlas | Airbus | Turboprop | 4 |
| **A06** | Boeing 747-100 | Boeing | Jet | 4 |

El campo `PlaneID` es único para cada registro (no tiene duplicados) y esto se denomina clave primaria.

- **Clave primaria:** un campo que identifica de forma única un registro en una tabla.
- **Clave foránea:** un atributo en una tabla que hace referencia a la clave primaria de otra tabla.

### Clave foránea (Foreign key)

Imagina que quieres registrar datos sobre vuelos específicos en un aeropuerto. La tabla AEROPLANE solo proporciona información sobre los aviones. Por lo tanto, necesitarás crear una nueva tabla para registrar los detalles de los vuelos.

#### FLIGHTS (VUELOS)
| FlightID | Departure | Destination | PlaneID (FK) | FlightDate | DeptTime | ArrivalTime |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| LG8903 | LUX | OTP | A03 | 01/07/25 | 17:00 | 20:20 |
| OS864 | CAI | VIE | A04 | 15/01/25 | 16:45 | 19:20 |
| GB961 | LHR | ZRH | A03 | 25/02/25 | 8:40 | 11:35 |

En esta tabla, el `FlightID` actúa como clave primaria.

Las dos tablas, FLIGHTS y AEROPLANE, están estableciendo una relación, ya que el PlaneID de la tabla AEROPLANE se utiliza en la tabla FLIGHTS para identificar qué tipo de avión se está usando para un vuelo específico. Sin embargo, el `PlaneID` ya no es una clave primaria en la tabla FLIGHTS, ya que tiene valores repetidos; aquí actúa como clave foránea.

Una clave foránea es un atributo o conjunto de atributos en una tabla que hace referencia a la clave primaria en otra tabla.

### Clave compuesta (Composite key)

Si introduces una tercera tabla para registrar a los pilotos en el vuelo, podría verse así:

| FlightID (PK/FK) | PilotID (PK/FK) |
| :--- | :--- |
| LG8903 | P500 |
| OS864 | P104 |
| GB961 | P500 |

El `FlightID` se vincula con la tabla FLIGHTS y el PilotID se vincula con la tabla PILOTS (suponiendo que existe también una tabla PILOTS que registra los detalles de los pilotos). En la tabla PILOTFLIGHT, no hay una clave primaria individual. Una solución podría ser usar una clave compuesta, formada por los dos atributos `FlightID` y `PilotID`.

- **Clave compuesta:** un conjunto de atributos que forman una clave primaria.
- **Relación:** un vínculo establecido entre diferentes tablas, donde la clave foránea en una tabla hace referencia a la clave primaria en otra tabla.

Una clave compuesta es un conjunto de atributos que forma una clave primaria para proporcionar un identificador único para una tabla.


### Relaciones

Relaciones
Una **relación** se crea cuando existe una asociación lógica entre dos o más tablas de una base de datos, en la que una tabla contiene una o más claves foráneas (o ajenas) que hacen referencia a las claves primarias de las otras tablas. Estas relaciones permiten que las bases de datos relacionales dividan y almacenen los datos en tablas separadas, manteniendo al mismo tiempo la conexión entre sus elementos.

Para garantizar que los datos sean siempre precisos, accesibles y coherentes, las bases de datos relacionales siguen ciertas reglas de integridad. Por ejemplo, la regla de integridad referencial evita que los usuarios o las aplicaciones introduzcan datos inconsistentes. Se trata de una restricción que asegura que ninguna tabla contenga valores de una clave foránea que no coincidan con su clave primaria correspondiente. En otras palabras, garantiza que una clave foránea siempre haga referencia a un registro que existe en otra tabla. Al aplicar restricciones de integridad referencial, los datos se mantienen consistentes durante operaciones como la inserción, eliminación y modificación de tuplas.

Existen varios tipos de relaciones:

- Uno a uno (1:1)
- Uno a muchos (1:n)
- Muchos a uno (n:1)
- Muchos a muchos (n:m)

#### Relaciones uno a uno (1:1)

Cuando existe una relación uno a uno entre dos tablas, significa que un registro de una tabla está asociado exactamente con un registro de otra tabla: la clave primaria se corresponde con uno o ningún dato en la otra tabla. Por ejemplo, cada miembro del personal de una escuela tiene un único ID de empleado; cada país tiene exactamente una ciudad capital; o un usuario en una plataforma de redes sociales tiene un único perfil de usuario. Estos son tipos de relaciones muy poco comunes que no encontrarás con frecuencia al trabajar con bases de datos.

#### Relaciones uno a muchos (1:n)

Este es un tipo de relación utilizado frecuentemente y se refiere a que un registro en una tabla está asociado con uno o más registros en otra tabla: la clave foránea de una tabla hace referencia a la clave primaria de otra tabla. Ejemplos de relaciones uno a muchos son: un profesor imparte muchas asignaturas; un turista visita muchos países; una persona posee muchas propiedades; una persona tiene muchas cuentas bancarias.

#### Relaciones muchos a uno (n:1)

Las relaciones muchos a uno son similares a las de uno a muchos, pero difieren en su direccionalidad. La disponibilidad de la entidad y el lado de la relación en el que se encuentre determinan si es una relación uno a muchos o muchos a uno. Por ejemplo, si un profesor imparte varias asignaturas, la relación entre los profesores y las asignaturas es de uno a muchos, mientras que la relación entre las asignaturas y los profesores es de muchos a uno. Ejemplos de relaciones muchos a uno son: muchos estudiantes se matriculan en un solo curso; muchas personas trabajan para una sola empresa; hay muchas galaxias en el universo.

#### Relaciones muchos a muchos (n:m)

Este tipo de relación aparece cuando múltiples registros de una tabla tienen relación con múltiples registros de otra tabla. Ejemplos de relaciones muchos a muchos son: muchos clientes compran muchos productos; muchos actores actúan en muchas películas.

El problema con una relación muchos a muchos es que un atributo de clave foránea solo puede contener un único valor y, por lo tanto, no puede manejar las múltiples referencias requeridas. Para implementar este tipo de relaciones en bases de datos relacionales, se debe introducir una entidad de enlace (o tabla intermedia). Esto significa que se crearán dos relaciones uno a muchos: una entre la primera tabla y la tabla de enlace, y otra entre la segunda tabla y la tabla de enlace.

En el ejemplo anterior, cuando se quería conectar la tabla VUELOS con la tabla PILOTOS, se introdujo una tercera tabla llamada PILOTOVUELO. De este modo, se estableció una relación de uno a muchos entre las tablas VUELOS y PILOTOVUELO, y otra relación de uno a muchos entre las tablas PILOTOS y PILOTOVUELO. Esto se hace porque una relación muchos a muchos no puede representarse físicamente en una base de datos.

Aquí tienes la traducción de los beneficios de las bases de datos relacionales al castellano:

### Beneficios de las bases de datos relacionales

#### Soporte de la comunidad

Las bases de datos relacionales existen desde la década de 1970 y son el modelo más aceptado. Por ello, existen muchísimas comunidades en línea capaces de brindar soporte y orientación en su construcción, mantenimiento y resolución de problemas.

#### Control de concurrencia

El control de concurrencia es un componente crucial del sistema de gestión de bases de datos (DBMS). Gestiona operaciones simultáneas sin que entren en conflicto entre sí, y su propósito es mantener la integridad, consistencia y el aislamiento de los datos cuando múltiples usuarios o aplicaciones acceden a la base de datos al mismo tiempo.

#### Consistencia de datos

La consistencia de datos se refiere a que los datos permanezcan en un estado coherente de principio a fin, reforzando su integridad. Esto significa que todas las copias o instancias de los datos son iguales en todos los sistemas y bases de datos. En las bases de datos relacionales, cada dato se almacena en un solo lugar y todos los datos relacionados se guardan juntos en la misma tabla. Esto garantiza que todos los usuarios tengan acceso a información precisa y actualizada.

#### Integridad de datos

La integridad de datos se refiere a la exactitud, completitud y consistencia de los datos a lo largo de su ciclo de vida. Asegura que los datos no hayan sido manipulados o alterados de forma no autorizada. Para garantizarla, se pueden utilizar técnicas de validación de datos.

#### Recuperación de datos

El proceso de recuperar datos de una base de datos relacional es eficiente y flexible. El lenguaje SQL permite escribir consultas complejas para obtener exactamente la información necesaria, utilizando sentencias `SELECT`, `JOIN`, cláusulas `WHERE` y más. Los usuarios también pueden crear consultas ad hoc para recuperar datos sin necesidad de programas o informes predefinidos.

#### Reducción de la duplicación de datos

Las bases de datos relacionales aseguran el uso de campos comunes para vincular tablas y hacer coincidir registros, sin tener que duplicar todos los detalles varias veces. Identificar y eliminar datos duplicados reduce la cantidad de almacenamiento necesaria.

#### Reducción de la redundancia

La redundancia de datos se refiere al almacenamiento de los mismos datos en múltiples ubicaciones al mismo tiempo. Esto puede dar lugar a inconsistencias, actualizaciones parciales y duplicaciones innecesarias. Las bases de datos relacionales permiten reducir la redundancia mediante la normalización (organizar los datos en varias tablas y crear relaciones entre ellas para evitar grupos repetidos de atributos, asegurando que los atributos que no son clave sean independientes).

#### Procesamiento de transacciones fiable

Una transacción es una secuencia de acciones realizadas en una base de datos que se considera como una única unidad (como insertar, eliminar o actualizar datos). Es una unidad de trabajo o acción lógica, independiente de otras transacciones. Una transacción **o se ejecuta en su totalidad o no se ejecuta en absoluto**. Las transacciones garantizan la integridad y fiabilidad de los datos.

#### Escalabilidad

La escalabilidad se refiere a la capacidad de una base de datos para manejar cantidades crecientes de datos, usuarios y tipos de solicitudes sin sacrificar el rendimiento. Las bases de datos relacionales suelen tener **escalabilidad vertical**, lo que significa que permiten añadir más recursos (CPU, RAM, espacio en disco) a los sistemas existentes, lo cual es un enfoque más barato, fácil y rápido para gestionar incrementos de carga.

#### Funciones de seguridad

Las bases de datos relacionales aumentan la seguridad al controlar el acceso a los datos almacenados, garantizando que solo los usuarios autorizados puedan interactuar con ellos. Permiten la asignación de cuentas de usuario únicas con permisos específicos basados en sus roles y responsabilidades, así como diferentes "vistas" de las tablas según los derechos de acceso.

### Limitaciones de las bases de datos relacionales

#### Problemas de escalabilidad con Big Data

Las bases de datos relacionales pueden ser más difíciles de escalar a medida que aumentan el tamaño y la complejidad de los datos. El rendimiento puede disminuir al manipular grandes conjuntos de datos (**escalado horizontal**) o al lidiar con consultas complejas; las uniones (*joins*) entre tablas pueden volverse lentas y las estrategias de indexación pueden ser difíciles de optimizar.

#### Complejidad de diseño

Las bases de datos relacionales requieren mucha estructura y planificación para diseñar las tablas y sus relaciones de manera que se ajusten correctamente a los requisitos del sistema.

#### Gestión de datos jerárquicos

Almacenar datos jerárquicos en bases de datos relacionales es un reto debido al desajuste entre la estructura jerárquica y la naturaleza tabular de estas bases de datos. Incluso si se utiliza una estrategia como el **modelo de lista de adyacencia** (donde cada registro contiene una referencia a su registro padre, formando una estructura de árbol, como una tabla de empleados con un campo que referencia al ID del gerente), resulta complicado recuperar y recorrer las jerarquías, especialmente en grandes conjuntos de datos, o reordenar nodos y realizar consultas en los subárboles creados.

#### Esquema rígido

Las bases de datos relacionales tienen un esquema predefinido (la estructura de los datos y cómo se almacenarán). Definir este esquema puede ser un desafío, ya que no es fácil predecir la estructura de los datos de antemano, y modificarla más adelante es complicado. Cuando se trata de cambiar la estructura de la base de datos, actualizar el esquema es un proceso costoso en tiempo y complejo.

#### Desajuste de impedancia objeto-relacional

El "desajuste de impedancia" (object-relational impedance mismatch) se refiere a las dificultades que surgen cuando un programa escrito en un lenguaje de **programación orientada a objetos (POO)** utiliza bases de datos relacionales. Una de las mayores discrepancias es la diferencia en los tipos de datos. Los modelos relacionales no permiten el uso de atributos por referencia (punteros), mientras que los lenguajes de POO se basan en este comportamiento. No existe una forma clara de traducir todos los conceptos de POO a bases de datos relacionales o viceversa; por ejemplo, no hay una forma directa de traducir la herencia a un concepto de base de datos relacional.

#### Gestión de datos no estructurados

Los datos no estructurados son colecciones de datos donde un registro difiere de otro. Al no poder identificar campos o atributos comunes para los registros, resulta imposible diseñar un esquema para dichos datos que permita representarlos en una base de datos relacional.
