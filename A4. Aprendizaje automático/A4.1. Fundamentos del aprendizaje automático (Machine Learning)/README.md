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

> [!WARNING]
> El **aprendizaje profundo (deep learning)** es un subconjunto del aprendizaje automático (machine learning). El aprendizaje profundo no es algo independiente del aprendizaje automático, sino más bien un enfoque específico dentro de él. Utiliza capas de redes neuronales para extraer de forma progresiva características de mayor nivel a partir de la entrada. El aprendizaje automático incluye muchos otros tipos de algoritmos que no requieren redes neuronales.

### Aprendizaje supervisado

El **aprendizaje supervisado** se refiere a un algoritmo que se entrena con conjuntos de datos etiquetados. Estos conjuntos de datos constan de valores de entrada de ejemplo y la respuesta de salida correcta que debe darse si el algoritmo detecta algo similar a esa entrada.

Por lo general, cuanto mayor y mejor sea el conjunto de datos, más precisos serán los resultados producidos por el algoritmo de aprendizaje supervisado. Los conjuntos de datos utilizados por las principales empresas tecnológicas contienen muchos millones de registros.

**Aprendizaje supervisado:** cuando a un algoritmo de aprendizaje automático se le proporciona un conjunto de datos de pares de elementos, donde el par consta de un valor y la respuesta que la red debe proporcionar si detecta dicho valor. Al aprender las respuestas a los valores dados, la red realizará generalizaciones para ser capaz de estimar la respuesta cuando se le presente un valor no visto previamente.

- **Regresión:** aprendizaje automático donde la salida generada debe ser un valor numérico.
- **Clasificación:** aprendizaje automático donde la salida generada debe ser una categoría, elegida de entre un conjunto discreto de categorías disponibles.

El aprendizaje supervisado puede utilizarse para tareas de regresión y de clasificación.

#### Tareas de regresión

Una tarea de regresión es aquella en la que el algoritmo predice un valor numérico para la salida dentro de un rango asignado, por ejemplo:

- Un algoritmo de **predicción de calificaciones** podría tomar como entradas las horas de estudio, el registro de asistencia, la participación en clase, las puntuaciones en exámenes anteriores y las horas dedicadas a los deberes; y devolver como salida una calificación final prevista en el rango 0–100.
- Un algoritmo de **previsión meteorológica** podría tomar como entradas las temperaturas históricas de cada día de la última semana, la humedad, la velocidad del viento y la presión atmosférica; y devolver como salida una temperatura prevista para el día siguiente en un rango determinado.

#### Tareas de clasificación

Una tarea de clasificación es aquella en la que el algoritmo predice a qué categoría pertenece el elemento de entrada; por ejemplo, un algoritmo de **reconocimiento de imágenes** podría recibir una imagen e intentar clasificarla como un perro o un muffin.

> [!WARNING]
> Ten clara la diferencia entre los resultados de las tareas de **regresión** y de **clasificación** en el aprendizaje supervisado. Los modelos de regresión predicen un resultado continuo (valores numéricos), mientras que los modelos de clasificación predicen resultados categóricos (etiquetas de clase).
> Por ejemplo, predecir el precio de una casa basándose en sus características (como el tamaño y la ubicación) es un problema de regresión porque el precio es una variable continua. Por otro lado, determinar si un correo electrónico es spam o no lo es, es un problema de clasificación porque hay categorías discretas para elegir.
> - Un algoritmo de clasificación de **géneros musicales** puede recibir como entrada el tempo, el ritmo, el tono y los instrumentos utilizados de una canción; y devolver como salida el género (pop, rock, hip-hop, clásica, etc.).
> - Un algoritmo de **reconocimiento de escritura** puede recibir la imagen de un carácter e intentar clasificarlo como una letra individual, un número o un signo de puntuación.

### Aprendizaje no supervisado

Aprendizaje no supervisado
El aprendizaje no supervisado es aquel en el que el algoritmo se construye para identificar patrones o estructuras dentro de sus conjuntos de datos sin que se le proporcione una etiqueta explícita que indique la salida correcta. Esto puede deberse a que la naturaleza de los datos no permite tener una respuesta "correcta" emparejada, o porque el algoritmo aprende constantemente basándose en interacciones del usuario que no tienen una respuesta fija acertada o errónea.

