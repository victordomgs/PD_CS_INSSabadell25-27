<h1 align="center">A1.2. Representación de datos y lógica computacional
<div align="center">

</div>

## Contenido:

- [A1.2.1. Describe los principales métodos de representación de datos](#A121-describe-los-principales-métodos-de-representación-de-datos)  
- [A1.2.2. Explica cómo se utiliza el sistema binario para almacenar datos](#A122-explica-cómo-se-utiliza-el-sistema-binario-para-almacenar-datos)
- [A1.2.3. Describe el propósito y el uso de las puertas lógicas](#A123-describe-el-propósito-y-el-uso-de-las-puertas-lógicas)
- [A1.2.4. Construye y analiza tablas de verdad](#A124-construye-y-analiza-tablas-de-verdad) 

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
