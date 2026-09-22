<h1 align="center">B2.1. Fundamentos de la programación
<div align="center">

</div>

## Contenido:

- [B2.1.1. Variables](#B211-variables)
- [B2.1.2. Manipulación de subcadenas (substrings)](#B212-manipulación-de-subcadenas-substrings)

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
