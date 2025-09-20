<h1 align="center">A1.1. Hardware y funcionamiento de las computadoras
<div align="center">

</div>

## Contenido:

- [A1.1.1. Funciones e interacciones de los principales componentes de la CPU](#A111-funciones-e-interacciones-de-los-principales-componentes-de-la-CPU)  
- [A1.1.2. Función de una GPU](#A112-función-de-una-GPU)
- [A1.1.3. Diferencia entre CPU y GPU](#A113-diferencia-entre-CPU-y-GPU)
- [A1.1.4. Finalidad de la memoria primaria](#A114-finalidad-de-la-memoria-primaria) 
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
    <p><em>Figura 1: Modelo de CPU. Fuente: Paul Baumgarten, Ioana Ganea, Carl Turland</em></p>
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
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%203.%20Graphic%20processing%20unit%20(GPU).jpg" alt="GPU" width="350" height="auto"/>
    <p><em>Figura 3: Graphic Processing Unit. Fuente: PcCompomentes</em></p>
  </div>

### Procesamiento gráfico

Las **GPU** están diseñadas con una estructura altamente paralela, lo que les permite realizar muchos cálculos simultáneamente. Esto las hace excepcionalmente adecuadas para renderizar los gráficos complejos e intensivos en recursos que se ven en los videojuegos y aplicaciones modernas.

También manejan la aplicación de **shaders y textures a modelos 3D**, lo que incluye iluminación, sombreado y mapeado de texturas, mejorando el realismo de la escena.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%204.%20Gr%C3%A1ficos%20de%20videojuegos.jpg" alt="GPU" width="450" height="auto"/>
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
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%205.%20Bitcoin.jpg" alt="Bitcoin" width="450" height="auto"/>
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

# Comparación entre CPU y GPU

| Procesador | Procesamiento | Arquitectura | Funcionalidad |
|------------|---------------|---------------|---------------|
| **CPU** | Es un procesador **de propósito general**, capaz de manejar muchas tareas diferentes. Ejecuta las instrucciones de los programas de ordenador, implicando operaciones como aritmética, lógica y control de operaciones de entrada/salida (E/S), según lo indicado por el sistema operativo. | Las CPU generalmente tienen menos núcleos. Los dispositivos de usuario general suelen tener entre 4 y 8 núcleos; sin embargo, existen algunas CPU avanzadas que ahora tienen 64 núcleos o más. Cada núcleo es muy versátil, lo que le permite manejar cálculos complejos que requieren procesamiento secuencial. | Permite al usuario cambiar entre múltiples tareas y aplicaciones. Esto lo hace ideal para ejecutar el sistema operativo y aplicaciones de software en general. |
| **GPU** | Es un procesador **especializado**, centrado en manejar gráficos, **renderizar** imágenes, video y animaciones. | Compuesto por cientos o miles de núcleos pequeños que son adecuados para tareas que se pueden ejecutar en paralelo. Aunque cada núcleo no es tan potente como uno estándar de la CPU, el alto número de núcleos les permite realizar un gran número de cálculos simultáneamente, lo que los hace perfectos para el procesamiento gráfico. | Adecuado para tareas que requieren el procesamiento simultáneo de grandes bloques de datos, como el renderizado de imágenes, el procesamiento de video y las aplicaciones de *deep learning*. |

> [!IMPORTANT]  
> En resumen, las CPU son mejores para tareas que requieren alta velocidad, toma de decisiones complejas y versatilidad.
Las GPU son mejores cuando la misma operación debe realizarse en muchos datos de forma simultánea.
> Esto significa que, para tareas como los videojuegos, la edición de video y la investigación computacional (IA y aprendizaje automático), las GPU suelen superar significativamente a las CPU.
