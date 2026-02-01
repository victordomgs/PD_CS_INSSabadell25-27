# A1. Fundamentos de la informática

Nivel Medio: 11 horas. Nivel Superior: 18 horas.

## Pregunta de orientación
¿Qué principios sustentan el funcionamiento de una computadora, desde la funcionalidad de bajo nivel del hardware hasta las interacciones del sistema operativo?

## A1.1 Hardware y funcionamiento de las computadoras

### A1.1.1 Describir las funciones e interacciones de los principales componentes de la CPU

- Unidades: unidad lógica aritmética (ALU), unidad de control
- Registros: registro de instrucciones, contador de programa, registro de direcciones de memoria, registro de datos de memoria, acumulador
- Buses: dirección, datos, control
- Procesadores: procesador de núcleo único, procesador multinúcleo, coprocesadores
- Una representación diagramática de la relación entre los componentes especificados de la CPU

### A1.1.2 Describir la función de una GPU

- Arquitectura que permite a las unidades de procesamiento gráfico (GPU) manejar tareas específicas y las hace adecuadas para cálculos complejos.
- Las situaciones del mundo real pueden incluir videojuegos, inteligencia artificial (IA), simulaciones a gran escala y otras aplicaciones que requieren renderizado de gráficos y aprendizaje automático.

### A1.1.3 Explicar las diferencias entre la CPU y la GPU (solo NS)

- Diferencias en las filosofías de su diseño y situaciones de uso
- Diferencias en su arquitectura central, potencia de procesamiento, acceso a la memoria y eficiencia energética
- Colaboración entre la CPU y la GPU: división de tareas, compartición de datos y coordinación de la ejecución

### A1.1.4 Explicar la finalidad de los distintos tipos de memoria primaria

- Memoria de acceso aleatorio (RAM), memoria de solo lectura (ROM), caché (L1, L2, L3) y registros
- Interacción de la CPU con diferentes tipos de memoria para optimizar el rendimiento
- Pertinencia de los términos “fallo de caché” y “acierto de caché”

### A1.1.5 Describir el ciclo de búsqueda, decodificación y ejecución

- Operaciones básicas que realiza una CPU para ejecutar una única instrucción en lenguaje máquina
- Interacción entre la memoria y los registros a través de los tres buses: dirección, datos, control

### A1.1.7 Describir los tipos internos y externos de almacenamiento de memoria secundaria

- Discos duros internos: unidad de estado sólido, unidad de disco duro, tarjetas multimedia integradas
- Discos duros externos: unidades de estado sólido, unidades de disco duro, unidades ópticas, unidades flash, tarjetas de memoria, almacenamiento conectado a la red
- Situaciones en las que se utilizan los distintos tipos de unidades de almacenamiento

### A1.1.8 Describir el concepto de compresión

- Diferencias entre los métodos de compresión con y sin pérdidas
- Codificación RLE (run-length encoding), codificación de transformación

### A1.1.9 Describir los distintos tipos de servicios de computación en nube

- Servicios: software como servicio (SaaS), plataforma como servicio (PaaS), infraestructura como servicio (IaaS)
- Diferencias entre los enfoques de SaaS, PaaS e IaaS en distintas situaciones del mundo real, reconociendo que los diferentes grados de control y flexibilidad influyen en la gestión y la disponibilidad de los recursos

<br>

## A1.2 Representación de datos y lógica computacional

### A1.2.1 Describir los principales métodos de representación de datos

- Representación de números enteros en binario y hexadecimal
- Conversión de enteros binarios y hexadecimales a decimales, y viceversa
- Conversión de enteros de binario a hexadecimal y viceversa

### A1.2.2 Explicar cómo se utiliza el binario para almacenar datos

- Fundamentos de la codificación binaria y su impacto en el almacenamiento y la recuperación de datos
- Mecanismos mediante los cuales se almacenan en forma binaria datos como números enteros, cadenas, caracteres, imágenes, audio y video

### A1.2.3 Describir la finalidad y el uso de las puertas lógicas

- Finalidad y uso de las puertas lógicas
- Funciones y aplicaciones de las puertas lógicas en los sistemas informáticos
- Función de las puertas lógicas en la computación binaria
- Operadores booleanos: AND, OR, NOT, NAND, NOR, XOR, XNOR

### A1.2.4 Elaborar y analizar tablas de verdad

- Tablas de verdad para predecir la salida de circuitos lógicos sencillos
- Tablas de verdad para determinar las salidas a partir de las entradas en la descripción de un problema
- Tablas de verdad y su relación con una expresión booleana, con entradas y salidas
- Tablas de verdad derivadas de diagramas lógicos para ayudar a la simplificación de expresiones lógicas
- Mapas de Karnaugh y simplificación algebraica para simplificar las expresiones de salida

### A.1.2.5 Elaborar diagramas lógicos

- Diagramas lógicos para demostrar cómo se conectan e interactúan las puertas lógicas en un circuito
- Uso de símbolos de compuerta estándar para las compuertas AND, OR, NOT, NAND, NOR, XOR y XNOR
- Entradas procesadas diagramáticamente para producir salidas
- Combinaciones de estas compuertas para realizar operaciones lógicas más complejas
- Reglas de álgebra booleana para simplificar diagramas lógicos complejos y expresiones complejas

<br>

## A1.3 Sistemas operativos y de control

### A1.3.1 Describir la función de los sistemas operativos

- Los sistemas operativos abstraen las complejidades del hardware para gestionar los recursos del sistema

### A1.3.2 Describir las funciones de un sistema operativo

- Mantener la integridad del sistema mientras se ejecutan las operaciones en segundo plano de los sistemas operativos
- Gestión de memoria, sistema de archivos, gestión de dispositivos, programación, seguridad, contabilidad, interfaz gráfica de usuario (GUI), virtualización, redes

### A1.3.3 Comparar distintos enfoques de la programación
- Gestión de la ejecución de procesos mediante la asignación de tiempo de CPU para optimizar el rendimiento del sistema
- Por orden de llegada, round robin, programación de colas multinivel y programación prioritaria

### A1.3.4 Evaluar el uso del sondeo y el manejo de interrupciones
- Frecuencia de los eventos, sobrecarga de procesamiento de la CPU, fuentes de alimentación (batería o red eléctrica), previsibilidad de los eventos, latencia controlada y problemas de seguridad
- Las situaciones del mundo real pueden incluir entradas de teclado y mouse, comunicaciones de red, operaciones de entrada/salida de disco, sistemas integrados y sistemas de tiempo real
