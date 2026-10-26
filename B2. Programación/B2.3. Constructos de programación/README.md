<h1 align="center">B2.3. Estructuras de control de programación
<div align="center">

</div>

## Contenido:

- [B2.3.1. Secuenciación](#B231-secuenciación)
- [B2.3.2. Estructuras de selección](#B232-estructuras-de-selección)
- [B2.3.3. Bucles e iteración](#B233-bucles-e-iteración)

<br>

## B2.3.1. Secuenciación

Al resolver problemas, **el orden en que se ejecutan las instrucciones importa**. Veamos primero el ejemplo del intercambio de variables (apartado B2.1) hecho correctamente:

```python
a = 5
b = 7
temp = a   # 5 se guarda en la variable temporal temp
a = b      # 7 se guarda en a
b = temp   # 5 (desde la variable temporal) se guarda en b
```

Al final **a vale 7 y b vale 5**: el intercambio se ha realizado correctamente.

Si se cambia el orden de las instrucciones, el resultado es incorrecto:

```python
a = 5
b = 7
a = b      # 7 se guarda en a
temp = a   # 7 se guarda en la variable temporal temp
b = temp   # 7 (desde la variable temporal) se guarda en b
```

Aunque las instrucciones son las mismas, el resultado es erróneo solo por no estar en el orden correcto: al final **a y b valen 7** y no se ha producido el intercambio, a pesar de haber usado una variable temporal igual que en el algoritmo correcto.

La **secuencia** consiste en que las instrucciones se ejecutan una vez y en el orden exacto en que están escritas.

> [!NOTE]
> **Secuencia:** ejecutar las instrucciones una tras otra en el orden dado.

Respetar el orden es fundamental, porque afecta al resultado y puede provocar un funcionamiento incorrecto (como se ha visto), **errores lógicos** o **bucles infinitos**.

<br>

## B2.3.2. Estructuras de selección

### Estructuras de selección o ramificación

La **selección** es una construcción de programación que decide qué instrucciones, si las hay, se ejecutan en función de una o más condiciones. Las condiciones suelen construirse con **operadores lógicos**. Las sentencias **IF** son un ejemplo: se evalúa la condición y, si es verdadera, se ejecutan unas instrucciones; si no, no ocurre nada o se ejecutan otras.

#### IF simple

En el siguiente diagrama, si se cumple la condición se ejecutan las instrucciones 1 y 2; si no, las 3 y 4.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/B2.%20Programaci%C3%B3n/images/if_flowchart.png?raw=true" alt="Diagrama de flujo IF" width="500" height="auto"/>
    <p><em>Figura 1: Diagrama de flujo de una sentencia IF. Fuente: Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

Si la condición no se cumple, no ocurre nada. Un ejemplo: un comprador recibe un **20 % de descuento** si su compra es de **100 o más**; si es inferior, no pasa nada.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/B2.%20Programaci%C3%B3n/images/if_flowchart2.png?raw=true" alt="Diagrama de flujo IF" width="500" height="auto"/>
    <p><em>Figura 2: Diagrama de flujo de una sentencia IF. Fuente: Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

```python
purchase_value = float(input("Valor de la compra: "))
discount = 0

if purchase_value >= 100:
    discount = purchase_value * 0.2

print("Descuento:", discount)
```

- Las variables `purchase_value` y `discount` almacenan dinero, por lo que pueden tener **decimales**.
- Como el descuento solo se calcula si se cumple la condición, se **inicializa a 0** para que haya un valor que mostrar si no se calcula.
- En Python, la **indentación** indica qué instrucciones se ejecutan cuando se cumple la condición. Si el `print` no estuviera indentado, se ejecutaría **siempre**, independientemente de la condición.

#### IF - ELSE

Permite añadir instrucciones que se ejecutan cuando la condición se evalúa como **falsa**.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/B2.%20Programaci%C3%B3n/images/if_flowchart3.png?raw=true" alt="Diagrama de flujo IF-ELSE" width="450" height="auto"/>
    <p><em>Figura 3: Diagrama de flujo de IF-ELSE. Fuente: </em></p>
  </div>

```python
if purchase_value >= 100:
    discount = purchase_value * 0.2
else:
    discount = 0
```

#### IF anidados (nested IF)

El bloque de código puede ampliarse incluyendo **otro IF dentro del actual**. Esto se denomina **“nested IF”** ("if" anidado).

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/B2.%20Programaci%C3%B3n/images/if_nested.png?raw=true" alt="Diagrama de flujo IF anidado" width="450" height="auto"/>
    <p><em>Figura 4: Diagrama de flujo de un IF anidado. Fuente: Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

En el ejemplo se añade una variable que decide si el descuento es del **20 %** o del **10 %** según si el comprador es **socio** o no. Como no hace falta mostrar el descuento, también podría calcularse el importe a pagar multiplicando directamente por 0.9 (descuento del 10 %).

```python
purchase_value = float(input("Valor de la compra: "))
member = eval(input("¿Es socio? (True/False): "))

if purchase_value >= 100:
    if member == True:
        discount = purchase_value * 0.2
    else:
        discount = purchase_value * 0.1
else:
    discount = 0
```

> [!WARNING]
> El valor guardado en `member` debe ser **booleano**. Si se usa `bool()` en lugar de `eval()`, el resultado es incorrecto: `bool`

#### IF - ELIF - ELSE (else if)

Hay otra forma de resolver el problema anterior: usar el operador lógico **and** en la condición y encadenar varias condiciones con **else if**.

```python
if purchase_value >= 100 and member:
    discount = purchase_value * 0.2
elif purchase_value >= 100 and not member:
    discount = purchase_value * 0.1
else:
    discount = 0
```

- La **primera condición** exige que se cumplan **ambas** a la vez: ser socio **y** tener una compra de 100 o más. Solo entonces se aplica el 20 %.
- La **segunda condición** (`elif`) vuelve a comprobar ambas, pero ahora para una compra de 100 o más **sin ser socio**, con un descuento del 10 %.
- La rama **`else`** recoge el caso en que la compra **no** llega a 100.

> [!NOTE]
> En Python, `else if` se sustituye por la palabra clave **`elif`**.

#### Otros operadores lógicos (OR y NOT)

Las condiciones pueden usar otros operadores lógicos, como **OR** y **NOT**.

Si se quisiera aplicar el descuento cuando la compra es de 100 o más **o** el comprador es socio, el operador **OR** sustituiría al AND de la condición anterior:

```python
if purchase_value >= 100 or member:
    discount = purchase_value * 0.2
```

Como en el ejemplo anterior, una comparación con un valor verdadero puede escribirse con `if` seguido de la variable a evaluar:

- `if member:` se evalúa como **verdadero** si `member` vale `True`, y como falso en caso contrario.
- `if not member:` devuelve **verdadero** si `member` vale `False` y falso si vale `True`; se lee como “si no es socio”.

#### Operadores relacionales

En las comparaciones también se pueden usar otros operadores relacionales: `==`, `!=`, `<`, `>`, `<=`, `>=`.

> [!NOTE]
> Como `=` se usa para **asignar**, la **igualdad** se comprueba con `==`.

> [!TIP]
> **TdC: ¿cómo afecta el razonamiento a la toma de decisiones?**
>
> El **razonamiento** consiste en analizar, evaluar y extraer conclusiones a partir de hechos, datos y procesos. Son habilidades importantes para decidir bien, porque permiten definir con claridad problemas y objetivos, **seleccionar los detalles relevantes e ignorar los innecesarios**, analizar posibles soluciones, generar ideas y proponer soluciones eficientes.
>
> La palabra “decisión” viene del latín *decidere*, que significa **“cortar”**: para decidir hay que considerar y descartar soluciones alternativas. El razonamiento es clave primero para **identificar las opciones disponibles** y después para **evaluar sus consecuencias**. Sin embargo, la toma de decisiones suele combinar razonamiento con otros factores que pueden limitar la racionalidad, como los **sesgos** y las **emociones**.
>
> Al explorar el papel del razonamiento en la toma de decisiones, discute la importancia de la lógica, el análisis, el pensamiento crítico, las técnicas de resolución de problemas, las habilidades adquiridas y el propósito para llegar a conclusiones bien fundamentadas y eficaces.

<br>

## B2.3.3. Bucles e iteración

Imagina que necesitas mostrar tu nombre varias veces. Al principio podrías hacerlo escribiendo una sentencia `print` por cada repetición, pero este método se vuelve muy incómodo cuando hay muchas repeticiones, por ejemplo 100. Además, si quieres repetir acciones según lo que introduzca el usuario o hasta que se cumpla una condición, escribir cada repetición a mano es inviable. Para resolver estas situaciones de forma eficiente se usan los **bucles**.

Los bucles permiten ejecutar un bloque de código de forma repetida, ya sea un **número predeterminado de iteraciones** o **hasta que se cumpla una condición**. Tanto si se conoce de antemano el número exacto de repeticiones como si hay que iterar dinámicamente según condiciones en tiempo de ejecución, los bucles ofrecen una solución flexible y concisa.

Los bucles se usan para repetir instrucciones o bloques de código. **Un bucle hace referencia a una repetición.** Existen varios tipos:

- **Bucles controlados por contador** (bucles **FOR**).
- **Bucles condicionales**, que pueden ser:
  - **Bucles de precondición** (bucles **WHILE**).
  - **Bucles de postcondición** (bucles **REPEAT–UNTIL**).

<br>

### Bucle controlado por contador (FOR)

Un **bucle controlado por contador** (bucle FOR) se usa cuando **el número de repeticiones se conoce antes de ejecutar el código**. Por ejemplo, si hay que escribir todos los números entre 1 y 100, antes de escribir nada de código ya se sabe que el programa se repetirá 100 veces.

 <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/B2.%20Programaci%C3%B3n/images/count-controlled.png?raw=true" alt="Diagrama de flujo Bucle FOR" width="500" height="auto"/>
    <p><em>Figura 5: Diagrama de flujo Bucle FOR. Fuente: Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

Si `n` es el número de repeticiones necesarias, un bucle FOR tendría este aspecto:

```python
for i in range(0, n):
    print(i)
```

En Python, `range` indica el valor inicial de `i` (en este caso, 0) y el valor final (en este caso, `n`). Ten en cuenta que **el bucle se detiene cuando `i` llega a `n-1`**. Por ejemplo, si `n = 5`, `i` tomará los valores 0, 1, 2, 3, 4. Hay cinco repeticiones en total; cuando `i` alcanza el valor 5, la repetición termina y ese valor no se muestra.

> [!NOTE]
> Como el punto de partida es 0, que es el valor por defecto, la sentencia podría haberse escrito como `for i in range(n):` y tendría el mismo efecto.

El punto de partida se puede cambiar. Supón que hay que mostrar todos los números entre 1 y 100. Para resolverlo, se fija el inicio en 1 y el final en 101, de modo que el 100 también quede incluido:

```python
for i in range(1, 101):
    print(i)
```

Otra alternativa sería mantener el bucle de 0 a 100 y modificar la sentencia de impresión para que muestre `i + 1`:

```python
for i in range(0, 100):
    print(i + 1)
```

#### Números impares entre 1 y 100

Una posible solución es mantener la misma estructura y comprobar si el número es impar:

```python
for i in range(1, 101):
    if i % 2 == 1:
        print(i)
```

`i % 2 == 1` comprueba si el **resto** de dividir `i` entre 2 es 1. Es decir, si hay resto, el número es impar; si no hay resto, es par.

El mismo problema se puede resolver **sin necesidad de un IF**, añadiendo un **paso** (*step*) que cambie el incremento: en lugar de aumentar `i` de 1 en 1 (valor por defecto), se aumenta de otra forma.

```python
for i in range(1, 101, 2):
    print(i)
```

Aquí se ha incluido un paso de `2` en `range`, de modo que la variable `i` tomará los valores 1, 3, 5, … 99.

#### Números de 100 a 1 (cuenta atrás)

¿Y si se pide mostrar los números de 100 a 1?

```python
for i in range(100, 0, -1):
    print(i)
```

El rango empieza en 100 y debe detenerse al llegar a 1 (el 0 no se alcanza), y el paso se fija en `-1` para que el número se **decremente** de uno en uno.

> [!NOTE]
> **Sintaxis de `range` en Python:** `range(inicio, fin, paso)`
> - `inicio`: primer valor (por defecto, 0).
> - `fin`: valor en el que se detiene el bucle (**no se incluye**).
> - `paso`: cuánto cambia `i` en cada repetición (por defecto, 1).

<br>

### Bucle de precondición (WHILE)

Un **bucle de precondición** (WHILE) se usa cuando **el número de repeticiones no se conoce antes de ejecutar el código**. Se espera que el código se repita **mientras se cumpla una condición**, es decir, mientras se evalúe como verdadera.

Cuando la condición deja de cumplirse, llamada **condición de terminación**, la ejecución del bucle se detiene. En un bucle WHILE puede que **la repetición no se ejecute ni una sola vez**: esto ocurre cuando la condición nunca se cumple.

 <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/B2.%20Programaci%C3%B3n/images/pre-condition.png?raw=true" alt="Diagrama de flujo Bucle Pre-Condición" width="500" height="auto"/>
    <p><em>Figura 6: Diagrama de flujo Bucle pre-condición. Fuente: Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

Los bucles WHILE se utilizan con frecuencia con fines de **validación** o **verificación**. Por ejemplo, cuando se pide al usuario que introduzca una contraseña dos veces, el ordenador compara ambas entradas para comprobar que coinciden (**verificación de doble entrada**). En este caso, se usaría un bucle para repetir la introducción de la contraseña hasta que las dos entradas coincidan.

> [!NOTE]
> - **Condición de terminación:** condición de un bucle que interrumpe o detiene la repetición.
> - **Validación:** proceso para asegurar que los datos de entrada son sensatos o razonables.
> - **Verificación:** proceso para asegurar que los datos de entrada se han copiado con exactitud de una fuente a otra.

```python
password = input("Introduce la contraseña: ")
pass_check = input("Repite la contraseña: ")

while password != pass_check:
    print("Las contraseñas no coinciden.")
    pass_check = input("Repite la contraseña: ")

print("Contraseña verificada.")
```

- `!=` es una **negación** de la igualdad: la condición comprueba si los dos valores **no son iguales**, y se pide al usuario que vuelva a introducir la contraseña hasta que coincidan.
- En Python, tanto para cadenas de texto como para números se usa `==` / `!=` para comparar.
- El mensaje final solo se muestra **después de salir del bucle**.
- Si la segunda contraseña nunca coincide con la primera, el código del interior del bucle se repetirá continuamente.

#### Convertir un FOR en un WHILE

**Cualquier bucle FOR puede reescribirse como un bucle WHILE.** Con el ejemplo que muestra todos los números entre 1 y 100, usando un WHILE el código sería:

```python
i = 1
while i < 101:
    print(i)
    i = i + 1
```

- El bucle se repetirá **mientras `i` sea menor que 101**. La condición de terminación es `i >= 101`.
- La función del incremento (`i = i + 1`) es cambiar el valor de `i` para que el bucle se detenga en algún momento. Sin esa sentencia, el bucle se ejecutaría **de forma infinita**.

<br>

### Bucle de postcondición (REPEAT–UNTIL)

En el **bucle de postcondición** (REPEAT–UNTIL), la condición se comprueba **al final**. Por tanto, el código del interior del bucle se ejecuta **al menos una vez**.

 <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/B2.%20Programaci%C3%B3n/images/post-condition.png?raw=true" alt="Diagrama de flujo Bucle Post-Condición" width="500" height="auto"/>
    <p><em>Figura 7: Diagrama de flujo Bucle post-condición. Fuente: Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

> [!NOTE]
> En Python, las estructuras de postcondición se escriben usando bucles `while`, ya que no existe una sentencia `repeat–until` propia. Se suele usar `while True` junto con `break` para salir del bucle cuando se cumple la condición de terminación.

```python
i = 1
while True:
    print(i)
    i = i + 1
    if i > 100:
        break
```

En el ejemplo, la variable `i` se inicializa a 1. Ese valor se muestra y después se incrementa, **ocurra lo que ocurra con la condición**. Si la condición de terminación (`i > 100`) se evalúa como falsa, el bucle se repite; si se evalúa como verdadera, la repetición se detiene.

<br>

> [!IMPORTANT]
> **Información clave**
>
> - Los bucles FOR se llaman bucles **“controlados por contador”**, los bucles WHILE se llaman bucles **“de precondición”** y los bucles REPEAT–UNTIL se llaman bucles **“de postcondición”**.
> - Los bucles controlados por contador se usan cuando **el número de repeticiones se conoce antes de ejecutar el código**.
> - Los bucles de precondición **pueden no ejecutarse ni una vez** (si la condición no se cumple).
> - Los bucles de postcondición se ejecutan **al menos una vez**, aunque la condición nunca se cumpla.

> [!TIP]
> **Consejo**
>
> Cuando se te pida identificar el tipo de bucle que ejemplifica un fragmento de código, utiliza los nombres **controlado por contador**, **de precondición** o **de postcondición**. Por ejemplo, decir que es un “bucle FOR” en lugar de un bucle “controlado por contador” no es suficiente, ya que no queda claro que sepas de qué tipo de bucle se trata un FOR.

<br>