**Aprendizaje no supervisado:** método de aprendizaje automático donde el conjunto de datos no incluye las "respuestas" o salidas esperadas para los datos proporcionados. El algoritmo intentará descubrir los patrones por sí solo.

#### Ejemplos incluyen:

- **Algoritmos para identificar grupos sociales de un usuario:** Los datos de entrada pueden consistir en la actividad en redes sociales (me gusta, comentarios y seguidos). El algoritmo analiza estos datos para identificar a otros usuarios con conocidos mutuos o intereses similares. Curiosamente, este análisis puede realizarse sin necesidad del contenido de los mensajes; por eso empresas como WhatsApp ofrecen cifrado de extremo a extremo, ya que saber cuántos mensajes se intercambian entre usuarios es suficiente para realizar el análisis de grupos sociales.
- **Tiendas minoristas:** Utilizan el aprendizaje no supervisado para encontrar asociaciones y correlaciones entre los diferentes productos que compran los clientes. Los programas de fidelización permiten crear perfiles de datos para comparar clientes y personalizar estrategias de marketing.
- **Empresas de medios (Netflix, Spotify, YouTube):** Utilizan estos sistemas para perfeccionar sus recomendaciones de contenido futuro.

### Aprendizaje por refuerzo

En el aprendizaje por refuerzo, el algoritmo analiza sus datos de entrada, decide una salida particular y, posteriormente, se le informa de qué tan buena o mala fue esa decisión. Utiliza esa información para refinar acciones futuras ante situaciones similares. Puede entenderse como un aprendizaje basado en el ensayo y error.

**Aprendizaje por refuerzo:** aprendizaje automático por ensayo y error. Basándose en lo aprendido en cada momento, el algoritmo selecciona una acción en un entorno determinado. El entorno proporciona una retroalimentación (llamada "recompensa"), que el algoritmo utiliza para aprender y perfeccionar su proceso de toma de decisiones.

#### Situaciones comunes donde se utiliza:

- **Videojuegos:** Para entrenar jugadores de IA o bots.
- **Robótica:** Para enseñar a un robot a caminar o manipular objetos. Los coches autónomos también lo utilizan para navegar de forma más segura entre el tráfico.
- **Finanzas:** Bots que operan en bolsa y reciben retroalimentación según si ganaron o perdieron dinero en la operación.
- **Sistemas de recomendación:** Se utiliza para refinar sugerencias basándose en la interacción real del usuario (¿vio o escuchó el elemento sugerido?).

### Aprendizaje por transferencia (Transfer learning)

El **aprendizaje por transferencia** es aquel en el que el conocimiento obtenido al resolver un problema puede utilizarse para ayudar a resolver un problema diferente, pero relacionado en cierta medida. La ventaja del aprendizaje por transferencia es que requiere menos datos, ya que el algoritmo ya está parcialmente entrenado y puede que solo necesite un pequeño ajuste fino (fine-tuning) para la nueva tarea que se le solicita.

**Aprendizaje por transferencia:** cuando un modelo de aprendizaje automático previamente entrenado se aplica a una situación, contexto o problema similar pero nuevo. El objetivo es acelerar el proceso de entrenamiento utilizando un modelo ya entrenado, incluso si el problema es ligeramente distinto.

#### Considera los siguientes ejemplos:

- **Reconocimiento de imágenes:** Partiendo de un modelo que ha sido entrenado con un conjunto de datos masivo como ImageNet (más de un millón de imágenes etiquetadas y 1000 categorías diferentes), el aprendizaje por transferencia podría tomar ese modelo y ajustarlo para reconocer tipos específicos de objetos, como una especie de flor o una raza de perro. El modelo ya sería experto en procesar imágenes e identificar características como bordes y formas, por lo que solo necesitaría aprender a distinguir entre las nuevas categorías.
- **Reconocimiento de voz:** Utilizando un modelo generalizado que ha sido entrenado en lenguaje hablado para transcribirlo a texto, el aprendizaje por transferencia puede usarse para adaptarlo a acentos particulares o jerga especializada dentro de una industria específica.
- **Chatbot personalizado:** Utilizando un modelo LLaMA (Large Language Model Meta AI) preentrenado y disponible públicamente, una empresa podría ajustarlo entrenándolo con registros de atención al cliente para crear un chatbot que pueda añadirse a su sitio web para gestionar consultas específicas de su sector.
- **Generadores de imágenes personalizados:** Los modelos preentrenados para herramientas como Stable Diffusion pueden ampliarse y ajustarse más a fondo para generar imágenes que imiten un estilo artístico particular, o especializarse en imágenes para una industria o dominio concreto. Esto puede hacerse de forma relativamente rápida y sencilla sin la carga de repetir la tarea masiva del entrenamiento original que requirió el modelo base.

