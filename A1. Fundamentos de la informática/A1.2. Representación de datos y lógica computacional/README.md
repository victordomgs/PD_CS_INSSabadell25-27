<h1 align="center">A1.2. Representación de datos y lógica computacional
<div align="center">

</div>

## Contenido:

- [A1.2.1. Describe los principales métodos de representación de datos](#A121-describe-los-principales-métodos-de-representación-de-datos)  
- [A1.2.2. Explica cómo se utiliza el sistema binario para almacenar datos](#A122-explica-cómo-se-utiliza-el-sistema-binario-para-almacenar-datos)
- [A1.2.3. Describe el propósito y el uso de las puertas lógicas](#A123-describe-el-propósito-y-el-uso-de-las-puertas-lógicas)
- [A1.2.4. Construye y analiza tablas de verdad](#A124-construye-y-analiza-tablas-de-verdad)
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

#### Programming exercise

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

1. Después de estudiar cómo funciona este código, **escribe la función de descifrado** para alguien que reciba un mensaje cifrado.

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
| HD (720p)           | 1280 × 760           | Vídeo en HD, televisión HD básica |
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
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2024.%20Imagen%20de%20alta%20resoluci%C3%B3n.png" alt="Imagen" width="860" height="auto"/>
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
