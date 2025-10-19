<h1 align="center">A1.2. Representación de datos y lógica computacional
<div align="center">

</div>

## Contenido:

- [A1.2.1. Describe los principales métodos de representación de datos](#A121-describe-los-principales-métodos-de-representación-de-datos)  
- [A1.2.2. Explica cómo se utiliza el sistema binario para almacenar datos](#A122-explica-cómo-se-utiliza-el-sistema-binario-para-almacenar-datos)
- [A1.2.3. Describe el propósito y el uso de las puertas lógicas](#A123-describe-el-propósito-y-el-uso-de-las-puertas-lógicas)
- [A1.2.4. Construye y analiza tablas de verdad](#A124-construye-y-analiza-tablas-de-verdad) 
- [A1.2.5. Ciclo de búsqueda, decodificación y ejecución](#A125-construye-diagramas-lógicos) 

<br>

## A1.2.1. Describe los principales métodos de representación de datos

El sistema binario (base 2) es el lenguaje de los ordenadores modernos; sin embargo, no siempre fue así. Durante el desarrollo de los primeros ordenadores se probaron varios sistemas numéricos. Charles Babbage, el inventor de la Máquina Analítica, utilizó el sistema decimal en sus invenciones. Esto parecía una elección lógica, ya que las personas ya usaban comúnmente la base 10.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2020.%20The%20analytical%20engine.jpg" alt="Engine" width="550" height="auto"/>
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
