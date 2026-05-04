<h1 align="center">A4.1. Fundamentos del aprendizaje automático (Machine Learning)
<div align="center">

</div>

## Contenido:

- [A4.1.1 Describir los tipos de aprendizaje automático y sus aplicaciones en el mundo real](#A411-describir-los-tipos-de-aprendizaje-automático-y-sus-aplicaciones-en-el-mundo-real)
- [A4.1.2 Describir los requisitos de hardware para diversos escenarios donde se implementa el aprendizaje automático](#A412-describir-los-requisitos-de-hardware-para-diversos-escenarios-donde-se-implementa-el-apdrendizaje-automático)

<br>

## A4.1.1 Tipos de aprendizaje automático y sus aplicaciones

### TDC (Teoría del Conocimiento)
#### ¿Qué se considera conocimiento?
Los modelos de aprendizaje automático "aprenden" a partir de datos, lo que plantea interrogantes sobre qué constituye el conocimiento. Las perspectivas sobre el conocimiento suelen distinguir entre el conocimiento adquirido a través de la experiencia (empírico) y el conocimiento adquirido a través del razonamiento (racional).

Los modelos de aprendizaje automático adquieren conocimiento de forma empírica mediante el procesamiento de vastas cantidades de datos. Sin embargo, a diferencia de los humanos, las máquinas no "entienden" ni razonan sobre estos datos en el sentido humano. Esto plantea la pregunta: ¿pueden los patrones y las predicciones que generan las máquinas considerarse "conocimiento", o son simplemente resultados de datos procesados?

¡Bienvenido al mundo del aprendizaje automático! Vivimos en una época de crecimiento emocionante y rápida innovación. La **IA generativa** está ocupando los titulares mundiales y ha cambiado nuestra forma de vivir y trabajar en un periodo de tiempo muy corto. Abunda la especulación de que la "IA general" no está lejos de convertirse en realidad. Ciertamente, es un tema apasionante, pero ¿qué son el aprendizaje automático y la inteligencia artificial, y cómo funcionan? El objetivo de este capítulo es que comprendas qué ocurre "entre bastidores".

- **IA generativa:** una forma de inteligencia artificial capaz de generar texto, imágenes, audio, vídeo y otros artefactos digitales, generalmente en respuesta a una instrucción (prompt). Es una forma que está experimentando avances rápidos en el momento de escribir este texto.
- **Aprendizaje automático (Machine Learning):** una rama de la IA donde las computadoras aprenden de datos y experiencias para realizar tareas específicas o resolver problemas concretos, sin estar explícitamente programadas para ello.
- **Inteligencia artificial:** tecnología informática capaz de realizar tareas y tomar decisiones de una manera que imita la inteligencia humana. Existen dos formas principales de IA:
- **IA estrecha (o débil):** diseñada para realizar tareas específicas o resolver tipos específicos de problemas.
- **IA general (o fuerte):** posee inteligencia de nivel humano y puede operar en una amplia gama de dominios. Aunque persiste la especulación de que la IA general está "cerca", en este momento solo está disponible la tecnología de IA estrecha.

Este capítulo no pretende diseccionar los detalles de los últimos y más mediáticos desarrollos en el campo. Eso sería una tarea inútil, ya que quedarían obsoletos antes de que el libro se imprima. En su lugar, el objetivo es darte una comprensión sólida de las **teorías y técnicas fundamentales** que forman la base de todo el campo del aprendizaje automático. A partir de estos cimientos, estarás en una posición mucho más sólida para comprender las verdaderas implicaciones de los desarrollos modernos que ocurren en el sector.

Antes de seguir adelante, es importante aclarar y diferenciar los términos aprendizaje automático (ML) e inteligencia artificial (AI). La **inteligencia artificial** es un campo amplio que busca crear sistemas capaces de realizar tareas que normalmente requieren inteligencia humana. Esto puede incluir, entre otros, el razonamiento, el aprendizaje, la percepción, la resolución de problemas, la comprensión y la interacción. El **aprendizaje automático** es un subconjunto de la inteligencia artificial que se centra en el aspecto del aprendizaje. Busca enseñar a las computadoras a aprender de los datos, identificar patrones en ellos y tomar decisiones basadas en lo aprendido, con una intervención humana mínima. La implementación programática del aprendizaje automático depende en gran medida de las matemáticas de la **estadística, el álgebra lineal y el cálculo**.

Las aplicaciones de aprendizaje automático se utilizan cada vez más en el comercio, la industria, la investigación y el gobierno. Se emplean para todo, desde el análisis de mercado hasta la robótica, desde el arte generativo hasta el diagnóstico de condiciones médicas. Las aplicaciones del aprendizaje automático no harán más que crecer a medida que la tecnología continúe desarrollándose.

Dentro del aprendizaje automático, existen muchas otras subcategorías que consideraremos en la sección *A4.3 Enfoques de aprendizaje automático*. Estas pueden describirse a grandes rasgos como:

- **Aprendizaje supervisado:** regresión lineal.
- **Aprendizaje supervisado:** clasificación.
- **Aprendizaje no supervisado:** agrupamiento (clustering).
- **Aprendizaje no supervisado:** regla de asociación.
- **Aprendizaje por refuerzo.**
- **Algoritmos genéticos.**
- **Redes neuronales artificiales.**
- **Redes neuronales convolucionales.**

> [!TIP]
> Tómate el tiempo necesario para apreciar las diferencias entre los tipos de aprendizaje automático: **supervisado, no supervisado, por refuerzo, aprendizaje profundo (deep learning) y aprendizaje por transferencia**. Debes saber para qué escenarios es más adecuado cada uno y cuáles son los algoritmos típicos utilizados en cada categoría. En este tema, los términos y las definiciones son fundamentales para responder preguntas teóricas con precisión. Usar la terminología en un contexto incorrecto te restará puntos en la evaluación.

### Aprendizaje profundo (Deep learning)

El término "aprendizaje profundo" se utiliza para denotar el uso de una red neuronal dentro de un algoritmo de aprendizaje automático. Existe una gran variedad de técnicas de aprendizaje automático que funcionan perfectamente sin necesidad de una red neuronal; por lo tanto, el término "aprendizaje profundo" se emplea para distinguir entre aquellas que utilizan una red neuronal y las que no. Por ejemplo, se puede hacer referencia al "aprendizaje por refuerzo" y al "aprendizaje por refuerzo profundo".

- **Red neuronal:** un algoritmo informático que imita el diseño del cerebro humano mediante el uso de un conjunto de nodos interconectados para el procesamiento y análisis de datos.

Una red neuronal consiste en algoritmos y estructuras de datos construidos de tal manera que replican la comprensión biológica de cómo funciona el cerebro: como una red interconectada de neuronas, cada una de las cuales tiene varias conexiones de entrada y genera una salida basada en la combinación de dichas entradas.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A4.%20Aprendizaje%20autom%C3%A1tico/images/Figura%201.jpg" alt="Computación" width="650" height="auto"/>
    <p><em>Figura 1: Comparación de una neurona biologica con una red neuronal. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>