> [!WARNING]
> El aprendizaje por transferencia no consiste simplemente en utilizar un modelo preentrenado. Implica **adaptar** un modelo desarrollado para una tarea con el fin de resolver otra relacionada; no es solo reutilizar un modelo existente sin modificaciones. Es crucial cuando los datos escasean o cuando se trata de tareas similares.

## A4.1.2 Requisitos de hardware

El hardware necesario para fines de aprendizaje automático continuará innovando y evolucionando a lo largo de la vida útil de este texto. En consecuencia, esta sección no ofrecerá recomendaciones sobre números de modelo específicos de procesadores, sino que analizará las categorías generales de tecnología de hardware disponibles y sus diversos casos de uso.

### Plataformas informáticas
#### Portátiles estándar
El punto de partida es, obviamente, el portátil estándar disponible en el mercado minorista. Al momento de escribir esto, podría tratarse de un procesador i7 con 16 GB o 32 GB de RAM, o un equivalente de Apple Silicon.

Estas máquinas suelen limitarse a tareas de aprendizaje automático a pequeña escala, como el desarrollo y la prueba de un modelo sencillo. Para fines educativos, se puede hacer mucho con un portátil estándar, pero no sería recomendable entrenar un modelo de grado comercial con dicho equipo, ya que sería demasiado lento y carecería de memoria o almacenamiento suficiente.

Algunos avances recientes buscan mejorar la capacidad de los portátiles estándar en lo que respecta al aprendizaje automático. Uno de ellos es la introducción de los procesadores Apple Silicon M en los MacBooks. Apple integra la CPU, la GPU, el motor neuronal (neural engine) y otros componentes en una única estructura de sistema en un chip (SoC), lo que permite un mejor rendimiento y eficiencia energética. Al integrar las funciones de CPU y GPU en un solo chip, estas agrupan y comparten la misma memoria. Esto contrasta con el enfoque tradicional en el que las GPU tienen su propia memoria dedicada, separada de la RAM utilizada por la CPU. Por esta razón, quienes tienen un ordenador basado en Apple Silicon a menudo pueden realizar tareas de aprendizaje automático que los propietarios de portátiles Intel tradicionales no pueden hacer sin acceso a una GPU dedicada.

Para no permitir que los usuarios de Windows se queden atrás, Microsoft ha lanzado su marca apoyada por IA, Microsoft Copilot, que requiere que los portátiles tengan una unidad de procesamiento neuronal (NPU) integrada, la cual se analiza más adelante en la sección relativa a las CPU.

#### Estación de trabajo dedicada (Workstation)
Después de un portátil estándar, el siguiente paso sería la compra de una estación de trabajo de sobremesa dedicada con una GPU, como una NVIDIA RTX.

Tener una GPU real puede ofrecer una mejora de un orden de magnitud en las velocidades de procesamiento para los cálculos de aprendizaje automático y serviría como una excelente plataforma para proyectos bastante sofisticados.

La ventaja principal de una GPU es su capacidad de procesamiento en paralelo, que proviene de tener miles de pequeños núcleos de procesamiento optimizados para tal fin. Los algoritmos de aprendizaje automático a menudo implican realizar los mismos cálculos sobre grandes cantidades de datos; las GPU pueden realizar estos mismos cálculos sobre diferentes valores simultáneamente, mientras que una CPU tiene que ponerlos en cola para procesarlos uno por uno.

#### Dispositivos periféricos (Edge devices)
Los dispositivos Edge se refieren a sistemas informáticos que realizan el procesamiento de datos en el lugar (o cerca de él) donde se generan los datos, en lugar de depender de recursos informáticos centralizados como la nube.

