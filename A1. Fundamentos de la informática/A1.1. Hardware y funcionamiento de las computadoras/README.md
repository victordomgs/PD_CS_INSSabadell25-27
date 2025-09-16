<h1 align="center">A1.1. Hardware y funcionamiento de las computadoras
<div align="center">

</div>

## Contenido:

- [A1.1.1. Funciones e interacciones de los principales componentes de la CPU](#111-funciones-e-interacciones-de-los-principales-componentes-de-la-CPU)  
- [A1.1.2. Función de una GPU](#112-función-de-una-GPU)
- [A1.1.3. Diferencia entre CPU y GPU](#113-diferencia-entre-CPU-y-GPU)
- [A1.1.4. Finalidad de la memoria primaria](#114-finalidad-de-la-memoria-primaria) 
- [A1.1.5. Ciclo de búsqueda, decodificación y ejecución](#115-ciclo-de-búsqueda-decodificación-y-ejecución) 
- [A1.1.6. Tipos externos e internos de memoria secundaria](#116-tipos-externos-e-internos-de-memoria-secundaria)
- [A1.1.7. Concepto de compresión](#117-concepto-de-compresión)
- [A1.1.8. Servicios de computación en la nube](#118-servicios-de-computación-en-la-nube)

## A1.1.1. Funciones e interacciones de los principales componentes de la CPU

### ¿Qué es la unidad central de procesamiento?
La unidad central de procesamiento (CPU) a menudo se refiere como el “cerebro” del ordenador. Es un componente crítico que lleva a cabo la mayor parte del procesamiento dentro de un dispositivo.

La CPU está compuesta por dos unidades principales: la unidad de control (CU) y la unidad aritmético-lógica (ALU).

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%201.%20Modelo%20de%20CPU.png" alt="CPU Model" width="450" height="auto"/>
    <p><em>Figura 1: Modelo de CPU. Fuente: Paul Baumgarten, Ioana Ganea, Carl Turland</em></p>
  </div>

#### Unidad de control (CU)
La unidad de control dirige las operaciones del procesador. Es responsable del ciclo de captación–decodificación–ejecución, gestionando las tres operaciones y dirigiendo la memoria del ordenador, la ALU y los dispositivos de entrada/salida para que respondan de manera adecuada.

#### Unidad aritmético-lógica (ALU)
Esta unidad es responsable de realizar operaciones aritméticas y lógicas. Estas incluyen operaciones aritméticas básicas como la suma, resta, multiplicación y división, así como operaciones lógicas incluyendo AND, OR, XOR y NOT.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%202.%20Central%20processing%20unit%20(CPU).jpg" alt="Switch Hub" width="350" height="auto"/>
    <p><em>Figura 2: Central Processing Unit. Fuente: PcCompomentes</em></p>
  </div>

###  ¿Qué son los registros?
Los registros son cantidades muy pequeñas de almacenamiento que están disponibles directamente en la CPU para mantener datos temporales con los que la CPU puede estar trabajando. Los registros son el registro de instrucciones (IR), el contador de programa (PC), el registro de direcciones de memoria (MAR), el registro de datos de memoria (MDR) y el acumulador (AC).

#### Registro de instrucciones
Cuando una instrucción es captada desde la memoria, se mantiene en el IR dentro de la CPU. Este registro contiene la instrucción que está siendo ejecutada actualmente por la CPU.

#### Contador de programa
El PC contiene la dirección de la siguiente instrucción que debe ser captada desde la memoria. Una vez que la instrucción ha sido captada, el PC se actualiza para apuntar a la siguiente instrucción que será necesaria.

#### Registro de direcciones de memoria
El MAR contiene la dirección de memoria que está siendo captada actualmente. El contenido del PC se copia en el MAR, y el MAR proporciona esta dirección a la unidad de memoria, de modo que los datos e instrucciones puedan ser leídos desde o copiados a esa ubicación.

#### Registro de datos de memoria
Este contiene los datos que han sido captados o que están a punto de ser escritos en la dirección de memoria que está actualmente en el MAR.

#### Acumulador (AC)
Este almacena los resultados aritméticos o lógicos intermedios producidos por la ALU.

## ¿Qué son los buses?
Los buses son un componente crítico del sistema informático, ya que transfieren datos entre varios dispositivos, incluyendo la CPU, la memoria, el almacenamiento y los periféricos. Los buses tienen anchos que se miden en bits. Cuanto mayor es el ancho del bus, más datos puede transmitir a la vez.
Existen tres tipos principales de buses: bus de control, bus de datos y bus de direcciones.

### Bus de control
El bus de control se utiliza para transmitir señales de comando y de control desde la CPU a otros componentes del sistema, y viceversa. Debido a la necesidad de que las señales sean enviadas y recibidas, este bus es bidireccional. Algunas de las señales que se transmitirían a través del bus de control son operaciones de lectura/escritura, peticiones de interrupción, señales de reloj para sincronización y señales de estado de los componentes de hardware.

### Bus de datos
El bus de datos transporta los datos que están siendo procesados entre la CPU, la memoria y otros periféricos. El ancho del bus de datos es importante para determinar la cantidad de datos que puede transferir a la vez. Los anchos comunes de los buses de datos son 8, 16, 32 y 64 bits. Como los datos necesitan ser leídos y escritos en la memoria, los buses de datos suelen ser bidireccionales.

### Bus de direcciones
El bus de direcciones se utiliza para transmitir la dirección que debe ser leída o escrita en la memoria. El ancho de este bus determina la capacidad de memoria del sistema. Por ejemplo, un bus de direcciones de 32 bits puede direccionar $2^{32}$ ubicaciones de memoria.
