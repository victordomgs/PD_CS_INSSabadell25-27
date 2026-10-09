<h1 align="center">B2.1. Fundamentos de la programación
<div align="center">

</div>

## Contenido:

- [B2.1.1. Variables](#B211-variables)
- [B2.1.2. Manipulación de subcadenas (substrings)](#B212-manipulación-de-subcadenas-substrings)
- [B2.1.3. Gestión de excepciones](#B213-gestión-de-excepciones)
- [B2.1.4. Técnicas de depuración](#B214-técnicas-de-depuración)

<br>

## B2.1.1. Variables

### Convertir un algoritmo en código

Convertir un algoritmo en código implica utilizar **variables** para almacenar y manipular datos, **bucles** para repetir instrucciones y **estructuras de selección** para tomar decisiones sobre el camino a seguir para completar una tarea. Los conceptos importantes a comprender al desarrollar un programa son:

- **Almacenamiento de datos**: el uso de variables y constantes.
- **Operadores**: utilizados para manipular y comparar datos (operadores matemáticos y lógicos).
- **Estructuras de selección/bifurcación**: utilizadas para construir sentencias de decisión.
- **Iteración**: bucles para repetir bloques de código, tanto basados en contador como en condición.

> [!NOTE]
> **Variable:** una posición de memoria designada que almacena un valor que puede cambiar durante la ejecución de un programa.
>
> **Bucle / iteración:** una repetición.
>
> **Selección:** una sentencia condicional o de decisión, por ejemplo, sentencias IF o CASE.
>
> **Almacenamiento de datos:** almacenamiento de datos dentro de la memoria primaria o secundaria.
>
> **Operador:** un carácter que representa una operación matemática, aritmética o lógica.
>
> **Identificador:** un token léxico que nombra las entidades del lenguaje.
>
> **Declaración:** una construcción del lenguaje que especifica las propiedades de un identificador.
>
> **Inicialización:** asignar un valor inicial a una estructura de datos.

### Almacenamiento de datos: uso de variables

Imagina un comercial que recibe un **salario base fijo**, complementado con una **bonificación** ligada al rendimiento de ventas mensual. Esta bonificación fluctúa de un mes a otro, por lo que puede caracterizarse como **variable** en el tiempo. En campos como las Matemáticas y la Informática, el término “variable” se utiliza para representar este tipo de valores dinámicos.

Una variable tiene un **identificador** (nombre) y un **valor actual**. Cada variable solo puede contener un valor a la vez. Antes de ser utilizada, una variable debe ser **declarada** e **inicializada**. La declaración de una variable consiste en especificar su tipo de dato, mientras que la inicialización consiste en asignarle un valor inicial.

> [!TIP]
> En Python no es necesario declarar las variables utilizadas. Por tanto, a efectos de evaluación, pueden mencionarse mediante un **comentario** (un comentario sirve para dar explicaciones sobre el código o notas al desarrollador, pero se elimina en la fase de análisis léxico, ya que no es necesario durante la compilación del programa).

> [!NOTE]
> **Comentario:** una nota que explica parte del código, y que será ignorada en la fase de compilación.

### Tipos de datos

El **tipo de dato** indica qué clase de valor almacenará una variable y qué operaciones se le pueden aplicar sin producir un error.

> [!NOTE]
> **Tipo de dato:** define el tipo de valor que tiene una variable o estructura de datos, y qué tipo de operaciones matemáticas, relacionales o lógicas pueden aplicarse sin causar un error.
>
> **String:** tipo de dato usado para representar una secuencia de caracteres, dígitos y/o símbolos.
>
> **Asignación:** establecer, restablecer o copiar un valor en una variable.
>
> **Entero (Integer):** tipo de dato usado para representar un número entero.
>
> **Float:** tipo de dato usado para representar un número decimal.
>
> **Double:** tipo de dato usado para representar un número decimal.

Los tipos de datos primitivos considerados en el currículo son: **int, double, char y boolean**.

#### String

El tipo **String** se utiliza para almacenar una secuencia de caracteres, dígitos y/o símbolos (un texto). El texto se escribe entre comillas dobles en Java, mientras que Python puede usar comillas simples o dobles.

#### Entero (Integer)

El tipo **int** se utiliza para almacenar números enteros (positivos o negativos).

#### Decimal

Los tipos **float** y **double** se utilizan para almacenar números decimales (de doble precisión). Como **double** tiene mayor precisión que **float**, es más seguro usar double en los ejercicios.

#### Char

El tipo **char** se utiliza para almacenar un único carácter, dígito o símbolo.

> [!NOTE]
> **Char:** tipo de dato usado para representar un único carácter, dígito o símbolo.
>
> **Boolean:** tipo de dato que representa uno de dos posibles valores: verdadero o falso.

#### Boolean

El tipo **boolean** se utiliza para almacenar uno de dos posibles valores: **true** o **false**. Por ejemplo, una variable booleana podría usarse para almacenar si un producto sigue en stock, si una persona es hombre, si un viaje ha sido pagado, etc.

Las variables booleanas se utilizan a menudo para evaluar expresiones lógicas. En el código, con frecuencia se añaden condiciones, y si la condición se evalúa como verdadera, se ejecutan ciertas sentencias; en caso contrario, se ejecutan sentencias diferentes.

Otro ejemplo del uso de una variable booleana sería repetir un fragmento de código mientras una expresión se evalúe como verdadera o falsa, según los requisitos.

Considera las siguientes variables: `a = 7` y `b = 54`.

- `((a<9) and (b>30))` se evalúa como **verdadero**: si ambas condiciones son verdaderas, el resultado es verdadero. 7 es menor que 9 y 54 es mayor que 30 (ambas condiciones se cumplen).
- `((a>3) or (b<3))` se evalúa como **verdadero**: si al menos una condición es verdadera, el resultado es verdadero. (La primera condición es verdadera; la segunda es falsa.)

### Operadores

Los **operadores** se utilizan para realizar cálculos, comparaciones y otras operaciones lógicas. Pueden ser **operadores aritméticos** (`+`, `-`, `/`, `*`, `%`), **operadores booleanos** (`!`, `&&`, `||`) u **operadores relacionales** (`<=`, `<`, `>`, `>=`, `==`, `!=`).

> [!NOTE]
> **Operador aritmético:** un carácter que se utiliza para realizar un cálculo.
>
> **Operador booleano:** un carácter que representa una operación lógica específica, utilizada para producir un resultado verdadero o falso.
>
> **Operador relacional:** un operador utilizado para comparar valores o expresiones.

| Operador en Java | Operador en Python | Significado |
|---|---|---|
| `+` | `+` | suma |
| `-` | `-` | resta |
| `*` | `*` | multiplicación |
| `/` | `/` | división |
| `%` | `%` | módulo (devuelve el resto) |
| `<` | `<` | menor que |
| `<=` | `<=` | menor o igual que |
| `>` | `>` | mayor que |
| `>=` | `>=` | mayor o igual que |
| `==` | `==` | igual a |
| `!=` | `!=` | distinto de |
| `&&` | `and` | y |
| `\|\|` | `or` | o |

#### Operadores unarios y binarios

Los operadores aritméticos vistos hasta ahora son **operadores binarios**, es decir, requieren dos operandos (dos valores) para aplicar el cálculo. También existen **operadores unarios** (que requieren un único operando), como:

| Operador unario | Significado |
|---|---|
| `-` | números negativos |
| `++` | incrementar el valor en 1 |
| `--` | decrementar el valor en 1 |

> [!NOTE]
> **Operador binario:** un operador que requiere dos operandos (valores).
>
> **Operando:** un valor utilizado en una expresión matemática.
>
> **Operador unario:** un operador que requiere un único operando.
>
> **División entera:** división en la que se descarta la parte fraccionaria.
>
> **División en coma flotante:** división en la que se conserva la parte fraccionaria.

#### División: entera vs. en coma flotante

Aunque resulta bastante sencillo entender cuándo utilizar los operadores de suma, resta o multiplicación, puede resultar algo más complicado comprender los operadores de **división entera** y **módulo**.

En **Java y Python**, existen dos tipos de división: la **división entera** y la **división en coma flotante**.

En **Java**, ambos tipos utilizan el mismo símbolo (barra diagonal `/`). Sin embargo, al dividir dos valores enteros, el resultado será un entero (división entera); al dividir dos números decimales, o un decimal y un entero, el resultado será un número decimal (división en coma flotante). Por ejemplo, aunque el resultado matemático sea 3.5, si ambos números son enteros, el valor mostrado será 3. En cambio, si ambas variables almacenan números decimales, el resultado mostrado también será decimal (3.5). Si los valores son de tipos mixtos (un entero y un decimal), el resultado también será decimal (3.5).

En **Python**, como el tipo de las variables no se especifica, existen operadores diferentes para representar los distintos tipos de división:

- La **división en coma flotante** se realiza con el operador `/` (barra diagonal), y el resultado siempre será un número decimal, independientemente del tipo de dato de los números (por ejemplo, el resultado sería 3.5).
- La **división entera** utiliza el operador `//` (doble barra diagonal). Este operador devuelve la **división por suelo (floor division)**, lo que significa que, sea cual sea el resultado, siempre se redondeará hacia abajo: la parte decimal se trunca (se ignora o elimina). Por ejemplo, el resultado mostrado sería 3, truncando el resultado sin tener en cuenta el tipo de dato de las variables.

<br>

## B2.1.2. Manipulación de subcadenas (substrings)

### Comillas dentro de un texto

Las comillas dobles se utilizan para almacenar un carácter en Java, o incluso una cadena en Python; lo mismo ocurre con las comillas simples. Por tanto, cuando se quiere incluir una comilla simple o doble dentro del texto, debe usarse la **barra invertida** (`\`).

| Carácter | Java y Python |
|---|---|
| “ | \" |
| ‘ | \' |
| \ | \\ |

### Bloques de texto

En Java, las cadenas de varias líneas pueden escribirse uniendo el texto de las diferentes líneas mediante el operador `+`. El carácter `\n` representa el salto de línea, indicando que el siguiente fragmento de texto se mostrará en la línea siguiente.

En Python, las cadenas de varias líneas pueden escribirse utilizando comillas dobles triples (`"""`).

El lenguaje de programación ofrece varias **funciones integradas** que pueden usarse para manipular cadenas. En los ejemplos siguientes, `text` es una variable que almacena un fragmento de texto, como: “Computer Science is fun!”.

### Longitud (Length)

La función de longitud devuelve el número de caracteres (incluyendo espacios) del valor almacenado en la cadena `text`. En este caso, el valor almacenado sería 24.

### Concatenación

La **concatenación** se refiere a unir dos o más valores de cadena.

> [!NOTE]
> **Concatenación:** unir cadenas de texto.

Tanto Java como Python permiten varias formas de lograr la concatenación. Una de ellas es mediante el operador `+`, que unirá las dos cadenas. En Java también puede usarse la función `concat` para este propósito.

Es importante señalar que la concatenación es una técnica que se aplica a una serie de variables de tipo cadena, en lugar de a una combinación de cadenas y enteros o decimales. Si es necesario concatenar una combinación de cadenas y números, en Java puede usarse el operador `+`, o bien convertir previamente el valor numérico a cadena. En Python, para este propósito pueden usarse el operador de interpolación (`%`), la función `str`, `str.format` o las **f-strings**.

> [!TIP]
> En Python, si se quiere mostrar el contenido de dos variables sin guardarlo en otra variable, basta con usar la función `print`, que acepta varios parámetros separados por comas.

### Subcadena (Substring)

`substring` es la función utilizada para obtener parte de una cadena, por ejemplo, para extraer la primera palabra o letra de un texto, o el texto entre posiciones específicas de la cadena.

La primera posición de una cadena es siempre **0**.

En **Java**, la función utilizada para este propósito se llama `substring`

En **Python**, la función de subcadena suele denominarse `slicing`.

### Reemplazar (Replace)

El método `replace` busca en una cadena un carácter o conjunto de caracteres y los reemplaza por otro carácter o caracteres.

En **Java**, el método `replace` reemplaza un único carácter (por ejemplo, convirtiendo el texto en “Comput@r Sci@nc@ is fun”). Para reemplazar varios caracteres, debe utilizarse el método `replaceAll`.

En **Python**, el método `replace` puede usarse tanto para reemplazar un único carácter como varios caracteres a la vez.

### Eliminar espacios (Strip)

En ocasiones, al leer valores desde un archivo de texto o cualquier almacenamiento permanente, puede ser necesario eliminar los espacios en blanco sobrantes al inicio o al final del texto. Esto puede lograrse utilizando el método `strip`.

Algunas versiones de **Java** aceptan `trim` en lugar de `strip` para el mismo propósito, eliminando los espacios iniciales y finales. Para lograr el mismo resultado en **Python**, puede usarse la función `strip`.

<br>

## B2.1.3. Gestión de excepciones

Cuando se ejecuta un programa informático, diferentes motivos o eventos pueden provocar que el programa se detenga o produzca un resultado inesperado. Entre estos motivos se incluyen **errores lógicos** en el código, **entradas inesperadas del usuario** o la **falta de disponibilidad de recursos**.

### Errores lógicos

Los **errores lógicos** son secuencias incorrectas en la lógica del programa, elecciones incorrectas de condiciones o cálculos incorrectos. Por ejemplo, al intentar calcular la media de tres números, dividir la suma de los tres números entre 2 en lugar de entre 3 produciría un resultado incorrecto.

> [!NOTE]
> **Error lógico:** un error en un programa que hace que funcione de forma incorrecta; no provoca el cierre inesperado del programa.
>
> **Error en tiempo de ejecución:** un error que se produce al ejecutar un programa; el programa puede detenerse inesperadamente.
>
> **Gestión de excepciones:** proceso de respuesta ante una excepción, de modo que el sistema no se detenga inesperadamente.
>
> **Excepción:** un evento inesperado que detiene la ejecución de un programa, por ejemplo, una división entre 0.

Este tipo de errores solo puede detectarse mediante pruebas, ya que superarían la fase de compilación.

### Errores en tiempo de ejecución

Los **errores en tiempo de ejecución** pueden hacer que el programa se bloquee. Se refieren a problemas que ocurren mientras el programa se ejecuta, como:

- una división entre 0;
- un archivo que no se encuentra;
- errores de truncamiento;
- errores de desbordamiento (overflow) o subdesbordamiento (underflow);
- un dispositivo de hardware no disponible, por ejemplo, una impresora que no está lista;
- un archivo de clase que no se encuentra.

Además, el usuario puede introducir **entradas inesperadas**, como escribir texto en lugar de un número, introducir valores que provocarían un intento de división entre 0, o indicar una ubicación de archivo incorrecta para leer o escribir datos.

### Falta de disponibilidad de recursos

La **falta de disponibilidad de recursos** se refiere a equipos de hardware y software que no están disponibles para la operación, como un archivo que no se encuentra o una impresora que no está lista para la operación.

### Técnicas de gestión de excepciones

Todos estos eventos pueden tratarse para que el programa no se bloquee, utilizando la **gestión de excepciones**. Aunque no se consiga la operación deseada, el usuario puede hacerse una idea de lo que ha fallado y puede seguir probando otras funciones del programa.

La función de las técnicas de gestión de excepciones es mantener el flujo normal del programa, capturando y lanzando excepciones que no pueden gestionarse localmente. En Java, esto toma la forma de bloques **try/catch**, mientras que en Python se utilizan bloques **try/except**. El código que puede lanzar un error se escribe dentro del bloque `try`, y la excepción se captura y se muestra, si es necesario, en el bloque `catch`/`except`.

Ambos lenguajes permiten un bloque **finally**, que se sitúa al final del bloque try/catch o try/except e incluye código que se ejecutará siempre después de salir de la sentencia `try`, independientemente del resultado del bloque `try`: tanto si se produce un error como si no.

**Python**

```python
number = int(input("Introduce un número: "))
try:
  result = 10/number
  print(result)
exceot ZeroDivisionError:
  print("No puedes dividir por cero")
finally:
  print("Esto se imprime en cualquier caso")
```

En el ejemplo anterior, se solicita al usuario que introduzca un número. Si el número introducido es 0, se capturará en la excepción; en caso contrario, se realizará el cálculo y se mostrará el resultado. Independientemente de la acción completada, se mostrará el mensaje incluido en el bloque `finally`.

**Python**

```python
number = int(input("Introduce un número: "))
try:
  result = 10/number
  print(result)
except:
  print("Se produjo un problema")
```

La estructura de gestión de excepciones puede incluir únicamente un bloque `try/catch` en Java, o solo un bloque `try/except` en Python. No es necesario indicar específicamente el tipo de error que ha podido provocar el bloqueo del programa, pero resulta útil para ayudar al programador a depurar el código y solucionar problemas que puedan resolverse, o para que el usuario entienda el problema si se proporciona una entrada incorrecta.

> [!IMPORTANT]
> **Información clave**
>
> “Excepción” se refiere al evento que interrumpe la ejecución de un programa, mientras que “gestión de excepciones” se refiere a las acciones que se llevan a cabo para tratar una excepción, o a cómo se evita que el sistema se detenga inesperadamente. Por ejemplo, una división entre 0 es una excepción; usar un bloque try/catch o try/except es la técnica de gestión de excepciones.

<br>

## B2.1.4. Técnicas de depuración

La **depuración** consiste en encontrar y corregir errores en el código. Las técnicas de depuración más comunes incluyen las **tablas de traza**, la **depuración con puntos de interrupción**, las **sentencias de impresión** y la **ejecución paso a paso** del código.

> [!NOTE]
> **Depuración (debugging):** encontrar y corregir errores en un programa.
>
> **Tabla de traza:** técnica utilizada para probar un algoritmo y predecir cómo se ejecutará y cómo cambiarán los valores de las variables.
>
> **Punto de interrupción (breakpoint):** una marca para interrumpir la ejecución del código con fines de depuración.

### Tablas de traza

Las **tablas de traza** son una técnica que se suele utilizar en la fase de diseño para probar un algoritmo y predecir paso a paso cómo se ejecutará. Pueden utilizarse para demostrar el resultado de un algoritmo o para identificar errores lógicos.

Una tabla de traza es una tabla en la que las columnas representan variables, condiciones o una salida del algoritmo. Sin embargo, no siempre son necesarias todas las variables, condiciones o salidas; esto depende del propósito de la tabla de traza.

Su función es identificar cómo cambian las variables, a qué se evalúan las condiciones y cuáles son los resultados producidos. Al elaborar una tabla de traza, se puede determinar el propósito del algoritmo o detectar cualquier fallo en él.

Por ejemplo, considera el siguiente problema: los estudiantes de un curso de idiomas aprobarán su examen final si su puntuación es 80 o superior. Como los estudiantes se matriculan en el curso cada trimestre, el número de estudiantes es desconocido. Por tanto, el profesor introducirá 999 para terminar el programa. Se pide identificar el número de estudiantes que aprueban la evaluación.

El siguiente diagrama de flujo se ha diseñado para proponer una posible solución al problema:

<div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/B2.%20Programacion/images/flowchart.png?raw=true" alt="Flowchart" width="300" height="auto"/>
    <p><em>Figura 1: Diagrama de flujo. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

La tabla de traza para los datos de entrada `23, 98, 33, 45, 78, 80, 81, 84, 34, 999` sería la siguiente:

| count | score | output |
|---|---|---|
| 0 | 23 | |
| | 98 | |
| 1 | 33 | |
| | 45 | |
| | 78 | |
| | 80 | |
| 2 | 81 | |
| 3 | 84 | |
| 4 | 34 | |
| | 999 | 4 students have passed the exam |

Cuando se introduce el valor 98, el contador se incrementa. Los valores 33, 45 y 78 no afectan al contador, por lo que su valor permanece igual. Puedes optar por repetir el valor anterior de la variable `count` o dejarlo en blanco, ya que no hay cambios. Ten en cuenta que, si hay una sentencia que reasigna el valor de la variable, aunque el valor sea el mismo que el anterior, debe aparecer en la columna `count`, ya que supone un cambio en la variable. Cuando se introduce el valor 80, el contador se incrementa de nuevo, y el procedimiento se repite para los valores 81 y 84, pero no ocurre nada con el contador cuando se introduce 34. 999 es el valor que terminará el programa, por lo que se mostrará la salida, ya que en este ejemplo la salida solo se muestra después de introducir 999.

### Depuración con puntos de interrupción (Breakpoints)

Los **puntos de interrupción** son marcas especiales que interrumpen la ejecución del código con fines de depuración. Para establecer un punto de interrupción en **Visual Studio Code**, basta con hacer clic en el margen izquierdo, a la izquierda del número de línea (o colocar el cursor en la línea y pulsar `F9`). Aparecerá un círculo rojo que indica que el punto de interrupción está activo. Para quitarlo, basta con volver a hacer clic sobre el círculo rojo (esto varía de un IDE a otro).

*Depuración con puntos de interrupción en Visual Studio Code*

Tras establecer los puntos de interrupción, el siguiente paso es ejecutar el programa en modo de depuración. Esto se hace abriendo la vista **Ejecutar y depurar** (`Ctrl+Shift+D`) y pulsando el botón **Ejecutar y depurar** (o el botón verde de reproducción), o simplemente pulsando `F5`. Para ello, es necesario tener instalada la extensión correspondiente al lenguaje utilizado (por ejemplo, *Extension Pack for Java* de Microsoft para Java, o la extensión *Python* de Microsoft para Python).

### Ejecución paso a paso

Para supervisar y ver qué ocurre con las variables, debes utilizar los botones de la barra de depuración: **Paso a paso por procedimientos (Step Over)**, **Paso a paso por instrucciones (Step Into)** y **Paso a paso para salir (Step Out)**. Si quieres comprobar qué ocurre en la línea del punto de interrupción, entrando en la función que se llama en ella, elegirías el botón **Step Into** (`F11`); pero si quieres omitir esa línea y ejecutar la siguiente, elegirías el botón **Step Over** (`F10`). Con **Step Out** (`Shift+F11`) se termina de ejecutar la función actual y se vuelve al código que la llamó. En Visual Studio Code, estas opciones aparecen como iconos en la barra flotante de depuración, junto con **Continuar** (`F5`), **Reiniciar** (`Ctrl+Shift+F5`) y **Detener** (`Shift+F5`). Mientras se depura, los paneles **Variables**, **Inspección (Watch)** y **Pila de llamadas (Call Stack)** de la vista de depuración permiten observar cómo cambian los valores de las variables.

### Sentencias de impresión (Print statements)

Al probar tu código, puede que te preguntes si la ejecución del programa ha llegado a una línea de código concreta, si una variable ha cambiado su valor como se esperaba o si una sentencia de decisión se ha evaluado como verdadera o falsa. Incluir sentencias de impresión en tu código para rastrear estos cambios es un método útil que te ayudará a identificar cuándo exactamente tu código dejó de ejecutarse como se esperaba y te dará una idea de qué ha salido mal. El único inconveniente puede ser que, una vez realizada la depuración y corregidos los errores, tendrás que eliminar esas sentencias de impresión.

> [!IMPORTANT]
> **Información clave**
>
> Debes ser capaz de construir y utilizar técnicas comunes de depuración. Saber completar tablas de traza es una técnica importante que puede utilizarse para probar la lógica y la funcionalidad de un algoritmo, para identificar cómo cambian las variables durante la ejecución del programa y para identificar la salida esperada de un algoritmo.
