<h1 align="center">B1.1. Enfoques del pensamiento computacional
<div align="center">

</div>

## Contenido:

- [B1.1.1. Construcción de una especificación de problema](#B111-construcción-de-una-especificación-de-problema)
- [B1.1.2. Conceptos fundamentales del pensamiento computacional](#B112-conceptos-fundamentales-del-pensamiento-computacional)
- [B1.1.3. Cómo se utilizan los conceptos fundamentales del pensamiento computacional para abordar y resolver problemas en Ciencias de la Computación](#B113-cómo-se-utilizan-los-conceptos-fundamentales-del-pensamiento-computacional-para-abordar-y-resolver-problemas-en-ciencias-de-la-computación)
- [B1.1.4. Diagramas de flujo](#B114-diagramas-de-flujo)

<br>

## B1.1.1. Construcción de una especificación de problema

### ¿Cómo aplicar una solución computacional a un problema del mundo real?

Desde sus inicios, los ordenadores han necesitado un método para indicarles cómo realizar una tarea específica. Hoy en día, esas instrucciones se proporcionan mediante un **lenguaje de programación**. Figuras como **Ada Lovelace, Charles Babbage, Alan Turing y Konrad Zuse** son reconocidas por sus contribuciones al desarrollo de la programación y los lenguajes informáticos.

Inicialmente, los lenguajes de programación se desarrollaron como una serie de pasos para **cablear** un programa concreto. Más adelante, evolucionaron hacia una serie de pasos **tecleados** en un ordenador y ejecutados directamente. Posteriormente, adquirieron características más avanzadas, como **iteraciones, ramificaciones e incluso polimorfismo, herencia** y otros principios de la **programación orientada a objetos**.

Incluso al abordar problemas sencillos, es esencial proporcionar al ordenador instrucciones precisas para que pueda llevar a cabo las tareas y resolver el problema. Sin embargo, no es posible dar instrucciones claras sobre cómo resolver un problema hasta que se haya definido claramente su **especificación**.

### ¿Qué es una especificación de problema?

Una **especificación de problema** es una explicación breve y clara de un asunto, que describe quiénes son los interesados (*stakeholders*) y por qué es importante resolver el problema. Puede incluir:

- Un **enunciado del problema** (*problem statement*)
- **Restricciones y limitaciones**
- **Objetivos y metas**
- **Especificaciones de entrada y salida**
- **Criterios de evaluación**

> [!NOTE]
> **Especificación de problema:** explicación breve y clara de un asunto, que puede incluir un enunciado del problema, restricciones y limitaciones, objetivos y metas, especificaciones de entrada y salida, y criterios de evaluación.
>
> **Stakeholder (interesado):** individuo o grupo de personas, dentro o fuera de una organización, que se ve afectado o considera que se ve afectado por un proyecto de desarrollo de software.
>
> **Enunciado del problema:** descripción del propio problema, identificación de para quién está pensada la solución, los problemas encontrados y qué debe resolverse.

### Enunciado del problema

Al definir el enunciado del problema, debe incluirse una descripción del problema en sí, para quién está diseñada la solución, los problemas encontrados y qué debe resolverse. Para comprender bien el problema, se recomienda:

- Recopilar información de literatura e investigaciones existentes.
- Utilizar experiencias previas relacionadas con el problema.
- Debatirlo con **múltiples interesados** afectados por el problema.

De esta forma, es posible identificar posibles **restricciones y limitaciones**, por ejemplo:

- Limitaciones en los **requisitos técnicos** disponibles (equipo de hardware o software).
- Aspecto **económico** (coste de producir la solución).
- **Legislación** (normativas sobre el desarrollo de software; aspectos éticos, sociales y legales).
- Problemas **operativos** (mano de obra disponible).
- **Calendario** (tiempo necesario para desarrollar e implementar la solución).

### Objetivos y metas

Una vez definidas claramente las restricciones, en colaboración con los principales interesados se deben establecer los **objetivos y metas** de la solución propuesta, identificando qué necesita resolverse y qué se quiere conseguir.

### Especificaciones de entrada y salida

Toda solución incluye alguna forma de **entrada y salida**. Conocer cómo se proporciona la entrada, qué entrada se suministra y el resultado o salida esperada ayuda a comprender el proceso necesario para alcanzar el objetivo.

La entrada puede adoptar diferentes formas:

- **Entrada directa** (mediante lectores de código de barras, escáneres OCR u OMR, o lectores MICR).
- **Entrada manual** (teclado, joystick, pantalla táctil, panel táctil o ratón, o datos introducidos manualmente por operadores humanos).
- **Entrada de datos automática** (mediante sensores: temperatura, luz, infrarrojos, presión, etc.).

Cada una tiene ventajas e inconvenientes. Por ejemplo, la **entrada manual** puede ser más barata, pero es propensa a errores, mientras que la **entrada automática** es claramente más costosa debido al hardware o software implicado, pero resulta más precisa y rápida.

En cuanto a la **salida**, esta puede clasificarse como:

- **Salida temporal** (mostrar la información en pantalla).
- **Salida permanente** (imprimir los datos).
- **Salida eléctrica o mecánica** (mediante actuadores: interruptores o relés).

Identificar los datos de entrada requeridos y la salida esperada ayuda a delinear el **flujo de datos** y a comprender cómo viajan los datos a través de la solución propuesta.

### Criterios de evaluación

Los **criterios de evaluación** constituyen el último paso en la construcción de una especificación de problema. Deben ser **claros, específicos, medibles** y estar relacionados con la funcionalidad que se pretende lograr con la solución propuesta. Esto permitirá utilizar dichos criterios para evaluar el éxito del producto en una etapa posterior.

> [!TIP]
> **Consejo clave:** la especificación de problema forma parte de los requisitos de la evaluación interna (criterio A). Se considera el punto de partida de la solución y debe servir de base para su desarrollo. Los criterios de éxito identificados en la especificación del problema se utilizarán en la planificación, el desarrollo y la evaluación del producto.

> [!TIP]
> **Consejo destacado:** los problemas de rendimiento derivados de no identificar correctamente las limitaciones, restricciones, entradas y salidas específicas de diferentes sistemas en ubicaciones geográficamente diversas pueden perjudicar a los usuarios finales y reducir la compatibilidad entre sistemas.

<br>

## B1.1.2. Conceptos fundamentales del pensamiento computacional

### Abstracción

La **abstracción** es el proceso de extraer la información esencial, descartando los datos irrelevantes, para proponer o esbozar una solución viable a un problema determinado. De esta forma, es posible diseñar **modelos simplificados** que excluyen los detalles innecesarios. Esto desempeña un papel crucial a la hora de ofrecer una solución que satisfaga los requisitos y necesidades del usuario, ya que resuelve el problema sin incluir funciones innecesarias y en menos tiempo, gracias a la reducción de la cantidad de código escrito.

> [!NOTE]
> **Abstracción:** disponer de un modelo simplificado y de mayor nivel para representar un sistema complejo. Permite centrarse en las ideas o conceptos esenciales, sin preocuparse en exceso por los detalles concretos de la implementación.

Ejemplos reales de abstracción son el diseño de un **mapa** como representación de un territorio, una **pintura** como representación de un paisaje, o un **horario**. En programación, la abstracción es un concepto importante en la **programación orientada a objetos**. Se utiliza para ocultar la complejidad al usuario mediante:

- La **abstracción de entidades de datos** (ocultando entidades de datos a través de una estructura de datos, reduciendo el conjunto de datos a una versión simplificada del todo).
- La **ocultación de la implementación subyacente de un proceso** (los programadores no necesitan conocer los detalles de cómo están implementadas las subrutinas, ni qué otras subrutinas invocan, simplemente pueden utilizarlas para cumplir su propósito).

Al utilizar la abstracción:

- Se **reduce el tiempo** necesario para crear un programa.
- El programa se vuelve **más pequeño**, por lo que requiere menos espacio en memoria y se reducen los tiempos de descarga.
- Aumenta la **satisfacción del cliente**, ya que sus requisitos se cumplen sin funciones adicionales innecesarias.

> [!TIP]
> **TdC (Teoría del Conocimiento):** ¿Qué cuenta como conocimiento?
>
> El mapa como abstracción del territorio: un mapa no es el territorio real que representa, sino una representación esquemática de un área, que incluye ciertos elementos y excluye otros. El mapa del metro de Londres fue diseñado en 1933 como un modelo simplificado de la realidad, que informa al viajero de cómo desplazarse entre estaciones, pero excluye muchos otros detalles y no ofrece una representación precisa del espacio real. Conocer el mapa no implica conocer realmente el territorio, del mismo modo que conocer el nombre de las cosas en distintos idiomas no refleja un conocimiento real sobre esas cosas.

### Diseño algorítmico

Antes de comenzar a escribir código, es necesario analizar e identificar los requisitos del problema y, a continuación, comprender los pasos lógicos necesarios para resolverlo. Una vez comprendidos con claridad los requisitos, el siguiente paso consiste en diseñar una posible solución. Un enfoque eficaz para lograrlo es crear un **algoritmo**, lo que implica diseñar soluciones paso a paso con resultados predecibles.

Un **algoritmo** es un conjunto estructurado de instrucciones secuenciales diseñado para abordar y resolver un problema.

> [!NOTE]
> **Algoritmo:** secuencia finita de instrucciones que debe seguirse paso a paso para resolver un problema.

Consideremos el siguiente problema:

*"Se requiere que un usuario proporcione dos números enteros. Construye un programa que calcule la suma de ambos números y la muestre."*

El algoritmo correspondiente sería:

1. Pedir al usuario que introduzca un número.
2. Almacenar ese número.
3. Pedir al usuario que introduzca otro número.
4. Almacenar este nuevo valor.
5. Sumar ambos números.
6. Almacenar el resultado.
7. Mostrar el resultado.

Estos pasos deben ser muy específicos y estar en el orden correcto para poder resolver el problema. Al aplicar el diseño algorítmico, se desarrollan habilidades de **pensamiento algorítmico** que ayudan a crear técnicas eficientes de resolución de problemas, mediante algoritmos estructurados y sistemáticos.

> [!TIP]
> Al esbozar algoritmos, asegúrate de que las instrucciones sean muy específicas, claras y estén en el orden correcto. No seguir el orden requerido suele provocar soluciones incorrectas o distintos errores. Por ejemplo, si necesitas calcular la media de tres números, establecer el valor de la variable `sum` en 0 **después** de haber almacenado la suma de los tres valores y, a continuación, intentar dividir por 3, produciría un error.

### Descomposición

La **descomposición** consiste en dividir problemas complejos en partes más pequeñas y manejables. Tras diseñar soluciones para esos problemas más pequeños, estas pueden combinarse para construir la solución final del problema complejo. Este concepto favorece la **modularidad**, permitiendo que varios programadores o expertos colaboren y trabajen simultáneamente en la resolución del problema.

> [!NOTE]
> **Descomposición:** dividir problemas complejos en partes más pequeñas y manejables.
>
> **Reconocimiento de patrones:** identificación de similitudes en los detalles de los problemas.

En programación, la descomposición se utiliza a menudo para estructurar la solución, diseñando varios métodos o funciones.

> [!WARNING]
> **Error común:** los estudiantes no siempre utilizan la terminología de forma adecuada y competente, y a veces abordan las preguntas ofreciendo un conocimiento superficial general, lo cual no obtiene la puntuación máxima.
>
> A menudo, los estudiantes definen la "descomposición" como dividir un programa en subprogramas más pequeños. Esto no es correcto, ya que, en la fase en la que ocurre la descomposición, todavía no se ha creado ningún programa; por tanto, lo que se está dividiendo en partes más pequeñas y manejables es el **problema**, no el programa.

### Reconocimiento de patrones

El **reconocimiento de patrones** consiste en identificar similitudes en los detalles de los problemas. Esto simplifica el proceso de encontrar una solución, al identificar patrones y centrarse en reutilizar las soluciones propuestas para resolver esas similitudes. Esto implica desarrollar **código reutilizable** en forma de funciones o procedimientos, reutilizar código existente que ya ha sido probado, y favorecer el uso de la **modularidad**, lo que reduce el tiempo de desarrollo.

<br>

## B1.1.3. Cómo se utilizan los conceptos fundamentales del pensamiento computacional para abordar y resolver problemas en Ciencias de la Computación

El **pensamiento computacional** no es programación, y no consiste en pensar como un ordenador, sino en pensar como un **científico de la computación**. Es un conjunto de técnicas disponibles para la resolución de problemas. Esto proporciona las habilidades necesarias para esbozar de forma eficiente una especificación de problema; analizar, comprender y simplificar el problema; e identificar y elegir soluciones óptimas para distintos problemas.

> [!NOTE]
> **Pensamiento computacional:** conjunto de técnicas disponibles para la resolución de problemas; sus conceptos fundamentales son la abstracción, la descomposición, el pensamiento algorítmico y el reconocimiento de patrones.

Los conceptos fundamentales del pensamiento computacional —abstracción, descomposición, pensamiento algorítmico y reconocimiento de patrones— pueden aplicarse para resolver problemas del mundo real, por ejemplo: desarrollo de software, análisis de datos, aprendizaje automático, diseño de bases de datos y problemas de seguridad de redes.

En cada una de estas áreas, todos los conceptos fundamentales son igualmente importantes:

- **Desarrollo de software:** no es posible crear un programa sin antes comprender el problema, hacer abstracción de los detalles innecesarios, encontrar patrones repetidos y diseñar algoritmos eficientes. Sin estos pasos, el software resultante podría carecer de precisión o no ser todo lo eficiente que debería.
- **Desarrollo de videojuegos:** la abstracción se emplea cuando se ofrece a los jugadores una serie de pistas, algunas de las cuales están pensadas para despistarlos. Los jugadores deben descartar esas pistas y centrarse en los detalles importantes.
- **Programación:** los lenguajes de programación ofrecen bibliotecas con funciones y métodos que los programadores pueden usar. El programador hace abstracción de cómo se escribieron esas funciones, centrándose en utilizarlas correctamente en su código.
- **Análisis de datos:** el pensamiento computacional se utiliza para automatizar tareas repetitivas, predecir tendencias de mercado y mejorar el servicio al cliente. Los analistas de datos identifican patrones (por ejemplo, productos populares para un grupo de personas, tareas repetitivas, quejas frecuentes de clientes) y aplican el pensamiento algorítmico para proponer soluciones viables y dividir los problemas en pasos más simples, ahorrando horas de trabajo adicional cada semana.
- **Aprendizaje automático:** el reconocimiento de patrones es un concepto importante, utilizado para clasificar datos encontrando patrones en grandes volúmenes de información, por ejemplo, para predecir el comportamiento de compra a partir de hábitos de consumo. También puede usarse para identificar las habilidades necesarias para ser un buen jugador de fútbol, analizando grabaciones de vídeo para encontrar automáticamente patrones en el comportamiento de jugadores profesionales. La misma tarea puede recurrir a la abstracción para excluir información irrelevante de los vídeos, y a algoritmos para fomentar esas habilidades en nuevos jugadores durante sus sesiones de entrenamiento virtual.
- **Diseño de bases de datos:** la abstracción permite identificar qué fuentes de datos son relevantes y cuáles pueden descartarse. La descomposición se usa para diseñar bases de datos relacionales, dividiendo el problema complejo en otros más pequeños. Las entidades pueden representarse como tablas, y las relaciones entre ellas se muestran gráficamente.
- **Normalización de bases de datos:** el reconocimiento de patrones puede usarse para garantizar que no existan grupos repetidos de atributos, y el diseño algorítmico ayuda a esbozar la estructura de las tablas e identificar la lógica de las relaciones establecidas entre ellas.
- **Seguridad de redes:** para resolver problemas de seguridad de redes, la abstracción permite generalizar modelos de seguridad complejos; la descomposición se usa para dividir los ecosistemas de ciberseguridad en modelos que permitan identificar claramente sus funciones de seguridad; el reconocimiento de patrones sirve para esbozar formas de identificar y clasificar posibles amenazas a la red; y el diseño algorítmico se usa para proponer instrucciones claras, paso a paso, sobre cómo abordar esos riesgos en situaciones similares.

> [!TIP]
> **TdC (Teoría del Conocimiento):** El conocimiento y la IA
>
> La inteligencia artificial mejora rápidamente y puede lograr objetivos que antes se consideraban imposibles. Las máquinas pueden detectar patrones a una velocidad asombrosa, tomar decisiones, generar resultados sorprendentes e incluso aprender cosas nuevas. Pero, ¿cómo acceden a esa amplia variedad de datos? ¿Qué papel juega nuestra huella digital en la mejora de las técnicas de aprendizaje automático? Los sistemas que predicen el comportamiento humano podrían dar lugar a discriminación, por lo que cabe preguntarse cómo definir éticamente los límites del conocimiento creado con ayuda de la tecnología.

<br>

## B1.1.4. Diagramas de flujo

Los **diagramas de flujo** se utilizan para diseñar algoritmos y describirlos mediante diagramas. Permiten seguir los cambios de las variables, mostrar el flujo de ejecución y determinar la salida esperada de un algoritmo.

### Símbolos estándar de los diagramas de flujo

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/tree/9cf9b083d9e696a47795b13ecc833a77970fafc6/B1.%20Pensamiento%20computacional/images/symbols.png" alt="Símbolos estándar de los diagramas de flujo" width="450" height="auto"/>
    <p><em>Figura 1: Símbolos estándar de los diagramas de flujo. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

| Símbolo | Nombre | Descripción |
|---------|--------|-------------|
| Terminador | **Terminador** | Inicio o fin del proceso |
| Paralelogramo | **Entrada/salida** | Entrada o salida de datos |
| Rectángulo | **Proceso** | Acción, como un cálculo o una asignación |
| Rombo | **Decisión** | Decisiones verdadero/falso o sí/no (sentencias de selección) |
| Flecha | **Línea de flujo** | Dirección del flujo de datos entre formas |
| Círculo pequeño | **Conector** | Continuación de un flujo a través de varias páginas o diagramas |

### Ejemplo práctico

Consideremos el siguiente problema:

*"Solicita al usuario que introduzca dos números por teclado. Muestra su media."*

Para resolver el problema, se identifican la entrada, los procesos y la salida:

- **Entrada:** los dos números (`a`, `b`)
- **Salida:** la media de los dos números (`avg`)
- **Procesos:** calcular la suma, calcular la media.

<div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/tree/9cf9b083d9e696a47795b13ecc833a77970fafc6/B1.%20Pensamiento%20computacional/images/flowchart1.png" alt="Flowchart 1 resolución" width="450" height="auto"/>
    <p><em>Figura 2: Diagrama de flujo. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

### Diagramas de flujo con selección

Los diagramas de flujo pueden volverse algo más complejos al incluir **selección** o **iteración**. Por ejemplo, el diagrama de flujo correspondiente a un algoritmo que muestra el mayor de dos números introducidos requiere sentencias de selección (decisión).

<div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/tree/9cf9b083d9e696a47795b13ecc833a77970fafc6/B1.%20Pensamiento%20computacional/images/flowchart2.png" alt="Flowchart 2 resolución" width="450" height="auto"/>
    <p><em>Figura 2: Diagrama de flujo con selección. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

Para comprobar dicho algoritmo, se podría probar con datos de prueba distintos, como **7 y −3**. Para hallar la salida esperada, se puede dibujar y rellenar una **tabla de trazado**, que incluye los cambios de las variables, las decisiones tomadas y las salidas esperadas.


#### Tabla de trazado (ejemplo con a = 7, b = −3)

| a | b | max | a > b | output |
|---|---|-----|-------|--------|
| 7 | −3 | | | |
| 7 | −3 | | TRUE | |
| 7 | −3 | 7 | TRUE | El valor mayor es 7 |

Para trazar la tabla y llegar a la salida final, es necesario recorrer el diagrama de flujo siguiendo el flujo de datos indicado por las flechas:

1. En primer lugar, ocurre la **entrada**: `a` toma el valor 7 y `b` toma el valor −3.
2. A continuación, se comprueba si el valor almacenado en `a` es mayor que el valor almacenado en `b` (condición verdadera, por lo que `max` toma el valor de `a`, es decir, 7).
3. Finalmente, se muestra la salida: *"El valor mayor es 7"*.

No es necesario insertar cada nuevo valor en una línea distinta de la tabla; esto se hace únicamente para poder apreciar el orden de ejecución de las operaciones. Las tablas de trazado se explorarán con más detalle en el bloque **B2. Programación**.

> [!WARNING]
> **Error común:** los estudiantes a menudo olvidan etiquetar las ramas de los símbolos de decisión al dibujar diagramas de flujo. Una rama sin etiquetar no permite identificar qué proceso se ejecuta cuando la condición se evalúa como **verdadera (Sí)** y cuál se ejecuta cuando se evalúa como **falsa (No)**. Además, hay que asegurarse de que todas las líneas de flujo estén conectadas y ninguna quede sin conexión a una forma.
