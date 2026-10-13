<h1 align="center">B2.3. Estructuras de control de programación
<div align="center">

</div>

## Contenido:

- [B2.3.1. Secuenciación](#B231-secuenciación)
- [B2.3.2. Estructuras de selección](#B232-estructuras-de-selección)

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
    <p><em>Figura 1: Diagrama de flujo de una sentencia IF. Fuente: </em></p>
  </div>

Si la condición no se cumple, no ocurre nada. Un ejemplo: un comprador recibe un **20 % de descuento** si su compra es de **100 o más**; si es inferior, no pasa nada.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/B2.%20Programaci%C3%B3n/images/if_flowchart2.png?raw=true" alt="Diagrama de flujo IF" width="500" height="auto"/>
    <p><em>Figura 2: Diagrama de flujo de una sentencia IF. Fuente: </em></p>
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
    <p><em>Figura 4: Diagrama de flujo de un IF anidado. Fuente: </em></p>
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
