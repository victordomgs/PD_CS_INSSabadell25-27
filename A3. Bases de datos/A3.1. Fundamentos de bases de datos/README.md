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
