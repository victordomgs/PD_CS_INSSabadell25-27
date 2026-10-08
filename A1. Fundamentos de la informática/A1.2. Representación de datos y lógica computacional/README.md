<h1 align="center">A1.2. Representación de datos y lógica computacional
<div align="center">

</div>

## Contenido:

- [A1.2.1. Describe los principales métodos de representación de datos](#A121-describe-los-principales-métodos-de-representación-de-datos)  
- [A1.2.2. Explica cómo se utiliza el sistema binario para almacenar datos](#A122-explica-cómo-se-utiliza-el-sistema-binario-para-almacenar-datos)
- [A1.2.3. Describe el propósito y el uso de las puertas lógicas](#A123-describe-el-propósito-y-el-uso-de-las-puertas-lógicas)
- [A1.2.4. Construye y analiza tablas de la verdad](#A124-construye-y-analiza-tablas-de-la-verdad)
- [A1.2.5 Construye diagramas lógicos](#A125-construye-diagramas-lógicos)

<br>

## A1.2.1. Describe los principales métodos de representación de datos

El sistema binario (base 2) es el lenguaje de los ordenadores modernos; sin embargo, no siempre fue así. Durante el desarrollo de los primeros ordenadores se probaron varios sistemas numéricos. Charles Babbage, el inventor de la Máquina Analítica, utilizó el sistema decimal en sus invenciones. Esto parecía una elección lógica, ya que las personas ya usaban comúnmente la base 10.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2020.%20The%20analytical%20engine.jpg" alt="Engine" width="450" height="auto"/>
    <p><em>Figura 20: The Analytical Engine. Fuente: Wikipedia</em></p>
  </div>

También se exploró el sistema ternario (base 3). El ordenador Setun, desarrollado en la Unión Soviética en 1958, utilizaba este sistema. Se produjeron más de 50 unidades para instituciones educativas y científicas con el fin de investigar los beneficios de la lógica ternaria en la computación. A pesar de su enfoque innovador, los desafíos prácticos y la adopción generalizada de la lógica binaria acabaron por llevar a su sustitución.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2021.%20The%20Setun%20Computer%2C%20desarrollado%20en%201958.png" alt="Setun Computer" width="350" height="auto"/>
    <p><em>Figura 21: The Setun computer, desarrollado en 1958. Fuente: Wikipedia</em></p>
  </div>

Otros científicos e inventores también exploraron sistemas cuaternarios (base 4) y otros sistemas numéricos. Sin embargo, las implementaciones prácticas de estos sistemas fueron escasas debido a la mayor complejidad del diseño del hardware y a los beneficios limitados en comparación con el binario.

En última instancia, la informática moderna adoptó el **sistema binario (base 2)** como el sistema numérico principal. El sistema base 2 representa dos estados posibles: **1 o 0**. Esto contrasta con el sistema decimal (base 10), con el que todos estamos familiarizados, que tiene diez estados posibles: del 0 al 9.

El sistema binario es especialmente adecuado para representar el estado de los **interruptores eléctricos** dentro de un sistema informático: encendido (1) y apagado (0). Esta simplicidad reduce la complejidad del hardware y mejora la fiabilidad.

El binario reduce la complejidad del diseño de hardware porque la electrónica digital, como los **transistores**, funciona de forma natural en modo binario. Los transistores actúan como interruptores que pueden estar encendidos o apagados, lo que se ajusta perfectamente a la lógica de dos estados del sistema binario.

Además, el **álgebra de Boole**, el marco matemático para el diseño y funcionamiento de los circuitos lógicos, permite la implementación sencilla de operaciones complejas mediante **puertas lógicas simples** con entradas binarias: 1 (encendido / verdadero) o 0 (apagado / falso).

La mayor fiabilidad de los sistemas binarios se debe a que utilizan solo dos estados. Las pequeñas variaciones en la intensidad de la señal no afectan tanto a la integridad de los datos como en los sistemas que usan bases mayores, lo que hace que el binario sea más **robusto en entornos con ruido**.

> [!NOTE]  
> - **Ruido:** perturbaciones eléctricas no deseadas que pueden afectar la integridad de las señales procesadas por un ordenador; este ruido no está relacionado con el sonido, sino con variaciones en el voltaje o la corriente que pueden alterar la transmisión y el procesamiento precisos de los datos digitales.
> - **Bit:** dígito binario; una sola cifra, ya sea 1 o 0.
> - **Byte:** conjunto de 8 bits.

Dado que **todos los datos en un sistema informático se almacenan en binario**, necesitamos sistemas que permitan representar distintos tipos de datos —como números enteros, cadenas, caracteres, imágenes, audio y vídeo— en forma binaria.

### Representación de números enteros en binario

Para representar números en binario, es útil recordar los fundamentos de nuestro sistema decimal (base 10).

En el sistema decimal, al contar, comenzamos con un solo dígito y lo incrementamos en 1 hasta llegar a 9.

Después del 9, añadimos un nuevo dígito delante para representar números mayores.

Desglosemos el número decimal **1024**:

| Miles | Cientos | Decenas | Unidades |
|:------:|:--------:|:--------:|:----------:|
| 1 | 0 | 2 | 4 |

Esto se puede expresar como:
(1 × 1000) + (0 × 100) + (2 × 10) + (4 × 1) = **1024**

Cada posición decimal aumenta por múltiplos de 10 al movernos hacia la izquierda porque trabajamos en base 10.

El sistema binario, y otros sistemas de base diferente, funcionan de manera similar, pero en lugar de 10 posibles estados por dígito, el binario solo tiene **dos (0 y 1)**.

Por tanto, cada posición aumenta por múltiplos de 2.

Desglosemos el número binario **0110**:

| 8s | 4s | 2s | 1s |
|:--:|:--:|:--:|:--:|
| 0 | 1 | 1 | 0 |

Esto se puede expresar como:
(0 × 8) + (1 × 4) + (1 × 2) + (0 × 1) = 6

En este ejemplo, no tenemos ochos, tenemos un cuatro, un dos y ninguna unidad.
Sumando 4 + 2 obtenemos el equivalente decimal (base 10) del número binario (base 2) 0110.

Para dejar claro si mostramos un número binario o decimal, solemos poner la base como subíndice para evitar confusiones:

**0110₂ = 6₁₀**

Cuando trabajamos con sistemas informáticos, normalmente usamos **números binarios de 8 bits**.

Un **bit** se define como un “dígito binario”, y **8 bits equivalen a 1 byte**.

Si el número no necesita 8 bits para representarse, normalmente completamos los bits restantes con ceros.

Por ejemplo, el número decimal **33** se representaría así:

| 128s | 64s | 32s | 16s | 8s | 4s | 2s | 1s |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 0 | 0 | 1 | 0 | 0 | 0 | 0 | 1 |

> [!WARNING]  
> Al ver el número **11111111₂**, un error común es decir que equivale a **256**. Sin embargo, aunque hay **256 combinaciones posibles, 255** es el número más grande que podemos representar en 1 byte (ya que el 0 también se puede representar).

Cuando nos referimos a bits y bytes:

- La **“b” minúscula (b)** representa **bits**.
- La **“B” mayúscula (B)** representa **bytes**.

A medida que aumentan los valores, utilizamos prefijos. Existen **dos tipos de prefijos** al referirnos a bits y bytes:

- Para **base 10** (por ejemplo: kilo, mega, giga)
- Para **base 2** (por ejemplo: kibi, mebi, gibi)

Durante un tiempo se usaron los prefijos de base 10 también para cantidades en base 2 debido a su similitud (por ejemplo, 1024 ≈ 1000). Sin embargo, esto generó confusión, por lo que en **1999 la IEC** introdujo nuevos prefijos (kibi, mebi, gibi) específicamente para múltiplos de base 2.

#### Prefijos binarios (base 2)

| Unidad | Abreviatura | Equivalencia |
|:--------|:-------------|:--------------|
| Kibibyte | KiB | 1 KiB = 1024 bytes |
| Mebibyte | MiB | 1 MiB = 1024 KiB |
| Gibibyte | GiB | 1 GiB = 1024 MiB |
| Tebibyte | TiB | 1 TiB = 1024 GiB |
| Pebibyte | PiB | 1 PiB = 1024 TiB |
| Exbibyte | EiB | 1 EiB = 1024 PiB |
| Zebibyte | ZiB | 1 ZiB = 1024 EiB |

#### Prefijos binarios (base 10)

| Unidad | Abreviatura | Equivalencia |
|:--------|:-------------|:--------------|
| Kilobyte | KB | 1 KB = 1000 bytes |
| Megabyte | MB | 1 MB = 1000 KB |
| Gigabyte | GB | 1 GB = 1000 MB |
| Terabyte | TB | 1 TB = 1000 GB |
| Petabyte | PB | 1 PB = 1000 TB |
| Exabyte | EB | 1 EB = 1000 PB |
| Zettabyte | ZB | 1 ZB = 1000 EB |

### Convertir números binarios a números decimales

Existen **dos métodos principales** para convertir un número binario a decimal:

- El **método de notación posicional**.
- El **método de duplicación**.

#### Método de notación posicional

Este es probablemente el método más directo, en el que se asignan los valores de posición y se suman.

**Pasos:**

1. Comenzando por la derecha, asigna los valores posicionales a cada bit binario.
2. Suma todos los valores posicionales que tengan un **1** debajo.

Por ejemplo, para convertir **10111011₂** a decimal:

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 1 | 0 | 1 | 1 | 1 | 0 | 1 | 1 |

Cálculo:

(1×128) + (0×64) + (1×32) + (1×16) + (1×8) + (0×4) + (1×2) + (1×1) = **187**

#### Método de duplicación

**Pasos:**

1. Empieza con el bit más a la izquierda (el bit más significativo, MSB).
2. Duplica el total actual y suma el siguiente bit.
3. Repite el proceso hasta procesar todos los bits.

| Paso | Dígito binario | Total actual | Cálculo |
|:----:|:---------------:|:-------------:|:---------|
| 1 | 1 | 1 | Valor inicial |
| 2 | 0 | 2 | 1 × 2 + 0 = 2 |
| 3 | 1 | 5 | 2 × 2 + 1 = 5 |
| 4 | 1 | 11 | 5 × 2 + 1 = 11 |
| 5 | 1 | 23 | 11 × 2 + 1 = 23 |
| 6 | 0 | 46 | 23 × 2 + 0 = 46 |
| 7 | 1 | 93 | 46 × 2 + 1 = 93 |
| 8 | 1 | 187 | 93 × 2 + 1 = 187 |

Resultado: 10111011₂ = 187₁₀

> [!WARNING]  
> Si utilizas este método, recuerda **comenzar con el bit más significativo (MSB)** y no con el bit menos significativo (LSB).

> [!NOTE]  
> - **Bit menos significativo (LSB):** el bit situado más a la derecha en un número binario, que representa la posición de menor valor (0 o 1).
> - **Cociente:** el resultado que se obtiene al dividir un número entre otro; por ejemplo, en la división de 15 entre 3, el cociente es 5.

### Convertir números decimales a números binarios

Existen **dos métodos principales** para convertir un número decimal a binario:

- El **método de división**.
- El **método de sustracción**.

#### Método de división

**Pasos:**

1. Divide el número decimal entre 2.
2. Anota el cociente y el resto. El resto será 0 o 1, y representa un dígito del número binario (el LSB o bit menos significativo en la primera división).
3. Actualiza el cociente.
4. Repite hasta que el cociente sea 0.
5. Construye el número binario **leyendo los restos desde el primero hasta el último**.

Por ejemplo, para convertir **42₁₀** a binario:

| Paso de división | Cálculo | Cociente | Resto |
|:-----------------:|:--------|:----------:|:--------:|
| 1 | 42 ÷ 2 | 21 | 0 |
| 2 | 21 ÷ 2 | 10 | 1 |
| 3 | 10 ÷ 2 | 5 | 0 |
| 4 | 5 ÷ 2 | 2 | 1 |
| 5 | 2 ÷ 2 | 1 | 0 |
| 6 | 1 ÷ 2 | 0 | 1 |

Construimos el número binario a partir de los restos (de abajo hacia arriba) y lo completamos a 8 bits:

`00101010₂`

> [!WARNING]  
> Recuerda construir el número binario **en el orden correcto** a partir de los restos. El **primer resto** corresponde al **bit menos significativo (LSB)**.

#### Método de sustracción

Primero, escribe los valores posicionales para un número binario de 8 bits:

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|

Comenzando con el valor más grande (128):

**Pasos:**

1. Intenta restarlo del número que deseas convertir.

- Si el valor posicional es **mayor** que el número, escribe un **0** debajo.
- Si es **menor o igual**, escribe un **1** y calcula el resto de la resta, que será el número con el que continuarás.

2. Repite el proceso para cada valor posicional.

Por ejemplo, para convertir **42₁₀** a binario:

Los valores **128₁₀** y **64₁₀** son mayores que 42₁₀, así que escribimos 0 debajo.
El siguiente valor, **32₁₀**, es menor, así que escribimos un 1 y restamos:
42₁₀ – 32₁₀ = 10₁₀

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 0 | 0 | 1 |   |   |   |   |   |

Continuamos con **10₁₀**:

- 16₁₀ es mayor → 0
- 8₁₀ es menor → 1
- 10₁₀ – 8₁₀ = 2₁₀
- 4₁₀ es mayor → 0
- 2₁₀ es igual → 1
- Resto 0

El resultado final es:

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 0 | 0 | 1 | 0 | 1 | 0 | 1 | 0 |

Resultado:

`42₁₀ = 00101010₂`

<br>

## Representación de números enteros en hexadecimal

El sistema **hexadecimal** (a menudo abreviado como **hex**) es un sistema numérico de **base 16** que utiliza 16 símbolos distintos para representar valores, en lugar de los 10 del sistema decimal o los 2 del sistema binario.

Los símbolos utilizados son los dígitos del **0 al 9** y las letras **A a F**, donde:

| Hexadecimal | Decimal |
|:-----------:|:-------:|
| A | 10 |
| B | 11 |
| C | 12 |
| D | 13 |
| E | 14 |
| F | 15 |

El sistema hexadecimal se utiliza ampliamente en informática por varias razones.

La conversión entre binario y hexadecimal es especialmente sencilla porque **cada dígito hexadecimal corresponde exactamente a 4 bits**. Por ejemplo, el número binario **1111₂** puede representarse como **F₁₆**.

Otra ventaja es que proporciona una forma mucho más compacta de representar números binarios. Esto facilita enormemente la lectura y la comunicación de valores binarios largos. Por esta razón, el hexadecimal se utiliza con frecuencia en:

- Herramientas de depuración (*debugging tools*).
- Volcados de memoria (*memory dumps*).
- Programación en lenguaje ensamblador (*assembly language*).

> [!NOTE]
> - **Herramientas de depuración (debugging tools):** aplicaciones o utilidades utilizadas por los desarrolladores para identificar, analizar y corregir errores en un programa inspeccionando el código, las variables y el flujo de ejecución.
> - **Volcado de memoria (memory dump):** proceso mediante el cual se captura y almacena el contenido de la memoria de un ordenador, normalmente con fines de diagnóstico y depuración de software.
> - **Nibble:** grupo de 4 bits.

### Convertir números binarios a hexadecimales

La conversión de binario a hexadecimal es un cálculo sencillo.

**Pasos:**

1. Divide el byte binario (8 bits) en dos *nibbles* (2 × 4 bits).
2. Calcula el valor decimal de cada grupo de 4 bits.
3. Convierte esos valores decimales a sus equivalentes hexadecimales y únelos.

Por ejemplo, para convertir **01101011₂** a hexadecimal:

#### Paso 1: Dividir en dos nibbles

| Primer nibble | Segundo nibble |
|:-------------:|:--------------:|
| 0110₂ | 1011₂ |

#### Paso 2: Calcular el valor decimal

| Binario | Decimal |
|:--------:|:--------:|
| 0110₂ | 6₁₀ |
| 1011₂ | 11₁₀ |

#### Paso 3: Convertir a hexadecimal

| Decimal | Hexadecimal |
|:--------:|:------------:|
| 6₁₀ | 6₁₆ |
| 11₁₀ | B₁₆ |

Resultado:

**01101011₂ = 6B₁₆**

### Convertir números hexadecimales a binarios

La conversión de hexadecimal a binario es simplemente el proceso inverso.

**Pasos:**

1. Separa los dos dígitos hexadecimales.
2. Convierte cada uno a un número binario de 4 bits.
3. Une ambos grupos para formar un byte completo.

Por ejemplo, para convertir **F2₁₆** a binario:

#### Paso 1: Separar los dígitos

| Dígito 1 | Dígito 2 |
|:---------:|:---------:|
| F₁₆ | 2₁₆ |

#### Paso 2: Convertir cada dígito a binario

| Hexadecimal | Binario |
|:-----------:|:-------:|
| F₁₆ | 1111₂ |
| 2₁₆ | 0010₂ |

#### Paso 3: Unir los grupos

```text
1111 0010
```

Resultado:

**F2₁₆ = 11110010₂**

### Convertir números decimales a hexadecimales

La conversión de decimal a hexadecimal requiere trabajar con divisiones sucesivas entre 16.

**Pasos:**

1. Divide el número decimal entre 16 y anota el resto.
2. Repite el proceso utilizando el cociente obtenido.
3. Continúa hasta que el cociente sea 0.
4. Construye el número hexadecimal leyendo los restos desde el último hasta el primero.

Por ejemplo, para convertir **254₁₀** a hexadecimal:

#### Paso 1: Primera división

| División | Cociente | Resto |
|:----------|:---------:|:------:|
| 254 ÷ 16 | 15 | 14 |

El resto **14₁₀** equivale a **E₁₆**.

#### Paso 2: Segunda división

| División | Cociente | Resto |
|:----------|:---------:|:------:|
| 15 ÷ 16 | 0 | 15 |

El resto **15₁₀** equivale a **F₁₆**.

#### Paso 3: Construir el resultado

Leyendo los restos desde el último hasta el primero:

**FE₁₆**

Resultado:

**254₁₀ = FE₁₆**

### Convertir números hexadecimales a decimales

Para convertir un número hexadecimal a decimal:

**Pasos:**

1. Convierte cada dígito hexadecimal a su equivalente decimal.
2. Multiplica cada valor por **16 elevado a la potencia correspondiente a su posición**, empezando por 0 desde la derecha.
3. Suma todos los resultados.

Por ejemplo, para convertir **2F₁₆** a decimal:

#### Paso 1: Convertir los dígitos

| Hexadecimal | Decimal |
|:-----------:|:-------:|
| 2₁₆ | 2₁₀ |
| F₁₆ | 15₁₀ |

#### Paso 2: Aplicar los pesos posicionales

| Cálculo | Resultado |
|:---------|:----------:|
| 2 × 16¹ | 32 |
| 15 × 16⁰ | 15 |

#### Paso 3: Sumar los resultados

```text
32 + 15 = 47
```

Resultado:

**2F₁₆ = 47₁₀**

## A1.2.2. Explica cómo se utiliza el sistema binario para almacenar datos

El sistema binario sustenta todo, desde los valores numéricos y la información textual hasta los archivos multimedia complejos, garantizando un procesamiento de datos eficiente y fiable. En esta sección, vamos a descubrir los mecanismos que se utilizan para almacenar datos como caracteres, cadenas de texto, imágenes, audio y vídeo en forma binaria.

### Caracteres y cadenas de texto

Los caracteres y las cadenas se almacenan utilizando esquemas de codificación binaria estandarizados, lo que permite un almacenamiento, recuperación y procesamiento coherentes entre distintos sistemas y aplicaciones. Los estándares de codificación más comunes son **ASCII** (American Standard Code for Information Interchange, Código Estándar Americano para el Intercambio de Información) y **Unicode**.

#### Codificación ASCII

El desarrollo del ASCII comenzó en 1960 y fue oficialmente estandarizado en 1963. Se desarrolló porque no existía una forma estandarizada de codificar los caracteres de texto, lo que provocaba problemas de compatibilidad entre dispositivos y sistemas. Cada fabricante utilizaba su propio sistema de codificación propietario, lo que hacía muy difícil la comunicación entre dispositivos. ASCII fue diseñado para proporcionar un estándar común para el intercambio de datos de texto.

Inicialmente, ASCII se creó como un sistema de codificación de **7 bits**, lo que le daba la capacidad de representar **128 (2⁷)** caracteres diferentes, considerados suficientes para la mayoría de los textos básicos (letras, números, signos de puntuación y caracteres de control). Sin embargo, a medida que la informática se globalizó y las aplicaciones necesitaron soporte para caracteres adicionales, se desarrolló una **extensión de 8 bits** del ASCII, que le permitió representar **256 (2⁸)** caracteres. Esta ampliación se conoció como **ASCII extendido**, y los nuevos caracteres se utilizaron principalmente para los idiomas de Europa Occidental.

ASCII utiliza un sistema sencillo pero ingenioso para representar caracteres en binario (siempre que solo consideremos el alfabeto latino, es decir, el inglés). **Los cinco primeros bits empezando por la derecha** se usan para representar la letra según su posición numérica en el alfabeto.

Los tres primeros bits por la izquierda representan si se trata de una letra mayúscula o minúscula.

011 = minúscula; 010 = mayúscula.

Por ejemplo:
01100001₂ = a
01000001₂ = A

> [!TIP]  
> Si los **cinco primeros bits por la derecha** son **00000** (cinco ceros), casi con toda seguridad se trata de un **espacio (00100000)**. Si los **tres primeros bits por la izquierda no son 011 ni 010**, es probable que se trate de un **signo de puntuación**.

#### Review exercice

Vamos a convertir el siguiente código binario en el mensaje correspondiente. Siguiendo el estándar ASCII:

01000110 01101111 01101100 01101100 01101111 01110111 00100000 01110100 01101000 01100101 00100000 01110111 01101000 01101001 01110100 01100101 00100000 01110010 01100001 01100010 01100010 01101001 01110100

#### Codificación Unicode

En la década de **1960**, los Estados Unidos y la mayoría de los países de habla inglesa utilizaban un sistema **ASCII de 7 bits** que funcionaba bien para el alfabeto inglés. Otros países no angloparlantes tenían sus propios sistemas de codificación únicos adaptados a sus respectivos idiomas.

Cuando el sistema ASCII se amplió a **8 bits** (ASCII extendido), permitiendo representar **256 caracteres** en los ordenadores modernos, los distintos países **no se pusieron de acuerdo en un mismo estándar**.
Los países nórdicos comenzaron a usar el espacio adicional para codificar los caracteres de sus propios idiomas, y **Japón llegó a utilizar cuatro sistemas diferentes** que ni siquiera eran compatibles entre sí.

Esto no representaba un gran problema mientras la comunicación entre sistemas fuera poco común, pero cuando **se lanzó Internet**, la compatibilidad pasó a ser **muy importante**, ya que cada vez se compartía más información entre sistemas de distintos países.

En **1991**, se creó el **Unicode Consortium** con el objetivo de resolver este problema. Esta organización se estableció para **desarrollar, mantener y promover el Estándar Unicode**, que asigna **un número único a cada carácter**, independientemente de la plataforma, el programa o el idioma.

Era necesario crear un sistema capaz de **almacenar todos los caracteres y signos de puntuación de todos los idiomas del mundo**, pero que además fuera **compatible hacia atrás con ASCII**.

En el momento de redactar este texto, la versión actual del estándar, **Unicode 15.0** (publicada en **septiembre de 2022**), codifica **149.186 caracteres diferentes**.

Unicode incluye los alfabetos **latino, cirílico, griego y árabe**, los **caracteres chinos**, así como muchos otros, e incluso **emojis** y **símbolos matemáticos y técnicos**.

En Unicode, **cada letra o símbolo tiene asignado un número único**, por ejemplo:

- A = 65
- 汉 = 27721 
- 💩 = 128169

#### 🧠💻 Programming exercise

Puedes encontrar la representación numérica de cualquier carácter o símbolo utilizando el siguiente código:

```python
# Python examples
char_a = 'A'
char_han = '汉'
char_poo = '💩'

# Get Unicode code points as integers
code_point_a = ord(char_a)      # 65
code_point_han = ord(char_han)  # 27721
code_point_poo = ord(char_poo)  # 128169

# Print integer representations
print(code_point_a)      # Output: 65
print(code_point_han)    # Output: 27721
print(code_point_poo)    # Output: 128169
```

En cuanto a cómo se ideó, la historia cuenta que fue **concebido en una cafetería, en la parte trasera de una servilleta**, cuando **Joe Becker (Xerox)**, **Lee Collins (Apple)** y **Mark Davis (Apple y más tarde Google)** se reunieron y diseñaron el esquema de codificación en **1987**.

Existen **varias versiones de Unicode: UTF-8, UTF-16 y UTF-32**.

Cada una tiene sus propios usos:

|                         | **UTF-8** | **UTF-16** | **UTF-32** |
|-------------------------|-----------|-------------|-------------|
| **Codificación de longitud variable** | 1–4 bytes por carácter | 2 o 4 bytes por carácter | 4 bytes por carácter |
| **Nota** | Compatibilidad: compatible hacia atrás con ASCII | Pares sustitutos: para los caracteres fuera del *Plano Multilingüe Básico (BMP)*, se utilizan dos unidades de código de 16 bits | Simplicidad: más fácil de procesar porque cada carácter ocupa exactamente 4 bytes |
| **Uso** | Codificación más utilizada en la web y en muchas aplicaciones | Frecuente en entornos Windows y Java | Menos común debido a los mayores requisitos de almacenamiento |

Examinemos **UTF-8**, el sistema de codificación más utilizado, para comprender su funcionamiento.

En lugar de simplemente ampliar el tamaño para admitir más de **100.000 caracteres**, lo que habría afectado negativamente a la mayoría del contenido en línea, se ideó una solución más eficiente.

Si todos los caracteres se hubieran estandarizado para usar **32 bits, cada letra del sistema ASCII habría cuadruplicado su tamaño**. Esto habría dado lugar a documentos y páginas web significativamente más grandes, lo que implicaría **mayores necesidades de almacenamiento y tiempos de transferencia más lentos**.

Además, el sistema debía evitar **enviar ocho ceros seguidos (00000000)**, ya que muchos sistemas antiguos interpretaban esto como el **fin de la comunicación** y dejaban de escuchar.

Por ello, el sistema **UTF-8 mantuvo el sistema ASCII tal cual**.

La letra **“A”** se codifica como:

**01000001 = A**

Sin embargo, si el carácter requerido va más allá del sistema ASCII estándar —por ejemplo, “é”—, se necesita **más de un byte**:

**11000011 10101001 = é**

Los bits en **negrita** son importantes:

- Los **tres primeros bits significativos “110”** del primer byte indican que **este carácter está formado por dos bytes en total** (se necesita un 0 al final para indicar que la información ha terminado).
- El **segundo byte comienza con “10”**, lo que significa que **es una continuación**.

Si se eliminan esos 5 bits de control y se combinan ambos bytes:

**000 1110 1001 = 233 = é**

Otro ejemplo es:

11110000 10011111 10011000 10000100 = 😄

Este emoji requiere **cuatro bytes** utilizando el sistema **UTF-8**. El **primer byte** indica que este carácter está compuesto por **cuatro bytes** (los bits iniciales **“11110”** lo señalan), y los **tres bytes siguientes** comienzan con **“10”**, lo que muestra que son **bytes de continuación**. Si eliminamos esa información de control:

0001 1111 0110 0000 0100 = 128516 = 😄

UTF-8 ha sido adoptado por Internet como el **principal sistema de codificación de caracteres**; sin embargo, **no está exento de algunos inconvenientes**.

Debido a su **longitud variable**, algunos caracteres —especialmente los de **idiomas asiáticos** o los **emojis**— ocupan **más espacio** en comparación con las codificaciones de **un solo byte**. Esto puede provocar **tamaños de archivo mayores** en ciertos contextos.

Además, el procesamiento necesario para manejar una codificación de longitud variable es **más complejo** que en los sistemas de **longitud fija**, como **UTF-32**.

A pesar de estos inconvenientes, **UTF-8 ha demostrado ser un estándar de codificación versátil y eficaz** que satisface las necesidades de la Internet moderna. Su **compatibilidad retroactiva, eficiencia y amplio soporte** lo convierten en una **opción duradera** para la codificación de texto.

Aunque presenta algunos desafíos, especialmente en el manejo de **caracteres no ASCII** y de la **codificación de longitud variable**, estos **no son lo suficientemente importantes** como para justificar su reemplazo completo.

Por lo tanto, es probable que **UTF-8 siga siendo el estándar de codificación de texto dominante** en un futuro previsible.

> [!NOTE]  
> **Cifrado por desplazamiento (Shift cipher):** es un tipo de cifrado por sustitución, en el que cada letra del texto original (texto plano) se desplaza un cierto número de posiciones hacia arriba o hacia abajo en el alfabeto.

#### 🧠💻 Programming exercise

El siguiente código utiliza un cifrado César para encriptar una cadena de texto introducida por el usuario usando una clave. Un cifrado César es un tipo de cifrado por desplazamiento simple, en el que cada letra se considera un número entero (a = 1, b = 2, c = 3, etc.), y la clave se suma a ese valor para obtener la letra cifrada.

```python
def caesar_cipher_encrypt(message, key):
    encrypted_message = ""
    for char in message:
        if char.isalpha():  # Comprueba si el carácter es una letra
            shift = ord("A") if char.isupper() else ord("a")  # Determina el desplazamiento ASCII
            # Desplaza el carácter y vuelve al inicio del alfabeto si es necesario
            encrypted_char = chr((ord(char) - shift + key) % 26 + shift)
            encrypted_message += encrypted_char
        else:
            encrypted_message += char  # Los caracteres que no son letras se mantienen sin cambios
    return encrypted_message

# Entrada del usuario
message = input("Enter the message to encrypt: ")
key = int(input("Enter the key (an integer): "))

# Encripta el mensaje
encrypted_message = caesar_cipher_encrypt(message, key)
print(f"Encrypted message: {encrypted_message}")
```

> [!NOTE]  
> **Fuerza bruta:** un método para romper un cifrado probando sistemáticamente todas las claves posibles hasta encontrar la correcta.

### Imágenes

En 1957, Russel Kirch escaneó una fotografía analógica de su hijo Walden, convirtiendo la imagen en un archivo digital. Esta fue la primera imagen digital creada en la historia.

Se trató de un hito significativo en la evolución de la tecnología visual, que revolucionó la forma en que capturamos, almacenamos y manipulamos las imágenes.

El desarrollo de las primeras cámaras y escáneres digitales, que permitieron a los dispositivos convertir la luz en datos digitales, inició una tendencia que hoy en día se ha vuelto común.

La transición del formato de película al digital ha transformado numerosas industrias, desde la fotografía y la imagen médica hasta las telecomunicaciones y el entretenimiento.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2022.%20La%20primera%20imagen%20digital%20escaneada%20en%201957.jpg" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 22: La primera imagen digital escaneada en 1957. Fuente: Wikipedia</em></p>
  </div>

#### Imágenes de mapa de bits (Bitmap images)

Las **imágenes de mapa de bits**, también conocidas como **imágenes rasterizadas (raster images)**, son una de las formas más fundamentales de gráficos digitales. Reproducen las imágenes mediante una **rejilla de píxeles**, donde **cada píxel tiene asignado un color y una intensidad específicos**.

Al final de la página se muestra una imagen bitmap con una **resolución de 13×10 píxeles** (13 píxeles de ancho por 10 de alto). Cada píxel se **“describe” utilizando 1 bit de información:** puede ser **1 o 0**.

En este caso:

- **1 = negro**
- **0 = blanco** (es decir, una imagen monocroma).

La cantidad de bits usados para describir el color se conoce como **“profundidad de bits”** o **“profundidad de color”**. Por lo tanto, en este ejemplo tenemos una **imagen de 13×10 píxeles** con una **profundidad de color de 1 bit**.

> [!NOTE]  
> - **Analógico:** señal continua que representa magnitudes físicas variables, como las ondas sonoras, que varían suavemente dentro de un rango. En cambio, digital representa los datos mediante valores binarios discretos (0 y 1), lo que permite un procesamiento más preciso y resistente a errores.
> - **Bitmap:** tipo de imagen digital compuesta por una rejilla de píxeles, donde cada píxel contiene un valor de color específico, representando la imagen en formato rasterizado.
> - **Píxel:** abreviatura de picture element (“elemento de imagen”); es la unidad más pequeña de una imagen o pantalla digital, que representa un punto individual con un color e intensidad determinados.

Para calcular el tamaño de la imagen, la fórmula es: 

tamaño de la imagen = ancho (píxeles) × alto (píxeles) × profundidad de color (bits por píxel)

```13 × 10 × 1 = 130 bits```

```130 / 8 = 16.25 bytes```

Sin embargo, en realidad este cálculo no es completamente preciso, ya que la imagen necesitaría más datos para almacenar metadatos y otra información de cabecera (header).

Estos datos adicionales pueden incluir información como:

- las dimensiones de la imagen,
- la profundidad de color,
- y otros atributos que permiten a la CPU leer correctamente los datos de la imagen de modo que pueda mostrarla adecuadamente en la pantalla.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2023.%20Imagen%20con%20resoluci%C3%B3n%2013x10.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 23: Imagen con resolución 13x10. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Para mejorar la calidad de una imagen bitmap, tenemos dos opciones:

1. **Aumentar el número de píxeles** → es decir, incrementar la resolución de la imagen.
2. **Aumentar la profundidad de color** → usar más bits por píxel para representar una gama de colores más amplia y precisa.

#### Resolución – aumentar el número de píxeles

Aumentar el número de píxeles en una imagen bitmap incrementa su calidad.
Una mayor resolución permite más detalle y nitidez, mientras que las imágenes con resoluciones bajas pueden mostrar pérdida de detalle y una apariencia pixelada.

Sin embargo, la cantidad de píxeles no es el único factor importante: también influye el tamaño de la pantalla donde se muestra la imagen.
Las imágenes con un mayor PPI (píxeles por pulgada, pixels per inch) se ven más nítidas que aquellas con un PPI menor.

Por ejemplo, imagina una imagen con una resolución de 1024×768 píxeles mostrada en tu teléfono frente a la misma imagen proyectada en una pantalla de cine.
El teléfono, al tener una mayor densidad de píxeles (PPI), mostrará la imagen más clara y detallada.

El inconveniente de una imagen con mayor resolución es que ocupa más espacio de almacenamiento, lo cual puede afectar la eficiencia de almacenamiento y transferencia.

> [!NOTE]  
> - **Resolución de imagen:** número de píxeles contenidos en una imagen digital, normalmente expresado como sus dimensiones (ancho × alto) en píxeles, y a veces también como densidad de píxeles (PPI / DPI) para referirse a la calidad de impresión.
> - **Profundidad de color:** también llamada “profundidad de bits” (bit depth); indica el número de bits usados para representar el color de cada píxel en una imagen digital, determinando así el rango y la precisión de los colores que se pueden mostrar.
> - **Metadatos:** información que describe otros datos, proporcionando contexto y detalles sobre su contenido, estructura y atributos. En el caso de las imágenes digitales, los metadatos incluyen datos como las dimensiones, la profundidad de color, la fecha de creación, el autor, la configuración de la cámara y otras propiedades que ayudan a gestionar, comprender y utilizar la imagen de forma eficaz.

Resoluciones comunes:

| **Nombre de la resolución** | **Dimensiones en píxeles** | **Uso común** |
|------------------------------|-----------------------------|----------------|
| VGA                 | 640 × 480            | Primeras pantallas de ordenador, gráficos web básicos |
| SVGA                | 800 × 600            | Monitores estándar de ordenador, gráficos web |
| HD (720p)           | 1280 × 720           | Vídeo en HD, televisión HD básica |
| Full HD (1080p)     | 1920 × 1080          | Vídeo en Full HD, monitores y televisores modernos |
| 2K                  | 2048 × 1080          | Cine digital, algunos monitores |
| Quad HD (1440p)     | 2560 × 1440          | Monitores de alta resolución, videojuegos, uso profesional |
| 4K (Ultra HD)       | 3840 × 2160          | Televisores Ultra HD, monitores de gama alta, vídeo |
| 8K                  | 7680 × 4320          | Televisores de última generación, vídeo profesional |

#### Profundidad de color – aumentar la cantidad de colores

Cuando aumentamos la profundidad de color, se permite representar una gama más amplia de colores, lo que da como resultado imágenes más vivas y precisas.

Si una imagen tiene una profundidad de color baja, esto puede causar el fenómeno conocido como “banding”, donde los degradados se ven como escalones visibles en lugar de transiciones suaves entre colores.

Sin embargo, al igual que ocurre con la resolución de imagen, también debemos tener en cuenta el impacto en el tamaño del archivo y los tiempos de transferencia.

Cuanto mayor sea la profundidad de color, mayor será el tamaño del archivo.

| **Profundidad de color (bits por píxel)** | **Número de colores** | **Uso común** |
|-------------------------------------------|------------------------|----------------|
| 1 bit  | 2 | Gráficos simples, pantallas monocromas |
| 4 bits | 16 | Primeros gráficos por ordenador, iconos |
| 8 bits | 256 | Imágenes GIF, gráficos web sencillos |
| 16 bits | 65.536 | Imágenes de alta coloración, algunos formatos de vídeo |
| 24 bits (color real) | 16,8 millones | Estándar para la mayoría de las imágenes y vídeos, fotografía digital |
| 30 bits (color profundo) | Más de 1.000 millones | Fotografía profesional, monitores y televisores de alta gama |
| 36 bits | Más de 68.000 millones | Imagen médica, gráficos profesionales |
| 48 bits | Billones | Aplicaciones personales de alta gama, imágenes científicas detalladas |

La mayoría de las **pantallas modernas** son de **24 bits**, lo que permite representar 16,8 millones de colores.
Cada píxel está compuesto por **tres luces**: una **roja (R)**, una **verde (G)** y una **azul (B)**, conocidas en conjunto como el modelo de color “RGB”.

Cada canal de color tiene un rango de valores de 0 a 255 (es decir, 1 byte por canal de color).
Esto es suficiente para la mayoría de las aplicaciones, ya que el ojo humano puede distinguir alrededor de 10 millones de colores distintos.

Los monitores que superan los 24 bits suelen ser necesarios solo en ámbitos profesionales, donde la precisión del color es esencial.

A continuación se muestra una imagen de alta resolución. Si hacemos zoom sobre el vestido de esa imagen, podemos observar la composición de los píxeles individuales y los valores de cada canal de color.

Al trabajar con gráficos, estos valores suelen expresarse en hexadecimal.
Por ejemplo, si tomamos el píxel superior izquierdo del vestido, sus valores son:

R: 216, G: 190, B: 199 → #d8bec7

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2024.%20Imagen%20de%20alta%20resoluci%C3%B3n.png" alt="Imagen" width="580" height="auto"/>
    <p><em>Figura 24: Imagen de alta resolución. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Una imagen de alta resolución con una resolución de 2268 × 4032 píxeles, una profundidad de color de 24 bits y un tamaño de archivo de 1,77 MB.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2025.%20Zoom%20en%20una%20%C3%A1rea%20de%20la%20imagen%20de%20alta%20resoluci%C3%B3n.png" alt="Imagen" width="650" height="auto"/>
    <p><em>Figura 25: Zoom en una área de la imagen de alta resolución. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Un área ampliada de la imagen anterior, que muestra el valor de cada píxel, creada utilizando la herramienta disponible en: [www.csfieldguide.org.nz/en/interactives/pixel-viewer](https://www.csfieldguide.org.nz/en/interactives/pixel-viewer).

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2026.%20El%20valor%20de%20un%20p%C3%ADxel%20del%20vestido.png" alt="Imagen" width="650" height="auto"/>
    <p><em>Figura 26: El valor de un píxel del vestido. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Los valores de color del píxel superior izquierdo del vestido en la fotografía —obtenidos utilizando [www.w3schools.com/colors/colors_rgb.asp](https://www.w3schools.com/colors/colors_rgb.asp).

También podemos observar el impacto de las menores profundidades de color sobre la misma imagen:

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2027.%20Misma%20imagen%20usando%20diferentes%20profundidades.png" alt="Imagen" width="650" height="auto"/>
    <p><em>Figura 27: Misma imagen usando diferentes profundidades. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

La misma imagen utilizando diferentes profundidades de color, desde 24 bits hasta 0 bits, creada utilizando: [https://www.csfieldguide.org.nz/en/interactives/image-bit-comparer/](https://www.csfieldguide.org.nz/en/interactives/image-bit-comparer/).

### Audio

El audio en su forma analógica es una señal continua que representa las ondas sonoras mediante variaciones de la presión del aire. Estas ondas sonoras pueden capturarse mediante dispositivos de entrada, como los micrófonos, que convierten las ondas en una señal digital, la cual se almacena en forma binaria.

Este proceso implica varios pasos:

Conversión analógico-digital (ADC)

El sonido es una señal analógica continua. Un **ADC** (Conversor Analógico-Digital) toma muestras de la **amplitud** (volumen o intensidad) del sonido a intervalos discretos en un proceso conocido como muestreo.

La velocidad a la que esto ocurre se mide en **Hertz (Hz)**: cuanto mayor es el número de Hertz, más muestras se registran por segundo.

El audio con calidad de CD utiliza **44,1 kHz**, mientras que el audio profesional se muestrea a 48 kHz.

Cada muestra se almacena y representa como un valor numérico en binario. La **precisión** está determinada por la **profundidad de bits (bit depth)**. Cuanto mayor sea la profundidad de bits, más valores posibles se podrán usar para describir la muestra.

Por ejemplo:

- La profundidad de bits del sonido con calidad de CD es de 16 bits, lo que en base dos, da 65.536 valores posibles.
- El audio profesional, que usa 24 bits, tiene 16.777.216 valores posibles.

Un solo segundo de audio estéreo (dos canales) con una frecuencia de muestreo de 44,1 kHz y una profundidad de 16 bits tiene:

- 44.100 muestras por segundo.
- Cada muestra representada por 16 bits.
- Una necesidad total de almacenamiento por segundo de:

44.100 muestras/segundo × 16 bits/muestra × 2 canales = 1.411.200 bits por segundo o 176.400 bytes por segundo.

> [!NOTE]  
> - **Amplitud:** la magnitud del cambio en una onda sonora, que representa la intensidad o volumen del sonido.
> - **Muestreo:** el proceso de convertir una señal analógica continua en una serie de valores digitales discretos midiendo su amplitud a intervalos regulares.
> - **kHz (kilohertz):** unidad de frecuencia equivalente a 1000 ciclos por segundo, comúnmente utilizada para medir la frecuencia de muestreo de señales de audio.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2028.%20Se%C3%B1al%20anal%C3%B3gica%20y%20digital.png" alt="Imagen" width="650" height="auto"/>
    <p><em>Figura 28: Señal analógica y digital. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

La forma de onda continua azul representa una **señal analógica**, que es una representación **suave y continua del sonido**.

La **señal digital** consiste en **muestras discretas** tomadas a intervalos regulares (frecuencia de muestreo), lo que ilustra cómo la señal analógica continua se convierte en una **serie de puntos discretos** en formato digital.

#### Formatos de almacenamiento

Existen muchos tipos diferentes de **formatos de archivo** para almacenar audio. Los más comunes son **WAV, AIFF, MP3 y FLAC**.

La principal diferencia entre ellos es si están **comprimidos** o **no comprimidos**.

- Los **formatos no comprimidos** almacenan los datos binarios en bruto.
- Los **formatos comprimidos** utilizan algoritmos para reducir el tamaño del archivo con el fin de facilitar su **almacenamiento o transmisión**.

Al igual que en la compresión de imágenes, la **compresión de audio** intenta reducir el tamaño del archivo **eliminando partes de la señal sonora menos perceptibles para el oído humano**.

Existen dos tipos de compresión de audio: **con pérdida (lossy)** y **sin pérdida (lossless)**.

- Los **algoritmos sin pérdida (lossless)** comprimen los datos **sin pérdida de calidad**.
- Los **algoritmos con pérdida (lossy)** eliminan de forma permanente partes del audio que el oído humano **percibe con menor facilidad** en la grabación.

Principales formatos de audio

- **WAV (Waveform Audio File Format):** sin comprimir.
- **AIFF (Audio Interchange File Format):** sin comprimir.
- **MP3 (MPEG Audio Layer III):** comprimido (con pérdida).
- **FLAC (Free Lossless Audio Codec):** comprimido (sin pérdida).

> [!NOTE]  
> **Estéreo:** método de reproducción de sonido que utiliza dos o más canales de audio para crear la percepción de que el sonido proviene de diferentes direcciones, lo que mejora la sensación de profundidad y dimensión espacial.

#### 🧠💻 Programming exercise

Explora los archivos de audio con el siguiente código. Esto te permitirá analizar la amplitud de cualquier archivo MP3.

```python
import soundfile as sf
import numpy as np
import matplotlib.pyplot as plt
from scipy.fftpack import fft

# Load the audio file
samples, sample_rate = sf.read("name_of_file.mp3")

# If stereo, select one channel
if samples.ndim > 1:
    samples = samples[:, 0]

# Visualize the waveform
plt.figure(figsize=(12, 6))
plt.plot(samples)
plt.title("Audio Waveform")
plt.xlabel("Sample Index")
plt.ylabel("Amplitude")
plt.show()

# Perform FFT
spectrum = fft(samples)
frequencies = np.fft.fftfreq(len(spectrum), 1 / sample_rate)

plt.figure(figsize=(12, 6))
plt.plot(frequencies[:len(frequencies)//2], np.abs(spectrum[:len(spectrum)//2]))
plt.title("Audio Spectrum")
plt.xlabel("Frequency (Hz)")
plt.ylabel("Magnitude")
plt.show()
```

Para ejecutar en Google Colab y poder seleccionar la canción. Debemos ejecutar esta celda:

```python
from google.colab import files
uploaded = files.upload()
```

### Vídeo

Los vídeos están compuestos por varios elementos que se encuentran dentro de un **formato contenedor encapsulado**, como **MP4, MKV o AVI**.

Los componentes son:

- **Fotogramas (datos visuales)**
- **Pistas de audio**
- **Metadatos**
- **Subtítulos y subtítulos ocultos (closed captions)**

El audio se almacena como se describió en la sección anterior sobre audio, y los metadatos y subtítulos se guardan como texto, por lo que esta sección se centrará únicamente en cómo se almacena el **vídeo**.

El vídeo, en esencia, se almacena como una **secuencia de imágenes fijas**, también conocidas como **fotogramas**.

Cuando se reproducen en rápida sucesión (normalmente entre **24 y 60 fotogramas por segundo**), estos fotogramas crean la **ilusión de movimiento**.

Esto es muy parecido a la técnica que quizá hayas utilizado para crear un **libro animado o flipbook**.

Los fotogramas se almacenan y codifican en **formato binario**, utilizando diversas técnicas para **optimizar el espacio** y garantizar una **reproducción eficiente**.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2029.%20Flipbook.png" alt="Imagen" width="550" height="auto"/>
    <p><em>Figura 29: Flipbook. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

La reproducción de vídeo digital es similar a un **flipbook**: una serie de imágenes que se muestran rápidamente, creando la **ilusión de movimiento**.

#### Fotogramas

En su forma bruta, los **fotogramas** se almacenan igual que las imágenes, donde cada **píxel** tiene un valor que puede representarse mediante un **modelo de color** como **RGB**.

Para mejorar la eficiencia del color, los fotogramas suelen convertirse del modelo RGB a otro diferente, como **YUV**.

Este modelo favorece la **luminancia** (brillo), a la que el ojo humano es más sensible que a los cambios en el detalle del color, lo que facilita la **compresión**.

Sin embargo, no podemos almacenar los fotogramas del mismo modo que almacenamos fotografías, ya que en ese formato serían **demasiado grandes**.

Por ello, los vídeos necesitan **ser comprimidos**, y existen dos técnicas principales para hacerlo:

- Compresión espacial (intraframe)
- Compresión temporal (interframe)

#### Técnicas de compresión

- **Compresión espacial (intraframe):** Es especialmente efectiva y común en vídeos con **gran variación de detalles dentro de cada fotograma**. Reduce el tamaño del archivo **eliminando información redundante dentro del propio fotograma**, como niveles de color o detalle que no aportan diferencias visibles. Este enfoque es importante para vídeos con mucho detalle que cambia significativamente entre fotogramas, como **animaciones, documentales de naturaleza** o **transmisiones en directo**.
- **Compresión temporal (interframe):** Es especialmente efectiva y común en vídeos con **movimiento coherente o continuo entre fotogramas**. Reduce el tamaño del archivo **eliminando información redundante entre fotogramas consecutivos**, capturando solo los **cambios o movimientos** de un fotograma al siguiente. Como técnica de **compresión predictiva**, predice el contenido de los fotogramas en función de los anteriores (y a veces de los siguientes), almacenando únicamente las diferencias.

Este método también es esencial en vídeos donde el contenido visual varía a lo largo del tiempo, como animaciones, documentales de naturaleza o emisiones de noticias en directo.

### Diferentes metodologias de código binario para el almacenamiento de enteros

#### Binario sin signo

Este es el sistema que se explicó en la Sección A1.2.1.

Este sistema solo representa números enteros positivos, utilizando directamente dígitos binarios (0 y 1).

#### Binario con signo

Incluye métodos para representar tanto números positivos como negativos.

#### Complemento a dos (Two’s complement)

El complemento a dos es un método para representar enteros con signo en binario, donde el bit más significativo (MSB) indica el signo:

- 0 → número positivo
- 1 → número negativo

Para convertir un número binario positivo en su equivalente negativo en complemento a dos:

1. Invierte todos los bits (cambia los 0 por 1 y los 1 por 0).
2. Suma 1 al bit menos significativo (LSB).


Ejemplo:
```
00000101 = +5  
Invertir bits → 11111010  
Sumar 1 → 11111011 = –5
```

**Limitación:**

En un sistema de 8 bits, el complemento a dos reduce el rango de números representables:

- En binario sin signo → de 0 a 255
- En complemento a dos → de –128 a +127

Esto reduce a la mitad la cantidad de valores positivos que se pueden representar.

#### Complemento a uno (One’s complement)

El complemento a uno es otro método para representar enteros con signo, donde el MSB indica el signo:

- 0 → positivo
- 1 → negativo

Para obtener el complemento a uno de un número positivo, simplemente se invierten todos los bits.

Ejemplo:
```
00000101 = +5  
11111010 = –5
```

**Limitaciones:**

Tiene dos representaciones para el número cero:

- Cero positivo → 00000000
- Cero negativo → 11111111

Esto genera confusión en operaciones aritméticas y lógicas, por lo que el complemento a dos es el sistema preferido.

Su rango es de –127 a +127.

#### Signo y magnitud (Sign-magnitude)

El método de signo y magnitud representa enteros con signo donde el bit más significativo (MSB) indica el signo:


- 0 → positivo
- 1 → negativo


Los bits restantes representan la magnitud del número, de forma similar al binario sin signo.

Ejemplo:
00000101 = +5  
10000105 = –5

**Limitaciones:**

Tiene dos representaciones para el cero:

- Cero positivo → 00000000
- Cero negativo → 10000000

Su rango también va de –127 a +127.

Es un sistema simple, pero menos eficiente que el complemento a dos.

#### Decimal codificado en binario (BCD)

El Decimal Codificado en Binario (BCD) es un método para representar números decimales en el que cada dígito del número decimal se codifica por separado en su propia forma binaria.

A diferencia de la representación binaria pura, que convierte el número decimal completo en una única secuencia binaria, el BCD asigna un código binario de 4 bits a cada dígito decimal (0–9).

Ejemplo:

```
0100 0101 = 45
```
ya que 0100 representa el 4 y 0101 representa el 5.

Este sistema es útil cuando se necesita una representación decimal exacta, como en aplicaciones financieras o en relojes digitales, ya que evita los errores de redondeo que pueden ocurrir en otros sistemas.

Sin embargo, como se utilizan cuatro bits por cada dígito, se requieren más bits para almacenar los números, lo que lo hace menos eficiente en espacio que las representaciones binarias puras.

Además, las operaciones aritméticas en BCD son más complejas, ya que requieren pasos adicionales para manejar acarreo (carry) y desbordamiento (overflow), por lo que no es adecuado para la computación de propósito general.

Código Gray (código binario reflejado)

El Código Gray es un sistema binario en el que dos valores sucesivos solo pueden diferir en un bit. Esto lo hace especialmente útil en situaciones donde la integridad de los datos durante las transiciones es importante.

Un ejemplo típico es el de un brazo robótico en el que se desea monitorizar su posición. A medida que el brazo gira, el codificador rotativo genera una secuencia de salidas binarias correspondientes al ángulo del brazo.

Si el codificador utilizara código binario estándar, pequeñas vibraciones mecánicas o inexactitudes podrían causar que varios bits cambien simultáneamente, provocando lecturas incorrectas. Sin embargo, al usar Código Gray, se minimiza el riesgo de errores de transición.

Comparación entre el Código Gray y el binario estándar para los números del 0 al 7:

| Números | Binario estándar | Código Gray |
|----------|------------------|--------------|
| 0        | 000              | 000          |
| 1        | 001              | 001          |
| 2        | 010              | 011          |
| 3        | 011              | 010          |
| 4        | 100              | 110          |
| 5        | 101              | 111          |
| 6        | 110              | 101          |
| 7        | 111              | 100          |

#### Exceso-N (Excess-N)

El sistema Exceso-N consiste en sumar un sesgo fijo (N) al valor real para formar un valor codificado, y restar ese sesgo para decodificarlo.
Este método se utiliza para que todos los números enteros con signo aparezcan como números binarios no negativos, facilitando así las comparaciones y las operaciones aritméticas.

Ejemplo con Exceso-3:

El número decimal 2 se codifica como:

2+3=5 → 0101

El número decimal –2 se codifica como:

−2+3=1 → 0001

En un sistema de 8 bits, se suele utilizar Exceso-127, que suma 127 para codificar un número y resta 127 para decodificarlo.

Si intentamos ordenar números binarios con signo, puede resultar complicado, ya que los números negativos aparecen como valores binarios mayores que los positivos.

Ejemplo con signo y magnitud:

01111111 = +127  
10000001 = –127

Codificados con Exceso-127:

127 + 127 = 254 → 11111110  
–127 + 127 = 0 → 00000000

Ahora los números positivos aparecen como mayores que los negativos, lo que facilita el orden.

Decodificación (Exceso-127):

254 – 127 = +127 → 11111110  
0 – 127 = –127 → 00000000

#### Representación en punto fijo (Fixed-point representation)

La **representación en punto fijo** es un método para almacenar **números reales (con parte fraccionaria)** en binario **fijando la posición del punto binario**.

En este sistema, el punto binario se coloca en una posición predefinida, lo que permite una representación sencilla de fracciones, aunque con limitaciones en **precisión** y **rango**.

Ejemplo:

Queremos representar 5.25 en un sistema de 8 bits, donde:

4 bits son para la parte entera

4 bits para la parte fraccionaria

```
Parte entera: 0101 = 5  
Parte fraccionaria: 0100 = 0.25  
Combinado: 0101.0100
```

En la parte fraccionaria binaria:

- El primer bit a la derecha del punto vale ½
- El segundo vale ¼
- El tercero vale ⅛
- El cuarto vale 1/16

Por tanto, en el ejemplo anterior tenemos 0.0100=0.25.

El número de bits asignados limita el rango y la precisión.

Por ejemplo, con 4 bits para la parte entera con signo, el rango es de –8 a +7.9375, con una resolución mínima de 0.0625.

Esto significa que este sistema no maneja bien números muy grandes o muy pequeños, aunque es más simple y rápido que la representación en punto flotante, ya que no necesita ajustar la posición del punto binario.

#### Representación en punto flotante (Floating-point representation)

La **representación en punto flotante** permite representar **números reales con un rango muy amplio**, incluidos números muy grandes, muy pequeños o con parte fraccionaria.
Se compone de tres partes:

1. **Bit de signo** (1 bit) → Indica si el número es positivo o negativo.
2. **Exponente** (8 bits) → Escala el número mediante una potencia de dos y se almacena usando el sistema **Exceso-127**.
3. **Mantisa o significando** (23 bits) → Representa los dígitos significativos del número (sin incluir el 1 inicial en forma normalizada).

Se utiliza el estándar **IEEE 754** para números de **precisión simple (32 bits)**.

<br>

## A1.2.3. Describe el propósito y el uso de las puertas lógicas

### La historia de las puertas lógicas
A mediados del siglo XIX, un matemático británico llamado George Boole desarrolló un sistema algebraico conocido como “álgebra booleana”. Este proporcionó un marco matemático para representar enunciados y operaciones lógicas que sentaron las bases de la lógica digital moderna.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2030.%20George%20Boole.jpg" alt="Imagen" width="550" height="auto"/>
    <p><em>Figura 30: George Boole. Fuente: Wikipedia</em></p>
  </div>
  
George Boole, el matemático británico que desarrolló el álgebra booleana, sentando las bases de la lógica digital y la informática moderna.

A principios del siglo XX, un matemático e ingeniero eléctrico estadounidense llamado Claude Shannon fue la primera persona en reconocer el potencial del álgebra booleana para el diseño de circuitos eléctricos. Demostró cómo el diseño de circuitos de relés eléctricos podía optimizarse utilizando álgebra booleana, y posteriormente el desarrollo de la tecnología de semiconductores impulsó aún más la evolución de las puertas lógicas.

El transistor fue inventado en 1947 en los Laboratorios Bell, lo que hizo posible construir puertas lógicas compactas y eficientes. Entre las décadas de 1960 y 1970, los circuitos integrados comenzaron a incorporar múltiples transistores en un solo chip, lo que llevó al desarrollo de los microprocesadores. Las puertas lógicas son los bloques fundamentales de los sistemas digitales modernos, desde la calculadora básica hasta los superordenadores avanzados.

### Puertas básicas

Las puertas lógicas son **componentes fundamentales en la electrónica digital**, esenciales para construir diversos tipos de circuitos dentro de los ordenadores y otros dispositivos digitales.
Los tipos básicos de puertas lógicas incluyen las puertas **AND**, **OR** y **NOT**, cada una de las cuales realiza una función lógica específica. Estas puertas reciben una o más entradas binarias y producen una salida binaria según la operación lógica que llevan a cabo.

Para comprender y verificar el comportamiento de estas puertas, utilizamos tablas de verdad, que enumeran de manera sistemática todas las combinaciones posibles de entradas y sus salidas correspondientes, proporcionando una representación clara de la función de la puerta. Además, cada puerta tiene una representación en álgebra booleana que permite simplificar expresiones lógicas complejas.

Las puertas lógicas están formadas por transistores, que actúan como interruptores electrónicos, permitiendo o bloqueando el flujo de corriente eléctrica. En un transistor, el cable de control (o “gate”) regula la corriente entre los dos electrodos, conocidos como “source” (fuente) y “drain” (drenador). Cuando se aplica un voltaje a la puerta, se permite que la corriente fluya desde la fuente hacia el drenador, lo que permite que el transistor cambie de estado y realice operaciones lógicas.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2031.%20Circuito%20l%C3%B3gico.png" alt="Imagen" width="550" height="auto"/>
    <p><em>Figura 31: Puerta Buffer apagada. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

  Una puerta Buffer que muestra el funcionamiento interno de la puerta: cuando el cable de control está apagado, no puede fluir electricidad entre los electrodos.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2032.%20Circuito%20l%C3%B3gico.png" alt="Imagen" width="550" height="auto"/>
    <p><em>Figura 32: Puerta Buffer encendida. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Cuando la electricidad circula por el cable de control, el transistor permite el flujo de electricidad entre los electrodos.

Arriba se muestra una puerta Buffer simple, donde podemos considerar el cable de control como la entrada y el electrodo drain como la salida. Si la entrada está encendida, la salida está encendida; y si la entrada está apagada, la salida está apagada. Podemos mostrar esto usando una tabla de verdad:

| Input A | Output X |
|---------|----------|
|    1    |     1    |
|    0    |     0    |

#### Puerta AND

El diagrama de debajo muestra una puerta AND implementada con transistores. La puerta tiene dos entradas y una salida. Si solo una de las entradas está encendida, uno de los transistores sin entrada detendría el paso de la corriente. Solo cuando ambas entradas están en alto (1) los transistores permiten que la corriente fluya, lo que da como resultado una salida alta (1).

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2033.%20Puerta%20AND.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 33: Puerta AND. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

**Regla de entrada y salida:** La puerta AND produce 1 solo si ambas entradas son 1.

| Input A | Input B | Output X |
|---------|----------|-----------|
|    0    |    0     |     0     |
|    0    |    1     |     0     |
|    1    |    0     |     0     |
|    1    |    1     |     1     |

```Boolean algebra: X = A · B```

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2034.%20Esquema%20a%20nivel%20de%20transistores%20de%20una%20puerta%20AND.png" alt="Imagen" width="550" height="auto"/>
    <p><em>Figura 34: Esquema a nivel de transistores de una puerta AND. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

#### Puerta OR

El diagrama de la izquierda muestra una puerta OR implementada con transistores. La puerta tiene dos entradas —A y B— y una salida. Cuando cualquiera de las entradas A o B está en alto (1), el transistor correspondiente se activa, permitiendo que la corriente fluya a través del circuito y dando como resultado una salida alta (1). Cuando ambas entradas están en bajo (0), ninguno de los transistores conduce y la salida permanece en bajo (0).

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2035.%20Puerta%20OR.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 35: Puerta OR. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

```Boolean algebra: X = A + B```

**Regla de entrada y salida:** La puerta OR produce 1 si al menos una de las entradas es 1.

| Input A | Input B | Output X |
|---------|----------|-----------|
|    0    |    0     |     0     |
|    0    |    1     |     1     |
|    1    |    0     |     1     |
|    1    |    1     |     1     |

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2036.%20Esquema%20a%20nivel%20de%20transistores%20de%20una%20puerta%20OR.png" alt="Imagen" width="550" height="auto"/>
    <p><em>Figura 36: Esquema a nivel de transistores de una puerta OR. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

#### Puerta NOT

El diagrama siguiente ilustra una puerta NOT (inversor) utilizando un transistor. En esta configuración, la línea de entrada está conectada a la puerta (gate) del transistor, la línea de salida está conectada a la fuente (source) y el drenador (drain) está conectado a tierra.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2037.%20Puerta%20NOT.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 37: Puerta NOT. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2038.%20Esquema%20a%20nivel%20de%20transistores%20de%20una%20puerta%20NOT.png" alt="Imagen" width="550" height="auto"/>
    <p><em>Figura 38: Esquema a nivel de transistores de una puerta NOT. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Cuando la entrada está en alto (1), el transistor se enciende, permitiendo que la corriente fluya desde la fuente hacia el drenador, conectando efectivamente la salida a tierra y produciendo un voltaje bajo en la salida (0). Cuando la entrada está en bajo (0), el transistor se apaga, impidiendo que la corriente fluya hacia tierra. En este estado, la salida adopta un voltaje alto (1).

**Regla de entrada y salida:** La puerta NOT produce el valor opuesto al de la entrada. 

| Input A | Output X |
|---------|-----------|
|    0    |     1     |
|    1    |     0     |

```Boolean algebra: X = ¬A```

### Puertas derivadas (complejas)

Las siguientes puertas —**NAND**, **NOR**, **XOR** y **XNOR**— son ejemplos de puertas derivadas. Las puertas derivadas son combinaciones de las puertas básicas y proporcionan funciones lógicas más complejas. Para mostrarlas, subiremos un nivel de abstracción y, en lugar de examinar el esquema a nivel de transistores, veremos cómo se combinan las puertas básicas para crearlas.

#### Puerta NAND (NOT AND)

Una puerta NAND se construye con una puerta AND seguida de una puerta NOT. Debido a esto, produce la salida opuesta a una puerta AND. Si ambas entradas están en alto (1), la salida es baja (0). En todos los demás casos, la salida es alta (1).

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2039.%20Puerta%20NAND.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 39: Puerta AND y NOT. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Cómo se construye una puerta NAND: una puerta AND seguida de una puerta NOT.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2040.%20Puerta%20NAND.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 40: Puerta NAND. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

**Regla de entrada y salida:** La puerta NAND produce 1 a menos que ambas entradas sean 1.

| Input A | Input B | Output X |
|---------|----------|-----------|
|    0    |    0     |     1     |
|    0    |    1     |     1     |
|    1    |    0     |     1     |
|    1    |    1     |     0     |

```Boolean algebra: X = ¬(A · B)```

#### Puerta NOR (NOT OR)

Una puerta NOR produce la salida opuesta a una puerta OR, ya que está construida utilizando una puerta OR seguida de una puerta NOT. Esto significa que solo cuando ambas entradas están en bajo (0) la salida es alta (1). En todos los demás casos, la salida es baja (0).

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2041.%20Puerta%20NOR.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 41: Puerta OR y NOT. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Cómo se construye una puerta NOR: una puerta OR seguida de una puerta NOT.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2042.%20Puerta%20NOR.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 42: Puerta NOR. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

**Regla de entrada y salida:** La puerta NOR produce 1 solo si ambas entradas son 0.

| Input A | Input B | Output X |
|---------|----------|-----------|
|    0    |    0     |     1     |
|    0    |    1     |     0     |
|    1    |    0     |     0     |
|    1    |    1     |     0     |

```Boolean algebra: X = ¬(A + B)```

#### Puerta XOR (OR exclusivo)

La puerta XOR (OR exclusivo) se diferencia de la puerta OR en un aspecto clave: su salida es verdadera solo cuando las entradas son diferentes. Esto significa que la puerta XOR produce verdadero cuando exactamente una de las entradas es verdadera, pero falso cuando ambas entradas son iguales. Por ejemplo, si ambas entradas están en alto (1), la salida de la puerta XOR es baja (0). Esto es distinto a la puerta OR, que en ese caso produciría una salida alta (1).

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2043.%20Puerta%20XOR.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 43: Puerta exclusive OR. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Cómo se construye una puerta XOR.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2044.%20Puerta%20XOR.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 44: Puerta XOR. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

**Regla de entrada y salida:** La puerta XOR produce 1 si las entradas son diferentes.

| Input A | Input B | Output X |
|---------|----------|-----------|
|    0    |    0     |     0     |
|    0    |    1     |     1     |
|    1    |    0     |     1     |
|    1    |    1     |     0     |

```Boolean algebra: X = A ⊕ B```

#### Puerta XNOR (exclusive NOT OR)

La puerta XNOR se construye utilizando una puerta XOR seguida de una puerta NOT. Esto significa que su salida es la opuesta a la de una puerta XOR, produciendo un valor alto (1) únicamente cuando ambas entradas son iguales (ya sea ambas altas o ambas bajas).

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2045.%20Puerta%20XNOR.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 45: Puerta XNOR. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Cómo se construye una puerta XNOR: una puerta XOR seguida de una puerta NOT.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2046.%20Puerta%20XNOR.png" alt="Imagen" width="250" height="auto"/>
    <p><em>Figura 46: Puerta XNOR. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

**Regla de entrada y salida:** La puerta XNOR produce 1 si las entradas son iguales.

| Input A | Input B | Output X |
|---------|----------|-----------|
|    0    |    0     |     1     |
|    0    |    1     |     0     |
|    1    |    0     |     0     |
|    1    |    1     |     1     |

```Boolean algebra: X = ¬(A ⊕ B)```

<br>

## A1.2.4. Construye y analiza tablas de la verdad

### Tablas de verdad para predecir la salida de circuitos lógicos simples

El siguiente diagrama muestra un circuito lógico, donde varios compuertas lógicas están conectadas entre sí. En este escenario, debes ser capaz de trabajar con circuitos que tengan hasta tres entradas.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2047.%20Diagrama%20de%20circuito%20l%C3%B3gico%201%20.png" alt="Imagen" width="550" height="auto"/>
    <p><em>Figura 47: Diagrama de circuito lógico 1. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Al crear una tabla de verdad, primero introduce las tres entradas y sus posibles estados; en este caso, A, B y C. Como hay tres entradas, puedes calcular el número de filas necesarias usando 2<sup>n</sup>, donde *n* representa el número de entradas.

En este ejemplo:

2<sup>3</sup> = 8

- Rellena la columna de la derecha alternando entre 0 y 1.
- Rellena la columna central alternando, cada dos filas, entre 0 y 1.
- Rellena la columna de la izquierda alternando, cada cuatro filas, entre 0 y 1.

Seguir este patrón te dará todos los posibles estados de entrada.

| A | B | C |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 0 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |
| 1 | 1 | 1 |

Una vez hecho esto, añadimos los valores intermedios para facilitar recordar el estado en cada etapa del circuito. En este ejemplo, tenemos tres valores intermedios: P, Q y R. Finalmente, añadimos la columna de salida, X.

| A | B | C | P | Q | R | X |
|---|---|---|---|---|---|---|
| 0 | 0 | 0 |   |   |   |   |
| 0 | 0 | 1 |   |   |   |   |
| 0 | 1 | 0 |   |   |   |   |
| 0 | 1 | 1 |   |   |   |   |
| 1 | 0 | 0 |   |   |   |   |
| 1 | 0 | 1 |   |   |   |   |
| 1 | 1 | 0 |   |   |   |   |
| 1 | 1 | 1 |   |   |   |   |

Ahora, comenzando por los valores intermedios, recorre el circuito lógico paso a paso.

| A | B | C | P (A AND B) | Q (B NOR C) | R (P OR Q) | X (C XOR R) |
|---|---|---|--------------|-------------|------------|-------------|
| 0 | 0 | 0 |      0       |      1      |     1      |      1      |
| 0 | 0 | 1 |      0       |      0      |     0      |      1      |
| 0 | 1 | 0 |      0       |      0      |     0      |      0      |
| 0 | 1 | 1 |      0       |      0      |     0      |      1      |
| 1 | 0 | 0 |      0       |      1      |     1      |      1      |
| 1 | 0 | 1 |      0       |      0      |     0      |      1      |
| 1 | 1 | 0 |      1       |      0      |     1      |      1      |
| 1 | 1 | 1 |      1       |      0      |     1      |      0      |

### Tablas de verdad para determinar las salidas a partir de las entradas de la descripción de un problema

**Descripción del problema:** *Una alarma para bebés que se activa cuando la alarma está encendida y el bebé está llorando o la habitación está demasiado fría.*

Con una descripción del problema, primero necesitamos identificar las entradas. Aquí tenemos tres: el interruptor de la alarma, el llanto del bebé y la temperatura de la habitación, que podemos representar como A, B y C y configurar nuestra tabla de verdad.

Sabemos que la alarma se activa si el dispositivo está encendido Y el bebé está llorando O la habitación está demasiado fría. A partir de aquí, podemos identificar las puertas lógicas en la descripción. Podemos deducir que el dispositivo debe estar encendido antes de que la alarma pueda activarse, por lo que, si el interruptor está apagado, todas las salidas serían 0. Si el dispositivo está encendido, al menos una de las otras dos entradas debe estar activa para que la alarma se dispare. Tenemos un valor intermedio (el bebé está llorando O la habitación está fría), representado con P.

| A (encendida) | B (llorando) | C (fría) | P (B or C) | X (A and P) |
|------------|------------|----------|------------|-------------|
| 0          | 0          | 0        | 0          | 0           |
| 0          | 0          | 1        | 1          | 0           |
| 0          | 1          | 0        | 1          | 0           |
| 0          | 1          | 1        | 1          | 0           |
| 1          | 0          | 0        | 0          | 0           |
| 1          | 0          | 1        | 1          | 1           |
| 1          | 1          | 0        | 1          | 1           |
| 1          | 1          | 1        | 1          | 1           |

### Expresiones lógicas

Podemos representar circuitos lógicos utilizando álgebra booleana. Si usamos de nuevo el escenario de la alarma para bebés, podemos representarlo así:

```X = A · (B + C)```

En álgebra booleana, los paréntesis se utilizan a menudo para indicar qué operaciones deben realizarse primero. Sin embargo, existe un orden estándar de las operaciones, similar a PEMDAS (o BODMAS) en matemáticas. Si no hay paréntesis presentes, se debe seguir esta secuencia:

- NOT
- AND (incluyendo NAND)
- OR (incluyendo NOR y XOR)

Esto garantiza que las operaciones se ejecuten en el orden correcto para obtener resultados precisos.

### Mapas de Karnaugh y simplificación algebraica

Los mapas de Karnaugh (K-maps) son una herramienta que ayuda a simplificar expresiones booleanas, facilitando la creación de circuitos digitales más simples y eficientes. En lugar de utilizar métodos algebraicos complicados, los mapas de Karnaugh permiten agrupar visualmente términos de una tabla de verdad, lo que hace más rápido encontrar una expresión simplificada.

Este proceso es útil porque reduce el número de puertas lógicas necesarias en un circuito, ahorrando tiempo, espacio, costes y consumo de energía.

#### Dos entradas

Este mapa de Karnaugh de dos entradas se utiliza para expresiones con dos variables. En este mapa, la variable A se coloca en el lateral y la variable B en la parte superior. Sin embargo, el orden de las variables no importa: B podría colocarse en el lateral y A en la parte superior. Ambos estados posibles (0 y 1) para cada variable se muestran en el mapa, representando todas las combinaciones de sus valores.

##### Expresión: A + B

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2048.%20K-map.png" alt="Imagen" width="450" height="auto"/>
  </div>

Dividimos la expresión en el operador OR (O) y nos centramos primero en el término que implica a A. Rellenamos el mapa de Karnaugh donde A es 1, lo que, en este caso, corresponde a toda la fila inferior. En esta etapa, ignoramos B y solo completamos las celdas en las que A = 1.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2049.%20K-map.png" alt="Imagen" width="450" height="auto"/>
  </div>

Hacemos lo mismo para la segunda parte de la expresión: B. 

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2050.%20K-map.png" alt="Imagen" width="450" height="auto"/>
  </div>

Este mapa de Karnaugh completado ahora muestra la expresión A + B.

Este es otro ejemplo de un mapa completado para la expresión ¬A + B:

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2051.%20K-map.png" alt="Imagen" width="450" height="auto"/>
  </div>

<br>

##### Expresión: A · B + A · ¬B

Esta es una expresión más complicada, pero que aún solo tiene dos entradas. Utilizando esta expresión, el circuito tendría el siguiente aspecto:

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2052.%20K-map.png" alt="Imagen" width="650" height="auto"/>
  </div>

La estructura del mapa en forma de tabla sigue siendo la misma:

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2053.%20K-map.png" alt="Imagen" width="450" height="auto"/>
  </div>

Volvemos a dividir la expresión en el símbolo OR (O), centrándonos inicialmente en A · B. En este caso, introducimos un 1 únicamente en una celda, donde tanto A como B son 1.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2054.%20K-map.png" alt="Imagen" width="450" height="auto"/>
  </div>

A continuación, nos centramos en la segunda parte de la expresión A · ¬B. En este caso, introducimos un 1 en la celda donde A es 1 y B es 0.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2055.%20K-map.png" alt="Imagen" width="450" height="auto"/>
  </div>

El mapa de Karnaugh ya está completo y muestra que el valor de B no tiene ningún impacto en el resultado, lo que nos permite simplificar la expresión a simplemente A. Si creamos el circuito utilizando esta expresión simplificada, podemos ver que el circuito es significativamente más eficiente, mientras que sigue realizando la misma función.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2056.%20K-map.png" alt="Imagen" width="450" height="auto"/>
  </div>

#### Tres entradas

##### Expresión: ¬A · B · C + A · ¬B · C + A · B · C
Con tres entradas, utilizamos un mapa de Karnaugh similar, pero en este caso colocamos dos de las entradas en la parte superior. Los dígitos de la parte superior pueden parecer fuera de orden en comparación con el conteo binario estándar (00, 01, 10, 11). En su lugar, siguen la convención del código Gray (véase la Sección A1.2.2 para más información), en la que solo cambia un dígito cada vez. Es importante configurar el mapa de esta manera para garantizar una agrupación y una simplificación correctas.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2057.%20K-map.png" alt="Imagen" width="650" height="auto"/>
  </div>

Ahora seguimos pasos similares a los del mapa de Karnaugh de dos entradas. Separamos la expresión por el operador OR (O) y nos centramos en el primer término: ¬A · B · C. En este paso, completamos el mapa de Karnaugh introduciendo un 1 en las celdas donde A es 0, B es 1 y C es 1.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2058.%20K-map.png" alt="Imagen" width="650" height="auto"/>
  </div>

Seguido de: A · ¬B · C

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2059.%20K-map.png" alt="Imagen" width="650" height="auto"/>
  </div>

Y finalmente: A · B · C

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2060.%20K-map.png" alt="Imagen" width="650" height="auto"/>
  </div>

#### Agrupación de los 1 y simplificación de la expresión

Aunque no se indicó explícitamente antes, es posible que hayas observado los recuadros dibujados alrededor de los grupos de 1 en los mapas de Karnaugh. Estos recuadros ayudan a simplificar la expresión booleana, pero hay algunas reglas importantes que deben seguirse al agrupar los 1:

- **Los grupos deben contener potencias de 2:** Se pueden agrupar uno, dos, cuatro, ocho o dieciséis 1.
- **Los grupos deben ser rectangulares o cuadrados:** Cada grupo debe formar un rectángulo o un cuadrado.
- **Los grupos no pueden ser diagonales:** Los 1 adyacentes solo se pueden agrupar horizontal o verticalmente, no en diagonal.
- **Los grupos deben ser lo más grandes posible:** Siempre se debe intentar formar los grupos más grandes para simplificar aún más la expresión.
- **Los grupos pueden solaparse:** Algunos 1 pueden incluirse en más de un grupo si esto ayuda a formar grupos más grandes.
- **Minimizar el número total de grupos:** El objetivo es utilizar el menor número de grupos posible para cubrir todos los 1.

Para determinar la expresión a partir de los grupos, analizamos cada grupo de celdas y nos fijamos en las variables. Si el valor de una variable se mantiene igual en todas las celdas del grupo, esa variable se conserva en la expresión simplificada. Sin embargo, si el valor de la variable cambia dentro del grupo, se elimina de la expresión.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2061.%20K-map.png" alt="Imagen" width="650" height="auto"/>
  </div>

El primer grupo está completamente a lo largo de la fila inferior, lo que significa que C se mantiene constante (C = 1), por lo que la conservamos en la expresión. A cambia de 0 a 1 entre las celdas del grupo, así que descartamos A. B permanece en 1 en ambas celdas, por lo que conservamos B.

Por tanto, la primera parte de nuestra expresión final es: B · C

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2062.%20K-map.png" alt="Imagen" width="650" height="auto"/>
  </div>

El segundo grupo, al igual que el primero, se encuentra a lo largo de la fila inferior, lo que significa que C se mantiene en 1, ya que no cambia dentro del grupo. En este caso, A permanece en 1 en ambas celdas, mientras que B cambia de 0 a 1. Dado que B cambia, descartamos B de esta parte de la expresión. Como resultado, conservamos A y C, lo que nos da la segunda parte de nuestra expresión: A · C

A continuación, combinamos estas expresiones mediante el operador OR (O), obteniendo la expresión final: B · C + A · C

> [!CAUTION]
> Al configurar tu mapa de Karnaugh para tres entradas, asegúrate de utilizar código Gray en los encabezados y no el binario estándar. El código Gray garantiza que solo cambie un bit entre celdas adyacentes, lo que ayuda a agrupar los 1 y a simplificar la expresión de forma más eficaz.

#### Conexión por los bordes en los mapas de Karnaugh

Aquí se muestra el mapa de Karnaugh para la expresión: ¬B + A · B · C

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2063.%20K-map.png" alt="Imagen" width="650" height="auto"/>
  </div>

Para agrupar estos 1, puedes asumir que esta es la respuesta:

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2064.%20K-map.png" alt="Imagen" width="650" height="auto"/>
  </div>

Sin embargo, los mapas de Karnaugh se consideran tridimensionales, y los grupos pueden formarse de izquierda a derecha y de arriba abajo (aunque con tres entradas solo es posible de izquierda a derecha). En este ejemplo, es posible construir un grupo más grande combinando los dos grupos de los extremos, formando un grupo cuadrado de cuatro 1.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2065.%20K-map.png" alt="Imagen" width="650" height="auto"/>
  </div>

<br>

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2066.%20K-map.png" alt="Imagen" width="550" height="auto"/>
  </div>

Mapa de Karnaugh dibujado sobre un toro y en un plano – las celdas marcadas con puntos son adyacentes.

Utilizando estos grupos, podemos formar la expresión simplificada: A · C + ¬B

<br>

## A1.2.5. Construye diagramas lógicos

### Diseño de circuitos digitales a partir de expresiones de álgebra booleana

Al comprender los principios del álgebra booleana, podemos simplificar expresiones lógicas complejas y traducirlas en diagramas de circuitos. Este proceso, que va desde la notación matemática abstracta hasta el diseño de circuitos, es esencial para crear sistemas digitales eficientes y fiables. Comenzaremos creando el circuito digital a partir de la expresión que se muestra a continuación:

```Y = (A · B) + (¬A · B)```

1. Comienza con dos entradas: A y B.

2. Trabaja sobre el primer paréntesis introduciendo una puerta AND (Y) y conectando tanto A como B a ella.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2067.%20K-map.png" alt="Imagen" width="370" height="auto"/>
  </div>

3. Trabaja sobre el segundo paréntesis, conectando A a una puerta NOT (NO) y B a otra puerta NOT.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2068.%20K-map.png" alt="Imagen" width="370" height="auto"/>
  </div>

4. Conecta ambas salidas a una puerta AND (Y).

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2069.%20K-map.png" alt="Imagen" width="550" height="auto"/>
  </div>

5. Ahora trabaja fuera de los paréntesis e introduce una puerta OR (O) para unirlas.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2070.%20K-map.png" alt="Imagen" width="550" height="auto"/>
  </div>
