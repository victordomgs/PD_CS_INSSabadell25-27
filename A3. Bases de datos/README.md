# A3. Bases de datos

Nivel Medio: 11 horas.

## Pregunta de orientación
¿Cuáles son los principios, estructuras y operaciones que constituyen la base de los sistemas de bases de datos?

## A3.1 Fundamentos de las bases de datos

### A3.1.1 Explicar las características, ventajas y limitaciones de una base de datos relacional

- Características: claves compuestas, claves externas, claves primarias, relaciones y tablas.
- Ventajas de las bases de datos: soporte comunitario, control de la concurrencia, integridad de los datos, integridad de los datos, recuperación de datos, reducción de la duplicación de datos, reducción de la redundancia, procesamiento fiable de las transacciones, escalabilidad, características de seguridad.
- Limitaciones de las bases de datos: problemas de escalabilidad de los “macrodatos”, complejidad del diseño, tratamiento jerárquico de los datos, esquema rígido, desajuste de impedancia objetorelacional y tratamiento de datos no estructurados.

## A3.2 Diseño de bases de datos

### A3.2.1 Describir el esquema de una base de datos

- Esquema conceptual, esquema lógico, esquema físico.
- Definiciones abstractas de la estructura y organización de los datos a diferentes niveles.

### A3.2.2 Elaborar diagramas ER

- Importancia de los diagramas de entidad-relación (ERD) en la elaboración de diseños de bases de datos organizados, eficientes y adaptados a aplicaciones específicas.
- Relaciones entre las diferentes entidades de datos dentro de una base de datos.
- Funciones de la cardinalidad y la modalidad en la definición de relaciones en los ERD.

### A3.2.3 Resumir los distintos tipos de datos utilizados en las bases de datos relacionales

- Importancia de la coherencia de los tipos de datos.
- Efectos potenciales de elegir un tipo de datos inapropiado.

### A3.2.4 Elaborar tablas para bases de datos relacionales

- Relación entre tablas mediante claves primarias, claves externas, claves compuestas y claves concatenadas.
- Importancia de unas tablas bien definidas para garantizar la integridad de los datos.

### A3.2.5 Explicar la diferencia entre formas normales

- Primera forma normal (1NF), segunda forma normal (2NF) y tercera forma normal (3NF).
- Términos: atomicidad, identificación única, dependencias funcionales, dependencias de clave parcial, dependencias no clave/transitivas.
- Los problemas de normalización pueden abarcar la duplicación de datos, los datos que faltan y una serie de problemas de dependencia, incluidas las dependencias de datos, las dependencias de claves compuestas, las dependencias transitivas y las dependencias multivaluadas.

### A3.2.6 Elaborar una base de datos normalizada a 3NF para una variedad de situaciones del mundo real

- Algunos ejemplos pueden ser la gestión de bibliotecas, hospitales, plataformas de comercio electrónico, administración de colegios, administración de personal, administración de existencias, denuncias policiales.

### A3.2.7 Evaluar la necesidad de desnormalizar las bases de datos

- Ventajas y desventajas de normalizar y desnormalizar las bases de datos.
- Situaciones en las que la desnormalización puede mejorar el rendimiento, especialmente en aplicaciones de lectura intensiva.
- Equilibrio entre las estructuras de consulta sencillas y el riesgo de redundancia de datos en los esquemas desnormalizados.

## A3.3 Programación de bases de datos

### A3.3.1 Resumir las diferencias entre los tipos de lenguaje de datos en SQL

- Los tipos de lenguaje de datos deben incluir el lenguaje de definición de datos (DDL) y el lenguaje de manipulación de datos (DML).
- Declaraciones SQL para definir estructuras de datos o manipular datos.

### A3.3.2 Elaborar consultas entre dos tablas en SQL

- Las consultas deben incluir uniones, operadores relacionales, filtrado, cotejo de patrones y ordenación de datos.
- Comandos SQL: SELECT, DISTINCT, FROM, WHERE, BETWEEN, ORDER BY, GROUP BY, HAVING, ASC, DESC, JOIN, LIKE con comodín %, AND, OR, NOT (nota: la sintaxis puede variar en los distintos sistemas de bases de datos).

### A3.3.3 Explicar cómo puede utilizarse SQL para actualizar los datos de una base de datos

- Insertar nuevos registros (INSERT INTO), modificar datos (UPDATE SET), eliminar datos (DELETE).
- Repercusiones para el rendimiento de la actualización de datos en columnas indexadas, y la posible necesidad de reconstruir o reorganizar los índices tras modificaciones significativas de los datos.

### Preguntas transversales

- ¿Qué procesos son necesarios para almacenar datos en estructuras de bases de datos de modo que puedan utilizarse en el aprendizaje automático (A4)?
- ¿En qué se diferencia la programación de bases de datos en SQL de la programación computacional en un lenguaje de alto nivel (B2)?
- ¿En qué medida la eficacia de una base de datos distribuida viene determinada por la red que conecta las distintas tablas (A2)?
- ¿Cómo podría aplicarse el aprendizaje automático a las bases de datos (A4)?
- ¿Cómo interactúan los lenguajes de programación con las bases de datos para almacenar, recuperar y manipular datos (B2)?
