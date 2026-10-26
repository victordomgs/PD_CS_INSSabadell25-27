<h1 align="center">B2.2. Estructuras de datos
<div align="center">

</div>

## Contenido:

- [B2.2.1. Estructuras de datos estáticas y dinámicas](#B221-estructuras-de-datos-estáticas-y-dinámicas)
- [B2.2.2. Arrays y listas](#B222-arrays-y-listas)
  - [Listas unidimensionales](#listas-unidimensionales-python)
  - [Arrays paralelos](#arrays-paralelos)
  - [Listas bidimensionales](#arrays--listas-bidimensionales)
  - [Listas dinámicas en Python](#listas-dinámicas-en-python)
- [B2.2.3. Pilas](#B223-pilas)
  - [Operaciones de una pila](#operaciones-de-una-pila)
  - [Usos de las pilas](#usos-de-las-pilas)
- [B2.2.4. Colas](#B224-colas)
  - [Operaciones de una cola](#operaciones-de-una-cola)
  - [Usos de las colas](#usos-de-las-colas)

<br>

## B2.2.1. Estructuras de datos estáticas y dinámicas

> [!NOTE]
> - **Estructura de datos estática:** estructura de datos de tamaño fijo predefinido, con los elementos almacenados en posiciones de memoria contiguas.
> - **Estructura de datos dinámica:** estructura de datos que puede crecer o decrecer en tiempo de ejecución, con los elementos almacenados en posiciones de memoria encadenadas, pero no necesariamente contiguas.
> - **Acceso directo:** método de acceso en el que los elementos se recuperan directamente mediante su índice (posición).
> - **Acceso secuencial:** método de acceso en el que los elementos se comprueban uno tras otro, desde el principio hasta el final de la estructura de datos.

Una **estructura de datos estática** tiene un **tamaño fijo predefinido**: se le asigna un espacio de memoria concreto que no cambia durante la ejecución del programa, y sus elementos se almacenan en **posiciones de memoria contiguas**. Sus elementos pueden accederse tanto de forma **directa** como **secuencial**.

Una **estructura de datos dinámica** no tiene un tamaño fijo predefinido: **puede crecer o decrecer en tiempo de ejecución** y sus elementos se almacenan en posiciones de memoria **encadenadas**, aunque no necesariamente contiguas. Sus elementos **no** pueden accederse de forma directa.

### Estructura de datos estática

| Ventajas | Desventajas |
|---|---|
| **Acceso rápido**, ya que los elementos se pueden acceder directamente mediante el índice (la posición del elemento en la estructura). | **Uso ineficiente de la memoria**: hay que conocer de antemano el tamaño probable de la estructura para asignar memoria suficiente. |
| **No hay que tratar errores de desbordamiento (*overflow*) o subdesbordamiento (*underflow*)** al añadir o eliminar elementos, porque el tamaño es fijo. | La memoria se asigna **aunque no se necesite**. |
| **Más fácil de programar**: no hace falta comprobar su tamaño en ningún momento. | **No permite flexibilidad**, ya que su tamaño es fijo. |
| | Al eliminar un elemento puede quedar un **hueco vacío** entre otros dos, y modificar el código para reutilizarlo puede llevar tiempo. |
| | **Insertar** elementos entre otros dos, si no hay un hueco libre, **consume mucho tiempo**. |

### Estructura de datos dinámica

| Ventajas | Desventajas |
|---|---|
| **Flexibilidad**: puede reducirse o crecer según sea necesario en tiempo de ejecución (adecuada cuando el tamaño de los datos no se conoce de antemano o puede cambiar con el tiempo). | El programador debe tratar situaciones de **desbordamiento** (la estructura podría superar el límite de memoria) y de **subdesbordamiento** (podría intentar eliminar un elemento de una estructura ya vacía) al insertar o eliminar elementos. |
| **Uso eficiente de la memoria**: como puede redimensionarse, no se desperdicia memoria. | **Más difícil de programar**, ya que el programador debe llevar siempre el control de su tamaño y de las asignaciones de datos. |
| Las operaciones de **inserción y eliminación son óptimas** en cuanto a complejidad temporal y espacial. | |

<br>

## B2.2.2. Arrays y listas

### Arrays unidimensionales y listas unidimensionales

Supón que tu profesor quiere almacenar las notas de 100 alumnos. Una forma de hacerlo es usar 100 variables, pero eso supone mucho desperdicio de memoria, muchas líneas de código y mucho esfuerzo. ¿Y si tuviera que almacenar 1000 notas?

Una solución mejor es almacenar los 100 o 1000 elementos bajo **un único nombre o identificador**. La estructura de datos **array** permite hacerlo.

Un **array 1D** (o **lista 1D** en Python) es una estructura de datos que almacena **elementos del mismo tipo de dato** bajo **un único identificador (nombre)**. Esos elementos se pueden **acceder directamente** mediante un **índice** (plural: *índices*), que indica la posición en el array. Algunos lenguajes indican el primer índice como el elemento 0, y otros permiten al programador decidir cómo se numerarán los elementos.

Por ejemplo, un array de cinco enteros que almacena notas sobre 100 se llama `grades`. Gráficamente, los arrays pueden representarse de forma horizontal o vertical.

El elemento en el índice 2 (el 3.er elemento, contando desde 0) se accede con el nombre del array seguido del índice:

```python
print(grades[2])
```

Ten en cuenta que, si el primer elemento tiene índice 0, **el último está en el índice 4** (en este caso, `grades` solo tiene cinco elementos).

Para procesar arrays se usan **bucles**. Los bucles permiten **recorrer** el array, por lo que cada vez que se hagan cálculos con todos los elementos, se busque un elemento, se ordenen, etc., se usarán bucles.

### Listas unidimensionales (Python)

Python sustituye los arrays por **listas**, pero se pueden manipular para que se comporten como arrays.

En Python **no hace falta declarar** las estructuras de datos. Se siguen usando **corchetes** para indicar que la estructura es una lista 1D. Por ejemplo, `grades` se vería así:

```python
grades = [75, 60, 90, 85, 70]
```

Si se quiere inicializar una lista 1D y rellenarla con un bucle FOR, el código sería:

```python
grades = [0] * 5

for i in range(5):
    grades[i] = int(input("Introduce una nota: "))
```

- La primera línea especifica el **valor inicial** que tomará cada elemento de la lista (en este caso, 0). Después del `*` va el **tamaño** de la lista (es decir, al principio hay cinco ceros).
- Si esa línea se escribiera como `grades = []`, al probar el bucle FOR se produciría un error (*index out of range*), porque el tamaño de la lista sería cero y no habría forma de añadirle elementos así.

Sin embargo, la siguiente secuencia es totalmente válida:

```python
grades = []
grades = [0] * 5
```

Esto es posible porque la lista `grades` **se sobrescribe**. Pero podría haberse escrito directamente:

```python
grades = [0] * 5
```

El objetivo de esta línea es inicializar la lista `grades` con 0 en sus cinco elementos.

Estos son ejemplos de una lista 1D de tipo **string** y otra de tipo **booleano**:

```python
names = ["Ana", "Luis", "Marta", "Pau", "Sara"]
passed = [True, False, True, True, False]
```

> [!WARNING]
> **Error común**
>
> Los algoritmos escritos para resolver un problema deben funcionar correctamente. Al pedir un algoritmo que encuentre el **valor más pequeño** de un array o lista 1D, muchos alumnos inicializan una variable llamada `min` a **0** y luego comparan cada elemento con ella para encontrar uno menor.
>
> La estructura podría almacenar **solo números positivos**, por lo que nunca se encontraría un valor menor que 0. Recuerda **inicializar esa variable con el primer elemento del array**: así, si ningún otro elemento es menor, ya tienes guardado el más pequeño.

```python
minimum = grades[0]      # se evita llamarla min, que es una función de Python

for i in range(1, len(grades)):
    if grades[i] < minimum:
        minimum = grades[i]

print("Nota mínima:", minimum)
```

### Arrays paralelos

Los **arrays paralelos** son dos o más arrays del mismo tamaño, de modo que el elemento *n* del primer array está relacionado con el elemento *n* del segundo, y así sucesivamente. Los valores almacenados en esos arrays en un índice dado están relacionados de algún modo, por ejemplo para definir una estructura de **registro** con datos de alumnos: el primer array almacena los nombres, el segundo las edades y el tercero las direcciones. Al recuperar el elemento de la posición 3 de cada array, se pueden identificar el nombre, la edad y la dirección del tercer alumno.

```python
names = ["Ana", "Luis", "Marta"]
ages = [16, 17, 16]
addresses = ["C/ Mayor 1", "C/ Sol 5", "C/ Luna 8"]

print(names[2], ages[2], addresses[2])   # Marta 16 C/ Luna 8
```

> [!NOTE]
> **Arrays paralelos:** grupo de arrays del mismo tamaño en los que el elemento de un índice dado en uno de los arrays se corresponde con otro elemento del mismo índice en otro array, como las descripciones de una misma entidad.

<br>

### Arrays / listas bidimensionales

Un array bidimensional puede verse como una **tabla** con **filas** y **columnas**. Para manipular y recorrer un array 2D se usan **dos índices**: uno para las filas y otro para las columnas. Al escribir código, **las filas van siempre primero y las columnas después**.

Piensa en almacenar los números del 1 al 9 en una tabla de tres filas y tres columnas. Para ello se crea un array 2D o una lista 2D. Cada elemento se puede **acceder directamente** indicando sus índices (índice de fila e índice de columna).

#### Declaración

```python
numbers = [[0] * 3 for i in range(3)]
```

- El `3` de `[0] * 3` indica el **número de columnas** y el `3` de `range(3)` el **número de filas**. El valor `0` es el valor inicial al que se fija la lista.
- La lista 2D aparece como una tabla de **tres filas y tres columnas llenas de ceros**.

> [!WARNING]
> No uses `[[0] * 3] * 3` para crear una lista 2D: las tres filas serían **la misma lista repetida**, y modificar una afectaría a todas.

Para referirse a un elemento concreto se usa el nombre de la lista seguido de corchetes con los índices de fila y columna:

- `numbers[0][2]` se refiere al elemento de la lista `numbers` situado en la intersección de la **primera fila** con la **tercera columna**.

#### Recorrer una lista 2D

Manipular listas 2D requiere **dos bucles**: el primero para las filas y el segundo para las columnas.

```python
# Rellenar la lista pidiendo los valores al usuario
for i in range(3):
    for j in range(3):
        value = int(input("Introduce un número: "))
        numbers[i][j] = value

# Mostrar los valores almacenados
for i in range(3):
    for j in range(3):
        print(numbers[i][j], end=" ")
    print()
```

- Los dos primeros bucles controlados por contador recorren la lista (`i` para las filas y `j` para las columnas). Después se pide al usuario un número, que se guarda en la variable `value` y se asigna a la lista `numbers`.
- Los dos últimos bucles recorren la lista para **mostrar por pantalla** los valores almacenados.

#### Listas con distinto número de filas y columnas

Una lista 2D también puede tener un número diferente de filas y de columnas. En el siguiente ejemplo, la lista `numbers` se construye con **dos filas y tres columnas**:

```python
numbers = [[0] * 3 for i in range(2)]
```

Para rellenarla con valores se puede usar el siguiente código:

```python
for i in range(2):
    for j in range(3):
        numbers[i][j] = int(input("Introduce un número: "))
```

> [!WARNING]
> **Error común**
>
> Muchos alumnos pierden puntos por un uso incorrecto de los índices en las listas 2D o por recorrerlas mal: pasar por alto los **límites** o no usar **dos índices** para recorrerlas. Recuerda que **siempre se usan las filas primero y las columnas después**.

<br>

### Listas dinámicas en Python

Una **lista dinámica** en Python es una **estructura de datos dinámica**, es decir, no tiene un tamaño fijo. Las listas dinámicas pueden almacenar **valores duplicados**. Al crear una lista dinámica, se puede declarar simplemente como una **lista vacía**:

```python
grades = []
```

Sin embargo, al intentar insertar un nuevo elemento escribiendo algo como lo siguiente, se producirá un **error**:

```python
grades[0] = 75   # IndexError: la lista está vacía
```

Para manipular listas dinámicas se usan **métodos** específicos:

| Método | Explicación | Ejemplo de código |
|---|---|---|
| `append()` | Añade un nuevo elemento, pasado como argumento, **al final** de la lista. | `grades.append(75)` |
| `insert()` | Inserta un nuevo elemento en un índice dado (el primer argumento es el índice y el segundo el valor a insertar). | `grades.insert(0, 64)` |
| `remove()` | Elimina la **primera aparición** de un elemento pasado como argumento. | `grades.remove(75)` |
| `pop()` | Elimina el elemento del índice especificado. | `grades.pop(0)` |
| `pop()` | Elimina el **último** elemento si no se indica ningún índice. | `grades.pop()` |
| `clear()` | Vacía la lista entera. | `grades.clear()` |
| `len()` | Devuelve el tamaño de la lista. | `len(grades)` |

Para recorrer una lista dinámica se puede usar un bucle FOR:

```python
for i in range(len(grades)):
    print(grades[i])
```

Otra forma de conseguir lo mismo es:

```python
for i in grades:
    print(i)
```

En este último caso, `i` **no es el índice**, sino un **elemento** de la lista dinámica.

<br>

## B2.2.3. Pilas

Si fueras cajero de un banco, manejarías muchas monedas. Para manipularlas con facilidad, se clasifican según su valor y se guardan en montones: un montón de monedas de 10 céntimos, otro de 20 céntimos, otro de 50 céntimos, etc. Cuando el cajero necesita una de estas monedas, la coge **de la parte superior** del montón correspondiente, de modo que la pila se mantiene intacta. Cuando necesita añadir una moneda nueva, la coloca de nuevo **encima** del montón.

Otro ejemplo es una **pila de platos**: un plato nuevo se añade encima de la pila y un plato se retira de la parte superior, ya que, de lo contrario, los platos podrían romperse.

En informática, cuando se realizan acciones que funcionan con el mismo principio, se puede usar una estructura de datos abstracta llamada **pila** (*stack*). La pila funciona según el principio **LIFO** (*Last In First Out*, "el último en entrar es el primero en salir") o **FILO** (*First In Last Out*), lo que significa que **solo se accede al elemento superior**. La operación de eliminar un elemento de la pila se llama **pop** (sacar el elemento superior), y la operación de añadir un elemento se llama **push** (añadir un elemento en la parte superior de la pila).

> [!NOTE]
> - **Pila (*stack*):** estructura de datos abstracta que funciona según el principio LIFO.
> - **Principio Last In First Out (LIFO) o First In Last Out (FILO):** el último elemento insertado es el primero en ser eliminado.
> - **Pop:** método para eliminar el elemento de la parte superior de una pila.
> - **Push:** método para insertar un elemento en la parte superior de una pila.
> - **Puntero de pila (*stack pointer*):** registro que almacena la dirección de memoria del último dato añadido a una pila o, en ocasiones, la primera dirección disponible de la pila.

Una pila puede usar una variable **puntero de pila** para indicar la **siguiente posición libre** de la pila.

Una pila puede implementarse como una **estructura de datos estática** usando **arrays** (tendría un tamaño fijo) o como una **estructura de datos dinámica** usando una **lista enlazada** (no tendría un tamaño fijo).

### Operaciones de una pila

Las operaciones que se realizan sobre una pila son:

| Operación | Descripción |
|---|---|
| `isEmpty` | Comprueba si la pila está **vacía**. Intentar hacer un `pop` en una pila vacía provocaría un error de **subdesbordamiento** (*underflow*). |
| `isFull` | Comprueba si la pila está **llena**. Intentar hacer un `push` en una pila llena provocaría un error de **desbordamiento** (*overflow*). |
| `push` | Añade un elemento a la **parte superior** de la pila. |
| `pop` | Elimina un elemento de la **parte superior** de la pila. |
| `peek` | **Devuelve** el elemento superior (sin eliminarlo). |

Ejemplo en Python usando una lista como pila:

```python
stack = []

stack.append(10)    # push
stack.append(20)    # push
stack.append(30)    # push

print(stack[-1])    # peek -> 30
print(stack.pop())  # pop  -> 30
print(stack.pop())  # pop  -> 20

if len(stack) == 0: # isEmpty
    print("La pila está vacía")
else:
    print("Quedan elementos:", stack)
```

### Usos de las pilas

Las pilas se usan para almacenar datos **en el orden en que ocurrieron** cuando puede ser necesario **volver atrás** hasta un punto o acción anterior, ya que respetan el principio LIFO.

Las pilas se pueden usar:

- **Para crear una función DESHACER (UNDO) en juegos:** las acciones se añaden a la pila (*push*); al deshacer, se sacan (*pop*).
- **Para permitir la navegación hacia atrás en un navegador web:** al pulsar el botón de retroceso se realiza una operación *pop*; al abrir un sitio web nuevo se realiza una operación *push*.
- **Para la gestión de interrupciones:** cuando se interrumpe la actividad actual de la CPU, el contenido de las variables y las direcciones de retorno se guardan en una pila; una vez atendida la interrupción, se sacan de la pila para restaurar la actividad.
- **Para evaluar expresiones aritméticas:** al evaluar expresiones en **notación polaca inversa (RPN)**, los operandos se introducen en la pila; cuando aparece un operador, si es binario (requiere dos operandos) se realizan dos operaciones *pop* más, se calcula el resultado y se vuelve a introducir en la pila (*push*). El proceso continúa hasta llegar al resultado.
- **Para la recursión:** las direcciones de retorno y los valores de los parámetros se almacenan en una pila para ayudar en el proceso de desenrollado (*unwinding*).

> [!NOTE]
> - **Gestión de interrupciones (*interrupt handling*):** tratamiento de las solicitudes de interrupción.
> - **Interrupción (*interrupt*):** señal enviada por un dispositivo o por software para solicitar la atención del procesador; el procesador detiene su actividad actual hasta que se haya atendido la interrupción.
> - **Recursión:** proceso que utiliza una función o procedimiento definido en términos de sí mismo y que se llama a sí mismo.

<br>

## B2.2.4. Colas

Una **cola** (*queue*) es una estructura de datos que funciona según el principio **FIFO** (*First In First Out*, "el primero en entrar es el primero en salir"). Un ejemplo es una fila de personas esperando para pagar en un supermercado: la primera persona en llegar a la cola es la primera en salir, y una persona nueva que se une a la fila entra **al final** de la cola.

> [!NOTE]
> - **Cola (*queue*):** estructura de datos abstracta que funciona según el principio FIFO.
> - **Principio First In First Out (FIFO):** el primer elemento insertado es el primero en ser eliminado.
> - **Enqueue (encolar):** método para insertar un elemento al final (parte trasera) de una cola.
> - **Dequeue (desencolar):** método para eliminar un elemento del principio (parte delantera) de una cola.

Una cola utiliza un **puntero frontal** (*front*) para indicar de dónde se eliminarán los elementos y un **puntero trasero** (*rear*) para indicar dónde se añadirán.

Una cola puede implementarse como una **estructura de datos estática** usando **arrays** (tendrá un tamaño fijo y es posible que se llene, ya que ese tamaño no se puede superar). O bien puede implementarse como una **estructura de datos dinámica** usando una **lista enlazada** (no tendría un tamaño fijo).

### Cola circular

Cuando una cola se implementa con un array, a menudo se gestiona como una **cola circular**. Esto se hace para que, si se han eliminado elementos de la cola, **siga habiendo forma de añadir nuevos elementos aunque se haya llegado al último índice**, ya que la cola en realidad no estará llena.

En una cola circular:

- Si el puntero trasero **se iguala** al puntero frontal **después de añadir** un elemento, la cola está **llena**.
- Si se igualan **después de eliminar** un elemento, la cola está **vacía**.

### Operaciones de una cola

| Operación | Descripción |
|---|---|
| `isFull` | Comprueba si la cola está **llena**. Intentar encolar un elemento en una cola llena provocaría un error de **desbordamiento** (*overflow*). |
| `isEmpty` | Comprueba si la cola está **vacía**. Intentar desencolar un elemento de una cola vacía provocaría un error de **subdesbordamiento** (*underflow*). |
| `enqueue` | Añade un elemento al **final** de la cola. |
| `dequeue` | Elimina un elemento del **principio** de la cola. |
| `front` | Muestra el elemento almacenado al **principio** de la cola. |

Ejemplo en Python usando `deque`:

```python
from collections import deque

queue = deque()

queue.append("A")         # enqueue
queue.append("B")         # enqueue
queue.append("C")         # enqueue

print(queue[0])           # front   -> A
print(queue.popleft())    # dequeue -> A
print(queue.popleft())    # dequeue -> B

if len(queue) == 0:       # isEmpty
    print("La cola está vacía")
else:
    print("Quedan elementos:", list(queue))
```

> [!TIP]
> No uses `list.pop(0)` para desencolar en programas grandes: es lento, porque desplaza todos los elementos. `deque.popleft()` es la opción adecuada.

### Usos de las colas

Las colas se usan en **simulaciones** o en situaciones que requieren que **el primer elemento en entrar sea el primero en ser atendido**. Algunas aplicaciones son:

- **Colas de impresión:** los trabajos de impresión se almacenan en una cola. El primer trabajo enviado es el primero en atenderse. Los nuevos trabajos se unen al final de la cola, de modo que todos se atienden por orden de llegada.
- **Colas del teclado:** el búfer del teclado (que almacena los caracteres a medida que se escriben) funciona como una cola. Así, la primera letra que aparece en pantalla es la primera que se ha escrito. Los nuevos caracteres se añaden al final de la cola.
- **Simulaciones de situaciones de la vida real:** las colas de cajas, de lavado de coches, de salida de aparcamientos, etc., son situaciones que requieren una cola. Las personas o coches entran en la cola por un lado y salen por el otro.

<br>

> [!WARNING]
> **Error común**
>
> Los alumnos suelen perder puntos por no dar respuestas adecuadas a las **palabras clave** utilizadas en la pregunta. Por ejemplo, "*compare* las estructuras de datos estáticas y dinámicas" espera que des **tanto similitudes como diferencias** entre los dos tipos de estructuras de datos, y no solo diferencias.

> [!WARNING]
> **Error común**
>
> Cuando se pide indicar **aplicaciones** de una estructura de datos, como una cola o una pila, los alumnos suelen perder puntos por no ser lo bastante claros. Por ejemplo, decir que las pilas se usan "para deshacer" no sería suficiente para obtener ningún punto.
>
> Sé específico y explica una **situación concreta** en la que se necesite una función de deshacer, como implementarla en juegos: las acciones se añaden (*push*) a la pila y, cuando se necesita volver a la acción anterior, la función de deshacer saca (*pop*) la acción superior de la pila.

<br>