Procesar los datos localmente reduce la necesidad de enviarlos de ida y vuelta a un centro de datos distante. Esta reducción en la transmisión de datos tiene el beneficio adicional de mejorar la privacidad y la seguridad. La desventaja es que sigues comprometido a invertir tú mismo en la infraestructura física de hardware, junto con toda la carga de trabajo de mantenimiento asociada.

#### Plataformas basadas en la nube
Para realizar el entrenamiento de modelos grandes o complejos, generalmente se requiere el uso de plataformas en la nube (en lugar de invertir uno mismo en una infraestructura masiva). Las plataformas en la nube son accesibles a través de Internet y proporcionan servicios bajo demanda a usuarios de todo el mundo.

Estos proveedores de la nube le permiten variar la combinación y las especificaciones de las CPU, GPU y Unidades de Procesamiento de Tensores (**TPU**) disponibles para su proyecto según sea necesario. También pueden escalar para proporcionar grandes cantidades de RAM, almacenamiento y conectividad de red. Los servicios en la nube también son útiles para el despliegue de su modelo como una API para que otros sistemas accedan a él.

El principal inconveniente de las plataformas en la nube es la dependencia que tendrá su proyecto de un proveedor externo. Debe confiar en sus medidas de seguridad de red y datos; debe transmitir sus datos a su red para que realicen las tareas por usted; y se está comprometiendo a los costes de suscripción mensual implicados. La flexibilidad de los sistemas en la nube siempre conlleva un coste, y esto no debe tomarse a la ligera.

Al momento de escribir esto, los principales líderes de la industria que proporcionan plataformas en la nube con equipo especializado en aprendizaje automático incluyen AWS, Google Cloud y Microsoft Azure. Una buena herramienta para comenzar con requisitos de configuración mínimos es Google Colab; permite crear un Python Notebook y utilizar tecnología GPU o TPU simplemente cambiando los ajustes en el menú "Entorno de ejecución" (Runtime).

#### Centros de computación de alto rendimiento (HPC)
A diferencia del enfoque de pago por uso disponible para el público de los proveedores en la nube, los centros **HPC (High-Performance Computing)** son instalaciones dedicadas, diseñadas para dar soporte a objetivos de investigación académica o científica a gran escala. Por este motivo, el acceso a un HPC está más restringido y suele requerir una membresía, afiliación a una institución académica o de investigación, o procesos específicos de subvenciones de investigación y asignación de tiempos.

Son centros de datos diseñados para ser adecuados para cargas de trabajo altamente exigentes que requieren recursos de computación de alto rendimiento de forma sostenida. Están construidos bajo un modelo orientado a tareas computacionales intensivas en recursos, no bajo un modelo de "servicios a la carta" (as-a-service).

Muchas universidades han realizado inversiones en sus propios centros HPC para que sean utilizados por sus estudiantes de investigación.

### Procesadores para el aprendizaje automático
Una vez analizadas las diversas plataformas disponibles para acceder a la potencia de cálculo necesaria, es momento de revisar la electrónica interna de los ordenadores que hace posible el aprendizaje automático.

#### Unidades centrales de procesamiento (CPU)
Las CPU son los procesadores de propósito general que se encuentran en todos los sistemas informáticos modernos. Están diseñadas para realizar una amplia gama de operaciones, son muy flexibles y pueden procesar tareas complejas. No son dispositivos especializados diseñados específicamente para el aprendizaje automático. Aunque es viable realizar algunas tareas introductorias con una CPU, generalmente están limitadas a procesos que no requieren un procesamiento en paralelo intensivo.

Recientemente, se han integrado Unidades de procesamiento neuronal (NPU) junto a las CPU tradicionales en portátiles de consumo. Las NPU son procesadores especializados diseñados específicamente para manejar los cálculos que requieren las redes neuronales y el aprendizaje profundo, como las operaciones de matrices y vectores. Al contar con procesadores especializados, el dispositivo ofrece tiempos de procesamiento más rápidos y un menor consumo de energía en tareas de IA en comparación con las CPU de propósito general.

A partir de 2024, los portátiles comercializados con soporte de IA para Microsoft Copilot incluyen NPU con una capacidad mínima de 40 TOPS (billones de operaciones por segundo).

