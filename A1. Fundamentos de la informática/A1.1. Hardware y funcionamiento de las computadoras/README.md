<h1 align="center">A1.1. Hardware y funcionamiento de las computadoras
<div align="center">

</div>

## Contenido:

- [A1.1.1. Funciones e interacciones de los principales componentes de la CPU](#A111-funciones-e-interacciones-de-los-principales-componentes-de-la-CPU)  
- [A1.1.2. Función de una GPU](#A112-función-de-una-GPU)
- [A1.1.3. Diferencia entre CPU y GPU](#A113-diferencia-entre-CPU-y-GPU)
- [A1.1.4. Propósitos de los diferentes tipos de memoria principal](#A114-propósitos-de-los-diferentes-tipos-de-memoria-principal) 
- [A1.1.5. Ciclo de búsqueda, decodificación y ejecución](#A115-ciclo-de-búsqueda-decodificación-y-ejecución) 
- [A1.1.6. Tipos externos e internos de memoria secundaria](#A116-tipos-externos-e-internos-de-memoria-secundaria)
- [A1.1.7. Concepto de compresión](#A117-concepto-de-compresión)
- [A1.1.8. Servicios de computación en la nube](#A118-servicios-de-computación-en-la-nube)

<br>

## A1.1.1. Funciones e interacciones de los principales componentes de la CPU

### ¿Qué es la unidad central de procesamiento?
La **unidad central de procesamiento (CPU)** a menudo se refiere como el “cerebro” del ordenador. Es un componente crítico que lleva a cabo la mayor parte del procesamiento dentro de un dispositivo.

La CPU está compuesta por dos unidades principales: la **unidad de control (CU)** y **la unidad aritmético-lógica (ALU)**.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%201.%20Modelo%20de%20CPU.png" alt="CPU Model" width="450" height="auto"/>
    <p><em>Figura 1: Modelo de CPU. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

#### Unidad de control (CU)
La unidad de control **dirige las operaciones del procesador**. Es responsable del ciclo de **búsqueda–decodificación–ejecución**, gestionando las tres operaciones y dirigiendo la memoria del ordenador, la ALU y los dispositivos de entrada/salida para que respondan de manera adecuada.

#### Unidad aritmético-lógica (ALU)
Esta unidad es responsable de **realizar operaciones aritméticas y lógicas**. Estas incluyen operaciones aritméticas básicas como la suma, resta, multiplicación y división, así como **operaciones lógicas** incluyendo AND, OR, XOR y NOT.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%202.%20Central%20processing%20unit%20(CPU).jpg" alt="CPU" width="350" height="auto"/>
    <p><em>Figura 2: Central Processing Unit. Fuente: PcCompomentes</em></p>
  </div>

###  ¿Qué son los registros?
Los registros son cantidades muy pequeñas de almacenamiento que están disponibles directamente en la CPU para **mantener datos temporales** con los que la CPU puede estar trabajando. Los registros son el **registro de instrucciones** (IR), el **contador de programa** (PC), el **registro de direcciones de memoria** (MAR), el **registro de datos de memoria** (MDR) y el **acumulador** (AC).

#### Registro de instrucciones
Cuando una instrucción es captada desde la memoria, se mantiene en el IR dentro de la CPU. Este registro contiene la instrucción que está siendo ejecutada actualmente por la CPU.

#### Contador de programa
El PC contiene **la dirección de la siguiente instrucción** que debe ser captada desde la memoria. Una vez que la instrucción ha sido captada, el PC se actualiza para apuntar a la siguiente instrucción que será necesaria.

#### Registro de direcciones de memoria
El MAR contiene **la dirección de memoria que está siendo captada actualmente**. El contenido del PC se copia en el MAR, y el MAR proporciona esta dirección a la unidad de memoria, de modo que los datos e instrucciones puedan ser leídos desde o copiados a esa ubicación.

#### Registro de datos de memoria
Este contiene los datos que han sido captados o que están a punto de ser escritos en la dirección de memoria que está actualmente en el MAR.

#### Acumulador (AC)
Este almacena los resultados aritméticos o lógicos intermedios producidos por la ALU.

## ¿Qué son los buses?
Los buses son un **componente crítico** del sistema informático, ya que transfieren datos entre varios dispositivos, incluyendo la CPU, la memoria, el almacenamiento y los periféricos. Los buses tienen anchos que se miden en bits. Cuanto mayor es el ancho del bus, más datos puede transmitir a la vez.
Existen tres tipos principales de buses: bus de control, bus de datos y bus de direcciones.

### Bus de control
El bus de control se utiliza para transmitir señales de comando y de control desde la CPU a otros componentes del sistema, y viceversa. Debido a la necesidad de que las señales sean enviadas y recibidas, este bus es bidireccional. Algunas de las señales que se transmitirían a través del bus de control son operaciones de lectura/escritura, peticiones de interrupción, señales de reloj para sincronización y señales de estado de los componentes de hardware.

### Bus de datos
El bus de datos **transporta los datos que están siendo procesados entre la CPU, la memoria y otros periféricos**. El ancho del bus de datos es importante para determinar la cantidad de datos que puede transferir a la vez. Los anchos comunes de los buses de datos son 8, 16, 32 y 64 bits. Como los datos necesitan ser leídos y escritos en la memoria, los buses de datos suelen ser bidireccionales.

### Bus de direcciones
El bus de direcciones se utiliza para transmitir la dirección que debe ser leída o escrita en la memoria. El ancho de este bus determina la capacidad de memoria del sistema. Por ejemplo, un bus de direcciones de **32 bits** puede direccionar $2^{32}$ ubicaciones de memoria.

### ¿Qué son los núcleos?
Las CPU vienen en varias configuraciones diferentes. Estas incluyen procesadores de un solo **núcleo**, **procesadores multinúcleo** y **coprocesadores**.

#### Procesadores de un solo núcleo
Esta CPU tiene una **única unidad de procesamiento**, lo que significa que solo puede manejar una tarea a la vez. Se encuentran con mayor frecuencia en ordenadores de **gama baja** o en **máquinas más antiguas**. Son adecuados para tareas simples que no requieren un alto nivel de multitarea. Los procesadores de un solo núcleo pueden ejecutar más de una aplicación a la vez, pero la CPU tiene que ser compartida entre estas aplicaciones, lo cual puede afectar al rendimiento.

#### Procesadores multinúcleo
Una **CPU con procesadores multinúcleo** tiene dos o más núcleos que pueden ejecutar múltiples instrucciones simultáneamente. A menudo se les denomina como de doble núcleo (dos procesadores), de cuatro núcleos (cuatro procesadores), de seis núcleos (hexa-core) o de ocho núcleos (octa-core). Su rendimiento es **significativamente más rápido que el de los procesadores de un solo núcleo** y son ideales para la multitarea, los videojuegos y los servidores. Sin embargo, el software debe estar escrito para aprovechar estos núcleos adicionales. El software más antiguo que no hace esto probablemente se ejecute a una velocidad similar a la de un procesador de un solo núcleo.

#### Coprocesadores
Un **coprocesador es un tipo especial de procesador que tiene una tarea específica para apoyar a la CPU principal**. Están construidos con un propósito concreto para lograr un rendimiento óptimo en comparación con una CPU de propósito general. Las tareas se descargan de la CPU al coprocesador para que puedan ejecutarse en paralelo, mejorando el rendimiento del sistema. Ejemplos de coprocesadores son las unidades de procesamiento gráfico (cubiertas en la Sección A1.1.2), los procesadores de audio y **los procesadores de señal digital (DSP)**, que se utilizan en telecomunicaciones y compresión de imágenes.

<br>

## A1.1.2. Función de una GPU

Una **unidad de procesamiento gráfico (GPU)** es un circuito electrónico especializado diseñado para acelerar el renderizado de imágenes, videos y animaciones mediante la realización de cálculos matemáticos rápidos. Inicialmente desarrolladas para manejar las exigentes **cargas de trabajo gráficas de los videojuegos y las aplicaciones visuales**, las GPU han evolucionado hasta desempeñar un papel crucial en diversos campos más allá del renderizado gráfico.

Su estructura, compuesta por **miles de núcleos pequeños y eficientes**, les permite procesar múltiples tareas simultáneamente, lo que las hace excepcionalmente adecuadas para aplicaciones computacionalmente intensivas. Esta capacidad ha llevado a su amplia adopción en la investigación científica, el aprendizaje automático, la inteligencia artificial y la minería de criptomonedas.

Al descargar estas tareas intensivas de la CPU, las GPU mejoran el rendimiento general del sistema, permitiendo un procesamiento y una visualización de datos más rápidos y eficientes.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%203.%20Graphic%20processing%20unit%20(GPU).jpg" alt="GPU" width="650" height="auto"/>
    <p><em>Figura 3: Graphic Processing Unit. Fuente: PcCompomentes</em></p>
  </div>

### Procesamiento gráfico

Las **GPU** están diseñadas con una estructura altamente paralela, lo que les permite realizar muchos cálculos simultáneamente. Esto las hace excepcionalmente adecuadas para renderizar los gráficos complejos e intensivos en recursos que se ven en los videojuegos y aplicaciones modernas.

También manejan la aplicación de **shaders y textures a modelos 3D**, lo que incluye iluminación, sombreado y mapeado de texturas, mejorando el realismo de la escena.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%204.%20Gr%C3%A1ficos%20de%20videojuegos.jpg" alt="GPU" width="750" height="auto"/>
    <p><em>Figura 4: Gráficos de videojuegos. Fuente: GAME</em></p>
  </div>

### Procesamiento de video

Las GPU ayudan en la decodificación y codificación de archivos de video, haciendo que procesos como la reproducción, la transmisión y la edición sean más eficientes y rápidos. Esto es particularmente útil para quienes trabajan con archivos de **video de alta resolución de 4K o superior**.

### Inteligencia artificial y aprendizaje automático

Las **GPU** fueron creadas originalmente para el procesamiento gráfico; sin embargo, a principios de los 2000, investigadores e ingenieros comenzaron a reconocer su potencial para manejar cálculos de propósito general, incluyendo aquellos requeridos para el **aprendizaje automático** y la **IA**.

El cambio hacia el uso de GPUs para esto se debió en gran parte a su capacidad de realizar muchos cálculos simples simultáneamente, y porque muchas GPU pueden ejecutarse en paralelo.

Muchos **modelos de IA dependen en gran medida de las multiplicaciones de matrices y vectores**, y las GPU superan ampliamente a una CPU cuando intentan procesar esto rápidamente.

### Blockchain y minería de criptomonedas

En 2010, el uso de GPUs para la **minería de Bitcoin** se disparó cuando los mineros descubrieron que las GPUs superaban significativamente a las CPUs en la resolución de acertijos criptográficos, como encontrar el nonce en el algoritmo de **hash** para el sistema de **proof-of-work**.

Esta constatación llevó a un cambio drástico hacia la minería con GPU. El auge de las criptomonedas entre 2017 y 2021 aumentó aún más la demanda de GPUs, lo que resultó en precios por las nubes y escasez global.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%205.%20Bitcoin.jpg" alt="Bitcoin" width="550" height="auto"/>
    <p><em>Figura 5: Bitcoin. Fuente: Freepik</em></p>
  </div>

> [!NOTE]  
> El auge de las criptomonedas – en su punto máximo en noviembre de 2021, la capitalización total de mercado de las criptomonedas alcanzó aproximadamente los 3 billones de dólares

A partir de 2023, esta demanda se había reducido un poco y los precios de las GPUs se estaban volviendo más estables. Esto se debió a varias razones:

La **volatilidad** y la **menor rentabilidad** de la minería de criptomonedas habían reducido la demanda de GPUs, específicamente para fines de minería.

Los grandes fabricantes habían incrementado la producción para satisfacer la demanda.

Los circuitos integrados de aplicación específica (ASICs), que están diseñados específicamente para la minería, habían reemplazado en gran medida el uso de GPUs en muchas operaciones de minería.

<br>

## A1.1.3. Diferencia entre CPU y GPU

La **unidad central de procesamiento (CPU)** y la **unidad de procesamiento gráfico (GPU)** son ambos componentes fundamentales de los ordenadores modernos. Están diseñados de manera diferente, lo que explica por qué se utilizan para distintos tipos de tareas. **La CPU es excelente para manejar diversos trabajos, mientras que la GPU es mejor para realizar la misma tarea muchas veces sobre grandes cantidades de datos a la vez**.

### Filosofías de diseño

Las **CPU** se denominan generalmente **procesadores de propósito general** porque pueden manejar muchos tipos de tareas. Están diseñadas para ejecutar el sistema operativo, procesar la entrada del usuario y gestionar programas. Las CPU son buenas para tareas en las que hay que tomar decisiones rápidamente y en las que se realizan diferentes tipos de trabajo al mismo tiempo.

Las **GPU** son **procesadores especializados** porque se centran en tipos específicos de tareas. Están hechas para procesar grandes volúmenes de datos en paralelo. Esto significa que pueden trabajar en muchos cálculos al mismo tiempo. Por ejemplo, las GPU se utilizan para procesar imágenes y videos porque pueden trabajar sobre miles de píxeles simultáneamente.

### Arquitectura del núcleo

La **CPU** tiene solo unos **pocos núcleos**, **pero estos núcleos son muy potentes**. Cada núcleo puede manejar muchas instrucciones diferentes, pero funciona mejor cuando realiza una tarea a la vez. Esto hace que la CPU sea muy adecuada para tareas como **ejecutar el sistema operativo**, donde se necesitan respuestas rápidas. Las CPU también incluyen características como la **predicción de saltos** (donde la CPU intenta adivinar qué ocurrirá a continuación) y la ejecución fuera de orden (donde la CPU puede trabajar en tareas que ya están listas antes que en otras).

La GPU tiene **muchos núcleos más pequeños**. Estos núcleos no son tan potentes como los de la CPU, pero hay **miles de ellos**, y todos **trabajan al mismo tiempo**. Por eso, la GPU es muy buena para tareas como el **renderizado de imágenes 3D**, donde se deben realizar muchos cálculos similares simultáneamente. La arquitectura de la GPU está diseñada para trabajar con grandes conjuntos de datos de forma paralela.

#### Acceso a la memoria y eficiencia energética

La CPU y la GPU acceden a la memoria de forma diferente. **La CPU utiliza una memoria caché más pequeña y de alta velocidad para obtener datos rápidamente**. Esto es útil cuando la CPU necesita acceder muchas veces a pequeñas cantidades de datos, como al ejecutar programas o procesar entradas del usuario.

La GPU utiliza su propia memoria especial llamada **VRAM (memoria de video)**. La VRAM tiene un **ancho de banda muy alto**, lo que significa que puede mover grandes cantidades de datos a la vez, como imágenes y videos. Sin embargo, la GPU consume más energía porque debe procesar muchos datos al mismo tiempo, especialmente al renderizar videos o ejecutar simulaciones complejas.

> [!NOTE]  
> **Renderizado:** el proceso de generar una imagen a partir de un modelo mediante programas informáticos.

### Comparación entre CPU y GPU

| Procesador | Procesamiento | Arquitectura | Funcionalidad |
|------------|---------------|---------------|---------------|
| **CPU** | Es un procesador **de propósito general**, capaz de manejar muchas tareas diferentes. Ejecuta las instrucciones de los programas de ordenador, implicando operaciones como aritmética, lógica y control de operaciones de entrada/salida (E/S), según lo indicado por el sistema operativo. | Las CPU generalmente tienen menos núcleos. Los dispositivos de usuario general suelen tener entre 4 y 8 núcleos; sin embargo, existen algunas CPU avanzadas que ahora tienen 64 núcleos o más. Cada núcleo es muy versátil, lo que le permite manejar cálculos complejos que requieren procesamiento secuencial. | Permite al usuario cambiar entre múltiples tareas y aplicaciones. Esto lo hace ideal para ejecutar el sistema operativo y aplicaciones de software en general. |
| **GPU** | Es un procesador **especializado**, centrado en manejar gráficos, **renderizar** imágenes, video y animaciones. | Compuesto por cientos o miles de núcleos pequeños que son adecuados para tareas que se pueden ejecutar en paralelo. Aunque cada núcleo no es tan potente como uno estándar de la CPU, el alto número de núcleos les permite realizar un gran número de cálculos simultáneamente, lo que los hace perfectos para el procesamiento gráfico. | Adecuado para tareas que requieren el procesamiento simultáneo de grandes bloques de datos, como el renderizado de imágenes, el procesamiento de video y las aplicaciones de *deep learning*. |

> [!IMPORTANT]  
> En resumen, las CPU son mejores para tareas que requieren alta velocidad, toma de decisiones complejas y versatilidad.
Las GPU son mejores cuando la misma operación debe realizarse en muchos datos de forma simultánea.
> 
> Esto significa que, para tareas como los videojuegos, la edición de video y la investigación computacional (IA y aprendizaje automático), las GPU suelen superar significativamente a las CPU.

### Cómo trabajan juntas la CPU y la GPU para aumentar el rendimiento en los videojuegos

Al jugar videojuegos, la CPU y la GPU trabajan juntas para ofrecer una experiencia fluida e inmersiva.

La CPU se encarga de la lógica principal del juego, incluyendo las reglas, los cálculos físicos y el comportamiento de la IA. También procesa las entradas del jugador (determinando los resultados de sus acciones y actualizando el estado del juego en consecuencia).

La GPU tiene como función principal renderizar los elementos visuales del juego. Procesa los datos de **vértices y píxeles para dibujar imágenes en la pantalla**, incluyendo objetos 3D, texturas y efectos como iluminación y sombras.

> [!NOTE]  
> **Datos de vértices y píxeles:** datos que la GPU utiliza para renderizar objetos e imágenes en 3D.
>
> **Frame (fotograma):** una sola imagen dentro de una secuencia que forma un video o animación.

<br>

## A1.1.4. Propósitos de los diferentes tipos de memoria principal

### Tipos de memoria
La memoria principal del ordenador almacena datos e instrucciones que la CPU necesita para procesar tareas. La memoria principal incluye varios tipos: RAM (memoria de acceso aleatorio), ROM (memoria de solo lectura), cachés y registros (tratados en la Sección A1.1.1). Todos estos son tipos de memoria principal, lo que significa que son utilizados directamente por la CPU.

#### RAM
La RAM (memoria de acceso aleatorio) contiene instrucciones y datos de los programas que se están ejecutando en ese momento. Por ejemplo, cuando abres una aplicación en tu teléfono o en tu ordenador, esta se carga en la RAM para que la CPU pueda acceder a ella rápidamente.

La RAM es **volátil**, lo que significa que pierde su contenido cuando se apaga la energía del ordenador. Por eso, cuando estás jugando y no guardas la partida, pierdes tu progreso (ya que el guardado se almacena en la memoria secundaria).

> [!NOTE]  
> **Volátil:** tipo de memoria o almacenamiento que pierde sus datos cuando se apaga la energía.

Un ejemplo real del uso de la RAM se encuentra en los teléfonos inteligentes, que utilizan la RAM para cambiar rápidamente entre aplicaciones. Cuando sales de una aplicación, esta permanece en la RAM, de modo que puedes volver a ella rápidamente sin necesidad de recargarla desde cero.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%206.%20Random%20Access%20Memory%20(RAM).png" alt="RAM" width="450" height="auto"/>
    <p><em>Figura 6: Random Access Memory (RAM). Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

#### ROM

La ROM (read-only memory o memoria de solo lectura) se utiliza para almacenar instrucciones que rara vez se modifican. La ROM se emplea para el **BIOS** (basic input/output system o sistema básico de entrada/salida) del ordenador, que se encuentra en la placa base.

La función principal del BIOS es **inicializar y comprobar los componentes de hardware del sistema durante el arranque**, y **cargar el sistema operativo (OS)** desde el almacenamiento secundario hacia la RAM, dejándolo listo para que la CPU obtenga, decodifique y ejecute las instrucciones.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%207.%20Memoria%20ROM%20de%20la%20placa%20base.png" alt="ROM" width="450" height="auto"/>
    <p><em>Figura 7: Read-Only Memory (ROM). Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

La **ROM** es una memoria **no volátil**, lo que significa que no pierde su contenido cuando el ordenador está apagado. Aunque la ROM es de “solo lectura”, lo que implica que sus datos no pueden modificarse fácilmente, la mayoría de los ordenadores modernos utilizan **memoria flash**, que permite actualizaciones y reprogramación. Esto hace posible que las compañías de placas base actualicen su software cuando sea necesario.

Un ejemplo real del uso de la ROM se encuentra en los teléfonos inteligentes, donde la ROM almacena el sistema operativo y las aplicaciones principales, que no cambian a menos que realices una actualización. Esto garantiza que tu teléfono pueda arrancar de manera confiable en cada encendido.

#### Caché (L1, L2 y L3)

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%208.%20Jerarqu%C3%ADa%20de%20memoria.png" alt="ROM" width="450" height="auto"/>
    <p><em>Figura 8: Memoria Caché. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

La **memoria caché** es pequeña, pero ofrece acceso de alta velocidad a la CPU en comparación con la RAM. Actúa como un búfer entre la CPU y la RAM más lenta, almacenando datos e instrucciones de uso frecuente.

Existen tres tipos de caché: **L1, L2 y L3**, cada una con diferentes tamaños y velocidades. Cuanto más cerca de la CPU se encuentre, más rápida es.

- **Caché L1**: se encuentra directamente en la CPU, lo que la convierte en la más rápida. Puede accederse a ella casi al instante debido a su ubicación. Sin embargo, también es la más pequeña, normalmente de solo unos pocos kilobytes (32KB a 128KB por núcleo). Cada núcleo de CPU suele tener su propia caché L1, que normalmente se divide en dos secciones: **L1i** para almacenar instrucciones y **L1d** para almacenar datos.
- **Caché L2**: puede estar en la CPU, como la L1, o situada muy cerca de ella. La caché L2 es más grande que la L1 y puede tener hasta varios megabytes de tamaño (256KB a 2MB por núcleo), proporcionando más espacio para almacenar instrucciones de uso frecuente. Es más rápida que la L3, pero un poco más lenta que la L1, aunque sigue acelerando significativamente el procesamiento al reducir la necesidad de acceder a la RAM más lenta.
- **Caché L3**: suele encontrarse más alejada del chip de la CPU. La caché L3 puede ser compartida entre varios núcleos en las CPU multinúcleo, mientras que L1 y L2 suelen ser exclusivas de un solo núcleo. Es la más grande de las tres y puede alcanzar decenas de megabytes (2MB a 64MB compartidos entre todos los núcleos). Es la más lenta de los tres tipos de caché, pero aún así es mucho más rápida que la RAM.

Los términos **acierto de caché (cache hit) y fallo de caché (cache miss)** se utilizan para describir la eficiencia de la memoria caché de la CPU al recuperar datos.

- Un **acierto de caché** es el escenario ideal: la CPU solicita datos y estos se encuentran en la memoria caché.
- Un **fallo de caché** significa que no se encontraron, lo que obliga a recuperarlos desde la memoria principal (RAM) más lenta o incluso desde un almacenamiento todavía más lento (SSD / HDD).

> [!TIP]
> Imagina una cebolla, con sus capas representando los niveles de caché:
>
> La **caché L1** es la más pequeña y rápida, como el centro mismo de la cebolla, donde todo está muy compacto y más cerca del núcleo de la CPU.
>
> La **caché L2** es un poco más grande y más lenta, como la siguiente capa hacia afuera: todavía cerca del centro, pero no tan rápida de acceder como el núcleo.
> 
> La **caché L3** es la más grande y lenta, como las capas exteriores de la cebolla. Sigue siendo importante, pero se tarda un poco más en llegar a ella, de la misma forma que la CPU necesita más tiempo para acceder a los datos en la caché L3 en comparación con L1 y L2.

#### Optimización del rendimiento de la CPU con caché

La caché desempeña un papel fundamental para garantizar que la CPU pueda acceder a los datos lo más rápido posible. Cuando la CPU encuentra los datos buscados en la caché (**acierto de caché**), estos pueden procesarse muy rápidamente. Sin embargo, cuando ocurre un **fallo de caché**, la CPU debe buscar los datos en la memoria más lenta, lo que provoca un retraso.

Imagina que estás jugando a un videojuego en un ordenador. La CPU revisa con frecuencia las cachés L1, L2 y L3 para encontrar los datos que necesita para que el juego funcione sin problemas. Las funciones principales del juego, como los controles del jugador y la lógica del juego, podrían almacenarse en la caché L1, mientras que los datos a los que se accede con menos frecuencia, como las texturas de fondo, pueden estar en la caché L3.

Este sistema por capas ayuda a garantizar que el juego se ejecute de forma fluida, sin interrupciones. Una CPU con una caché más grande o con técnicas de **prefetching** más avanzadas (una técnica mediante la cual la CPU predice qué datos necesitará y los carga en la caché por adelantado) tendrá menos fallos de caché y un mejor rendimiento general.

<br>

## A1.1.5. Ciclo de búsqueda, decodificación y ejecución

El ciclo de búsqueda–decodificación–ejecución, también conocido como “ciclo de instrucción”, es el proceso fundamental que utiliza una CPU para ejecutar instrucciones. El ciclo consta de tres etapas principales:

- **Búsqueda (Fetch):** la CPU obtiene una instrucción de la memoria.
- **Decodificación (Decode):** la CPU interpreta la instrucción y prepara las operaciones necesarias para ejecutarla.
- **Ejecución (Execute):** la CPU realiza las acciones requeridas por la instrucción.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%209.%20The%20fetch-decode-execute%20cycle.png" alt="ROM" width="250" height="auto"/>
    <p><em>Figura 10: The fetch-decode-execute cycle. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

### Little Man Computer (LMC)

Una forma más sencilla de ver estas etapas con más detalle es utilizar un modelo educativo de CPU conocido como **Little Man Computer**, que puedes buscar en línea o usar en este enlace: [https://peterhigginson.co.uk/lmc](https://peterhigginson.co.uk/lmc).  

Este modelo utiliza **lenguaje ensamblador**, un conjunto simple de instrucciones, cada una representada por tres letras, que se almacena como un código de tres dígitos en la memoria.  

#### Conjunto de instrucciones

| Instrucción | Código | Descripción |
|-------------|--------|-------------|
| **INP** | 901 | Introduce un valor y lo almacena en el acumulador. |
| **OUT** | 902 | Muestra el valor del acumulador. |
| **DAT** | N/A | Define valores de datos directamente en memoria en el punto de declaración, a menudo usados para constantes o variables. |
| **LDA** | 5XX | Carga en el acumulador el valor de la dirección de memoria especificada. |
| **STA** | 3XX | Almacena el valor del acumulador en la dirección de memoria especificada. |
| **ADD** | 1XX | Suma al acumulador el valor de la dirección de memoria especificada. |
| **SUB** | 2XX | Resta al acumulador el valor de la dirección de memoria especificada. |
| **HLT** | 000 | Detiene el programa. |
| **BRA** | 6XX | Salta a la dirección de memoria especificada. |
| **BRZ** | 7XX | Salta a la dirección de memoria especificada si el acumulador es cero. |
| **BRP** | 8XX | Salta a la dirección de memoria especificada si el acumulador es positivo. |

---

#### Ejemplo
Introduce el siguiente programa en la columna de la izquierda y ensámblalo en la RAM.  
Verás la representación de **tres dígitos** para cada instrucción almacenada en una dirección de memoria en la columna de la derecha.  

Por ejemplo:  
`LDA 4` se almacena como **504** en la dirección de memoria **0**.

```
LDA 4
ADD 5
STA 5
HLT
DAT 23
DAT 12
```

LMC se debe ver tal que así:

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2010.%20LMC%20Model.png" alt="LMC" width="750" height="auto"/>
    <p><em>Figura 11: LMC Model. Fuente: Peter Higginson</em></p>
  </div>

#### Primer ciclo (Click step)

1. **Búsqueda (Fetch):** El PC (contador de programa) está actualmente en 0, así que se recupera la instrucción en la dirección de memoria 0 (504) abriendo la dirección 0 en la RAM mediante el bus de direcciones y obteniendo la instrucción a través del bus de datos. El bus de control envía una señal de lectura para iniciar este proceso. El valor 5 se almacena en el registro de instrucciones y 04 en el registro de direcciones. Mientras esto sucede, el PC se incrementa a 1 mediante la ALU, preparándose para la siguiente instrucción.

2. **Decodificación (Decode):** Una vez recuperada la instrucción, la CPU la decodifica. La unidad de control utiliza el bus de control para coordinar este proceso. La instrucción almacenada en el registro de instrucciones es 5, que se decodifica como “cargar en el acumulador”. El registro de direcciones 04 indica la dirección de los datos que deben cargarse.

3. **Ejecución (Execute):** Se lleva a cabo la orden. La dirección 4 se abre en el bus de direcciones y el bus de control envía las señales apropiadas para recuperar los datos (23) de esa ubicación a través del bus de datos y almacenarlos en el acumulador.

#### Segundo ciclo (Click step)

1. **Búsqueda (Fetch):** La CPU usa ahora el PC para saber qué instrucción recuperar a continuación: el valor actual es 1. Se abre la dirección 1 y se obtiene la instrucción 105. El bus de control envía una señal de lectura para iniciar este proceso. El valor 1 se almacena en el registro de instrucciones y 05 en el registro de direcciones. El PC se incrementa a 2 mediante la ALU.

2. **Decodificación (Decode):** La instrucción 1 se decodifica como “sumar al acumulador”; el registro de direcciones indica la dirección de los datos que deben sumarse (5). La unidad de control utiliza el bus de control para coordinar este proceso.

3. **Ejecución (Execute):** Se abre la dirección 5, se recuperan los datos (12) y tanto el acumulador (que contiene 23) como los datos recuperados (12) se envían a la ALU. El resultado de 23 + 12 se almacena en el acumulador (35).

#### Tercer ciclo (Click step)

1. **Búsqueda (Fetch):** El PC está actualmente en 2, así que se recupera la instrucción en la dirección de memoria 2 (305). El bus de control envía una señal de lectura para iniciar este proceso. El valor 3 se almacena en el registro de instrucciones y 05 en el registro de direcciones. El PC se incrementa a 3 mediante la ALU.

2. **Decodificación (Decode):** La instrucción 3 se decodifica como “almacenar acumulador en dirección” y el registro de direcciones indica la ubicación donde guardar los datos (05). La unidad de control usa el bus de control para coordinar esto.

3. **Ejecución (Execute):** Se abre la dirección 5 mediante el bus de direcciones, y el bus de control envía las señales adecuadas para enviar el contenido del acumulador por el bus de datos y almacenarlo en la dirección 5 (sobrescribiendo los datos actuales).

#### Cuarto ciclo (Click step)

1. Búsqueda (Fetch): El PC está actualmente en 3, por lo que se recupera la instrucción en la dirección de memoria 3 (000). El bus de control envía una señal de lectura para iniciar este proceso. El valor 0 se almacena en el registro de instrucciones y 00 en el registro de direcciones. El PC se incrementa a 4 mediante la ALU.

2. Decodificación (Decode): La instrucción 0 se decodifica como “detener”. La unidad de control utiliza el bus de control para señalar esta operación.

3. Ejecución (Execute): El ordenador detiene todas las operaciones y finaliza el programa.

<br>

## A1.1.6. Tipos externos e internos de memoria secundaria

### Almacenamiento interno

#### Hard disk drive (HDD) y solid state drive (SSD)

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2011.%20Interior%20de%20una%20HDD%20y%20una%20SSD.png" alt="HDD y SSD" width="750" height="auto"/>
    <p><em>Figura 11: Interior de una HDD y una SSD. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Las **unidades de disco duro (HDD)** y las **unidades de estado sólido (SSD)** son las soluciones de almacenamiento más habituales en los ordenadores personales. Los HDD son una tecnología más antigua, pero todavía se utilizan con frecuencia, especialmente en dispositivos no portátiles, ya que resultan relativamente baratos en comparación con la capacidad de almacenamiento que ofrecen. Los HDD utilizan un disco magnético giratorio para leer y escribir datos. Son adecuados para almacenar grandes volúmenes de información, como archivos multimedia, copias de seguridad y documentos, en los que la velocidad no es un factor tan crítico.

Los SSD no tienen partes móviles. Utilizan memoria flash para almacenar datos, lo que proporciona un acceso de alta velocidad y mayor durabilidad. Esto los hace muy populares en dispositivos portátiles como portátiles y tabletas. Son ideales para sistemas operativos, aplicaciones de software y videojuegos debido a su alta velocidad de lectura y escritura, lo que mejora el rendimiento general del sistema.

| Característica       | HDD (disco duro)                                       | SSD (unidad de estado sólido)                  |
|-----------------------|-------------------------------------------------------|-----------------------------------------------|
| Tecnología de almacenamiento | Almacenamiento magnético con discos giratorios y cabezales de lectura/escritura | Memoria flash sin partes móviles               |
| Velocidad             | Velocidades de lectura/escritura más lentas (generalmente 50–150 MB/s) | Velocidades de lectura/escritura más rápidas (generalmente 200–500 MB/s) |
| Durabilidad           | Más propenso a daños físicos debido a las partes móviles | Más duradero; resistente a golpes físicos      |
| Ruido                 | Produce ruido debido a las partes móviles              | Funcionamiento silencioso                      |
| Consumo de energía    | Mayor consumo de energía debido a las partes mecánicas | Menor consumo de energía                       |
| Coste                 | Generalmente más barato por GB                         | Más caro por GB                                |
| Capacidad             | Disponible en mayores capacidades (hasta varios TB)   | Generalmente disponible en capacidades menores (hasta varios TB, pero a mayor coste) |
| Peso                  | Más pesado debido a los componentes mecánicos         | Más ligero                                     |
| Generación de calor   | Genera más calor debido a las partes móviles           | Genera menos calor                             |

Existe otra forma de unidad SSD que actualmente es muy popular y ofrece varias ventajas. Los SSD M.2 tienen el aspecto de una barra de chicle. Son muy pequeños y delgados, y ocupan mucho menos espacio que un SSD estándar. Los **SSD M.2 NVMe** también son más rápidos que los SSD SATA de 2,5” y se consideran más fáciles de instalar: simplemente se insertan en la placa base y se fijan con un solo tornillo.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2012.%20M2%20SSD.png" alt="M2 SSD" width="550" height="auto"/>
    <p><em>Figura 12: M.2 SSD. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

#### eMMC (Embedded MultiMediaCard)

En dispositivos de bajo coste, como teléfonos inteligentes de gama básica y portátiles económicos, donde no son esenciales todas las ventajas de los SSD, las eMMC son una opción popular. También son un tipo de almacenamiento flash que utiliza memoria flash NAND. Están soldadas directamente a la placa base del dispositivo. Aunque su capacidad y velocidad no igualan a las de un SSD estándar, su rendimiento es adecuado para las necesidades informáticas básicas y aplicaciones sencillas.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2013.%20eMMC.jpg" alt="M2 SSD" width="250" height="auto"/>
    <p><em>Figura 13: eMMC. Fuente: Kingston</em></p>
  </div>

### Almacenamiento externo

#### Hard disk drive (HDD) y solid state drive (SSD)

Como soluciones de almacenamiento externo, tanto los HDD como los SSD son opciones populares. Su rendimiento y comparación son idénticos a los de las versiones internas. El uso de uno u otro depende de los requisitos del usuario. Si necesitas transferencias rápidas de archivos, copias de seguridad y una solución portátil que sea menos propensa a sufrir daños al transportarse, los SSD son la mejor elección. Si lo que necesitas son copias de seguridad extensas, almacenar archivos multimedia o transportar archivos grandes, pero la velocidad no es tan crítica, puedes optar por un HDD como mejor alternativa.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2014.%20HDD%20externo.jpg" alt="HDD externo" width="350" height="auto"/>
    <p><em>Figura 14: HDD externo. Fuente: La Vanguardia</em></p>
  </div>

#### Discos ópticos y unidades ópticas

De izquierda a derecha: CD, DVD y Blu-Ray

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2015.%20CD%2C%20DVD%20y%20Blu-Ray.png" alt="Discos ópticos" width="550" height="auto"/>
    <p><em>Figura 15: De izquierda a derecha: CD, DVD y Blu-Ray. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Las unidades ópticas que leen/escriben discos ópticos, como los CD, DVD o Blu-Ray, están perdiendo popularidad, pero todavía se consideran una opción para el almacenamiento externo de datos. El coste de un disco óptico es bajo en comparación con un HDD o un SSD y, aunque sus velocidades de lectura/escritura pueden ser más lentas, son suficientes para el archivado de datos y la reproducción. Sin embargo, los discos son propensos a rayarse, especialmente si no se almacenan correctamente, y requieren una unidad óptica para leerlos o grabarlos, algo cada vez menos común en los dispositivos actuales.

#### Tarjetas de memoria

Las tarjetas de memoria son dispositivos de almacenamiento compactos que se utilizan con frecuencia en cámaras, teléfonos inteligentes y otros dispositivos portátiles. Son ideales para ampliar la capacidad de almacenamiento en dispositivos móviles y para guardar fotos y vídeos en cámaras, ya que utilizan memoria flash NAND. Existen en múltiples formatos, como SD, microSD y CompactFlash, adaptándose a diferentes dispositivos y necesidades de espacio. Se caracterizan por su durabilidad: son resistentes a golpes físicos, temperaturas extremas y al agua, lo que las hace perfectas para dispositivos portátiles. Sus tiempos de lectura/escritura suelen ser más lentos que los de los SSD, pero superan a los de los discos ópticos.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2016.%20Tarjetas%20de%20memoria.jpg" alt="HDD externo" width="350" height="auto"/>
    <p><em>Figura 16: Tarjetas de memoria. Fuente: JetComputer</em></p>
  </div>

#### Network Attached Storage (NAS)

El NAS es un sistema de almacenamiento de archivos dedicado, conectado a una red, que permite a múltiples usuarios acceder a los datos. Se utiliza a menudo en hogares o empresas para centralizar el almacenamiento de datos, el guardado de archivos y las copias de seguridad.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2017.%20NAS.jpg" alt="HDD externo" width="450" height="auto"/>
    <p><em>Figura 17: NAS. Fuente: MuyComputer</em></p>
  </div>

Un NAS normalmente está compuesto por múltiples HDD o SSD configurados en **RAID (Redundant Array of Independent Disks, Conjunto Redundante de Discos Independientes)**. Suele conectarse a la red mediante Ethernet y ejecuta un sistema operativo ligero diseñado para el almacenamiento, la gestión y el intercambio de archivos.

Al utilizar múltiples HDD o SSD, su capacidad suele ser alta, y es posible ampliar el sistema añadiendo más unidades.

> [!NOTE]  
> **RAID (Redundant Array of Independent Disks):** es una tecnología de almacenamiento de datos que combina múltiples discos físicos en una única unidad lógica para mejorar el rendimiento, proporcionar redundancia y garantizar la protección de los datos.

<br>

## A1.1.7. Concepto de compresión