#### Unidades de procesamiento gráfico (GPU)
Las GPU contienen cientos o miles de núcleos pequeños diseñados para tareas altamente paralelas, como el renderizado de gráficos. La GPU permite que todos los núcleos realicen el mismo cálculo sobre diferentes valores simultáneamente; por tanto, si hay grandes matrices que procesar donde cada elemento requiere la misma operación, las GPU ofrecen un ahorro de tiempo significativo. Las GPU destacan en el procesamiento paralelo de operaciones de matrices y vectores, que es precisamente la matemática que forma la base de las redes neuronales.
La presencia de una GPU dedicada a menudo puede mejorar la velocidad de entrenamiento hasta diez veces en comparación con el uso exclusivo de una CPU.

#### Unidades de procesamiento de tensores (TPU)
Partiendo de la idea de la GPU, la TPU fue diseñada a medida por Google específicamente para cálculos de tensores. Están optimizadas para cálculos de gran volumen y baja precisión con el fin de aumentar la eficiencia en tareas de redes neuronales.

"Baja precisión" en este contexto suele significar que los cálculos ocurren a un máximo de 16 bits, en contraste con los 32 o 64 bits de una GPU normal. El aprendizaje automático generalmente no requiere ese nivel de precisión, por lo que 16 bits o incluso 8 bits son suficientes.

- **Tensor:** término matemático para una matriz de tres o más dimensiones. Un solo número (sin dimensiones) se conoce como "escalar". Una matriz de una dimensión es un "vector". Una de dos dimensiones es una "matriz". Tres o más dimensiones se denomina "tensor".

En el corazón de una TPU hay una gran unidad de multiplicación de matrices. Dado que la multiplicación de matrices es fundamental para las redes neuronales, tener una unidad optimizada específicamente para esta tarea hace que las TPU sean ideales para el aprendizaje automático. La biblioteca TensorFlow está adaptada para utilizar TPU cuando están disponibles, y servicios como Google Colab las ponen fácilmente a disposición del público general.

#### Circuitos integrados de aplicación específica (ASIC)
Los ASIC se diseñan a medida para un uso específico en lugar de para la informática de propósito general. Están diseñados para realizar un conjunto particular de tareas con una eficiencia óptima. Ofrecen un rendimiento máximo, pero carecen de la flexibilidad de una CPU.

Si su carga de trabajo de aprendizaje automático está definida con precisión y no cambiará mucho con el tiempo, un ASIC puede realizar estas tareas más rápido que una GPU o TPU. Debido a su especialización, tienden a ser más eficientes energéticamente y tienen menores costes operativos a largo plazo. La desventaja es que el coste inicial es muy alto, ya que los chips requieren diseño y desarrollo personalizados. Esto significa que solo son viables cuando una aplicación se va a desplegar a gran escala.
Ejemplos de ASIC producidos en masa incluyen los chips de la serie A de Apple (usados en iPhones) y los Snapdragon de Qualcomm.

#### Matrices de puertas lógicas programables en campo (FPGA)
Las FPGA pueden programarse y reprogramarse para realizar tareas informáticas especializadas, ofreciendo un equilibrio entre la flexibilidad de las CPU/GPU y la eficiencia de los ASIC. Son ideales para el prototipado de modelos de aprendizaje automático o aplicaciones que requieren aceleración de hardware personalizada que puede cambiar con el tiempo. Por ejemplo, se utilizan en sistemas de trading de alta frecuencia, donde los microsegundos marcan la diferencia en la rentabilidad.

> [!WARNING]
> Hay muchas tecnologías distintas en este tema y es normal no tener experiencia directa con todas. Aquí tienes un resumen de sus diferencias:
> - **ASIC:** Diseñados para tareas específicas y no son reprogramables.
> - **FPGA:** Son versátiles y pueden reprogramarse.
> - **GPU:** Ideales para tareas de procesamiento en paralelo (gráficos y cálculos masivos).
> - **TPU:** Chips especializados diseñados por Google, optimizados para cálculos de tensores en modelos a gran escala.
> - **NPU:** Diseñadas para acelerar cálculos de redes neuronales en dispositivos de consumo (móviles y portátiles).
