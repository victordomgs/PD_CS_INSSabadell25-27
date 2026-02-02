<h1 align="center">A2.3. Transmisiones de datos
<div align="center">

</div>

## Contenido:

- [A2.3.1 Describir los diferentes tipos de direccionamiento IP](#A231-describir-los-diferentes-tipos-de-direccionamiento-IP)  
- [A2.3.2 Comparar los tipos de medios para la transmisión de datos](#A232-comparar-los-tipos-de-medios-para-la-transmisión-de-datos)
- [A2.3.3 Explicar cómo se utiliza la conmutación de paquetes para enviar datos a través de una red](#A233-explicar-cómo-se-utiliza-la-conmutación-de-paquetes-para-enviar-datos-a-través-de-una-red)

<br>

## A2.3.1 Describir los diferentes tipos de direccionamiento IP

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2018.jpg" alt="Redes" width="650" height="auto"/>
    <p><em>Figura 18: Estructura IP version 4. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

La **diferencia clave entre la versión 4 y la versión 6 del protocolo IP** es el tamaño del espacio de direcciones. IPv6 fue diseñado para hacer frente al problema, largamente anticipado, del agotamiento de direcciones IPv4.

- **Dirección IP:** un conjunto de números que identifica de forma única a cada computadora según el Protocolo de Internet (ya sea versión 4 o versión 6).

IPv4 utiliza una dirección de cuatro bytes o 32 bits, por lo que normalmente se muestra como cuatro números separados por puntos, donde cada número está dentro del rango de un byte (0–255), por ejemplo 192.168.0.1. Dado que existen 2³² direcciones posibles con este formato, IPv4 está limitado aproximadamente a 4.300.000.000 de nodos en la red.

IPv6, por otro lado, utiliza 16 bytes o 128 bits para sus direcciones. Estas direcciones suelen mostrarse como ocho grupos de cuatro bytes escritos en formato hexadecimal, como por ejemplo:

`2001:0db8:85a3:0000:0000:8a2e:0370:7334`

Disponer de 2¹²⁸ direcciones equivale a una capacidad para unos impresionantes 340.282.370.000.000.000.000.000.000.000.000.000.000 nodos.

### Direcciones públicas y privadas

La diferencia clave entre las direcciones públicas y privadas es su visibilidad en Internet público.

Las direcciones IP que se utilizan en Internet público deben ser globalmente únicas. Normalmente se asignan a sitios web, servidores accesibles desde el exterior y routers que se conectan a Internet. La asignación de estas direcciones públicas está gestionada por ICANN (Internet Corporation for Assigned Names and Numbers).

Las direcciones IP privadas utilizadas dentro de una red privada no son directamente enrutables en Internet global. Se usan habitualmente en redes domésticas y corporativas para dispositivos como ordenadores, tabletas y servidores internos. El tráfico de estos dispositivos debe convertirse en una dirección pública mediante el router para poder acceder a Internet.

ICANN ha reservado determinados rangos de direcciones como privadas y no enrutables para que las organizaciones los utilicen en sus redes internas. Estos rangos son:

- 10.0.0.0 a 10.255.255.255
- 172.16.0.0 a 172.31.255.255
- 192.168.0.0 a 192.168.255.255
- En IPv6: FC00:0000:0000:0000:0000:0000:0000:0000 a FDFF:FFFF:FFFF:FFFF:FFFF:FFFF:FFFF:FFFF

### Direcciones estáticas y dinámicas

Las **direcciones IP estáticas** son aquellas que se asignan de forma permanente a un dispositivo. El dispositivo utiliza la misma dirección IP cada vez que se conecta a la red. Las direcciones IP estáticas son esenciales para los servidores, ya que permiten que los dispositivos cliente sepan dónde localizarlos dentro de la red.

Por el contrario, una dirección IP dinámica es aquella que se asigna a un dispositivo cuando se conecta a la red. Este proceso está gestionado por un servidor DHCP, que asigna a los dispositivos que se conectan una dirección procedente de un conjunto predeterminado de direcciones disponibles. Las direcciones dinámicas ayudan a reducir costes y a utilizar de forma más eficiente un número limitado de direcciones IP en entornos donde los dispositivos se conectan y desconectan con frecuencia.

### Traducción de direcciones de red (NAT)

> [!TIP]
> Asegúrate de comprender y reconocer el papel de la traducción de direcciones de red (NAT). Su capacidad para permitir que múltiples dispositivos de una red privada compartan una única dirección IP para las comunicaciones con Internet ha mantenido a Internet como un sistema viable y funcional. No se puede exagerar la importancia de su papel en la conservación del espacio global de direcciones IP.
> **Traducción de direcciones de red (NAT):** modifica las direcciones IP de los paquetes de datos a medida que pasan por un router o cortafuegos; esto ayuda a mejorar la seguridad y a gestionar el número limitado de direcciones IP disponibles en IPv4, permitiendo que múltiples dispositivos compartan una sola dirección IP pública.

La traducción de direcciones de red es un proceso mediante el cual las redes convierten direcciones IP privadas en direcciones IP públicas y viceversa. Este proceso permite que múltiples dispositivos dentro de una red compartan una única dirección IP pública.

NAT ha sido fundamental para el funcionamiento eficaz de Internet, ya que sigue dependiendo en gran medida de direcciones IPv4, las cuales están prácticamente agotadas. También ayuda a proporcionar una capa adicional de seguridad para redes domésticas y de pequeñas oficinas al ocultar las direcciones IP internas frente a la red externa.

## A2.3.2 Comparar los tipos de medios para la transmisión de datos

> [!TIP]
> Crea una tabla comparativa lado a lado para fibra óptica, par trenzado y transmisión inalámbrica, centrándote en el ancho de banda, el coste y la complejidad de instalación. Considera los roles de cada tipo, como la fibra óptica en centros de datos, el par trenzado en oficinas y la transmisión inalámbrica para campus, hogares y configuraciones móviles. Presta especial atención a cómo varía la seguridad entre los distintos medios, especialmente en cuanto a la susceptibilidad a escuchas (eavesdropping) o interferencias.

### Cableado de fibra óptica

#### Ventajas:

- **Ancho de banda:** la fibra óptica ofrece las mayores velocidades de transmisión de datos entre los medios analizados en esta sección. La investigación activa continúa mejorando esta tecnología, pero la tecnología actual ya permite transmitir terabits por segundo.
- **Susceptibilidad a interferencias:** como el cableado de fibra óptica utiliza ondas de luz para transmitir datos, no es susceptible a interferencias electromagnéticas, lo que lo hace ideal para entornos con ruido eléctrico, como el generado por motores.
- **Alcance y atenuación:** la fibra óptica es el medio elegido para los cables submarinos intercontinentales que recorren el fondo oceánico, debido a su bajísima pérdida de señal a largas distancias. Los cables de fibra óptica monomodo disponibles comercialmente pueden cubrir fácilmente decenas o cientos de kilómetros antes de necesitar un repetidor
- **Seguridad:** los cables de fibra óptica son muy difíciles de “pinchar” sin ser detectados, lo que los convierte en una excelente opción cuando la seguridad es una prioridad.

#### Desventajas:

- **Coste:** los cables de fibra óptica suelen ser más caros que otras formas de cableado, tanto por el coste del material como por la infraestructura de hardware necesaria y el tiempo de instalación.
- **Fiabilidad:** los cables de fibra óptica son más frágiles que los metálicos y pueden dañarse si no se manipulan correctamente. En particular, tienen un radio mínimo de curvatura bajo el cual no pueden funcionar de forma segura.
- **Complejidad de instalación:** los requisitos de infraestructura de soporte y el manejo adecuado de los cables hacen que la fibra óptica requiera habilidades y equipos más especializados para su instalación y mantenimiento.

### Cableado de par trenzado

#### Ventajas:

- **oste:** el cableado de par trenzado es una tecnología conocida y consolidada desde hace décadas. Está ampliamente disponible y es económico.
- **Complejidad de instalación:** la instalación es considerablemente más sencilla que la de la fibra óptica. En redes domésticas y pequeñas oficinas suele realizarse de forma autónoma, requiriéndose técnicos especializados normalmente solo en entornos exteriores o complejos.
- **Fiabilidad:** los cables son mucho más flexibles, lo que permite instalarlos de forma segura y fiable en espacios reducidos.

#### Desventajas:

-  **Ancho de banda:** el par trenzado suele ser un orden de magnitud más lento que la fibra óptica equivalente. Aun así, es más que suficiente para la mayoría de hogares y pequeñas oficinas, ofreciendo rendimiento Gigabit. Además, el par trenzado supera significativamente a las redes inalámbricas. El cable de par trenzado de mayor calidad disponible actualmente —Ethernet Categoría 7— está clasificado para velocidades de hasta 10 Gb/s.
- **Susceptibilidad a interferencias:** al utilizar señales eléctricas para transmitir datos, el par trenzado es bastante vulnerable a interferencias electromagnéticas del entorno, especialmente cuando no cuenta con apantallamiento.
- **Alcance y atenuación:** el alcance del par trenzado es considerablemente menor que el de la fibra óptica. Los cables Ethernet de par trenzado Categoría 6a suelen tener un alcance máximo aproximado de 100 metros.
- **Seguridad:** al ser más fácil de interceptar que la fibra óptica, el par trenzado supone un mayor riesgo de seguridad; sin embargo, un atacante aún necesita estar físicamente cerca del cable, a diferencia de las redes inalámbricas.

### Transmisión inalámbrica

#### Ventajas:

- **Complejidad de instalación:** no hay cables físicos, por lo que la complejidad y el coste de instalación son significativamente menores que en los medios cableados.
- **Coste:** las redes inalámbricas pueden ser una forma rentable de cubrir grandes áreas donde el cableado no es práctico.
- **Fiabilidad:** las redes inalámbricas proporcionan movilidad a los dispositivos para conectarse desde cualquier ubicación dentro del alcance de la señal. No obstante, la fiabilidad puede verse afectada por interferencias de radio, como se explica a continuación.

#### Desventajas:

- **Ancho de banda:** en escenarios prácticos, el ancho de banda total disponible se comparte entre los dispositivos conectados, por lo que el rendimiento individual varía según las condiciones de la red y el número de dispositivos conectados. Normalmente, se dispone de varios Gb/s de capacidad total para compartir. Esto es inferior a lo que ofrecen el par trenzado o la fibra óptica, que además proporcionan ancho de banda dedicado en lugar de compartido.
- **Susceptibilidad a interferencias:** la transmisión inalámbrica es muy vulnerable a interferencias de otras señales inalámbricas o de radio, y los obstáculos físicos pueden afectar significativamente a la calidad de la señal.

> [!TIP]
> **¿Es seguro tu microondas?**
> Si el WiFi de tu casa se corta cuando alguien utiliza el horno microondas de la cocina, significa que está emitiendo microondas al exterior y debería repararse o sustituirse urgentemente. Los hornos microondas funcionan a 2,4 GHz, que es una de las dos frecuencias utilizadas por WiFi (la otra es 5 GHz). La razón por la que los microondas utilizan 2,4 GHz es que esta es la frecuencia de resonancia del agua; al emitir ondas de alta energía, se excitan las moléculas de agua de los alimentos, provocando su calentamiento.
> La tecnología WiFi se considera segura, aunque también utiliza 2,4 GHz, ya que la potencia de sus señales de radio se mide en milivatios, frente a los microondas domésticos, que emiten entre 800 y 1000 vatios de energía al entorno.
> - **Alcance y atenuación:** el alcance suele estar limitado a un máximo de unos 90 metros en condiciones ideales de línea de visión directa. La intensidad y calidad de la señal disminuyen con la distancia y con obstáculos físicos como paredes.
> - **Seguridad:** las tecnologías inalámbricas tienen una larga y compleja historia de riesgos de seguridad, ya que un atacante no necesita estar físicamente conectado a la red para interceptar la señal. A menudo, los atacantes pueden situarse en un coche fuera del hogar u oficina y capturar señales WiFi por el aire. Se han realizado grandes esfuerzos para añadir capas de cifrado a los sistemas WiFi modernos para mitigar este problema, pero los riesgos aún existen.

## A2.3.3 Explicar cómo se utiliza la conmutación de paquetes para enviar datos a través de una red

> [!TIP]
> **Ten en cuenta la pérdida de paquetes.** Al considerar la carga de trabajo asociada con la conmutación y el enrutamiento de paquetes, asegúrate de recordar que no todos los datos transmitidos llegan al otro extremo. La aparente fiabilidad del Internet moderno se debe en realidad a todos los mecanismos de comprobación de errores que funcionan en segundo plano para compensar la pérdida de paquetes. Esto puede tener un impacto significativo en el rendimiento de una red, especialmente en entornos donde abundan las interferencias electromagnéticas u otras fuentes de perturbación.

- **Conmutación de paquetes (Packet switching):** un método de envío de datos en pequeños bloques, conocidos como “paquetes”, a través de una red. Cada paquete puede tomar una ruta diferente para llegar a su destino.

> [!WARNING]
> **Confundir routers y switches.** Asegúrate de no malinterpretar las diferencias funcionales entre routers y switches en la transmisión de datos en red.

La conmutación de paquetes es la base de la mayoría de las tecnologías de redes modernas, incluido Internet. Consiste en dividir grandes cantidades de datos en fragmentos más pequeños y manejables llamados “paquetes”. Estos paquetes se transmiten de forma independiente a través de la red y se vuelven a ensamblar en su forma original al llegar al destino.

La conmutación de paquetes es una herramienta altamente escalable que permite un uso eficiente de los recursos de red, en contraste con tecnologías más antiguas como la conmutación de circuitos, en la que se utilizaba un canal o cable dedicado durante toda la sesión de comunicación (impidiendo que otros dispositivos pudieran utilizarlo).

### Proceso completo de la conmutación de paquetes

- **Segmentación:** los datos (como un archivo o un correo electrónico) que deben enviarse a través de la red se dividen en partes más pequeñas llamadas “paquetes”. Estos paquetes contienen una porción de los datos, además de información denominada “cabecera” (header), que incluye direcciones de red de origen y destino y otros datos de control. El tamaño MTU (Maximum Transmission Unit) de un paquete suele ser de 1500 bytes, incluyendo la información de la cabecera.

- **Cabecera del paquete:** la cabecera de cada paquete contiene información que ayuda a garantizar una transmisión eficiente y fiable a través de la red, como las direcciones IP de origen y destino. Además, cada paquete incluye un número de secuencia que se utiliza para reordenar los paquetes en el destino en el orden correcto, evitando que el contenido del archivo de datos quede desordenado. La cabecera también contiene información de comprobación de errores, como las sumas de verificación (checksums), que permiten calcular si el paquete ha llegado correctamente o si es necesario solicitar al origen su retransmisión.

- **Enrutamiento:** cada paquete se envía a través de la red de forma independiente del resto de paquetes asociados. Esto significa que los paquetes de un mismo archivo pueden recorrer rutas diferentes en la red, en función de condiciones como la congestión y la disponibilidad de rutas. Esta flexibilidad en el enrutamiento ayuda a optimizar el uso de la red y proporciona un entorno robusto más tolerante a fallos.

- **Routers (enrutadores):** estos dispositivos determinan la ruta óptima que debe seguir cada paquete para llegar a su destino. Inspeccionan la dirección de destino del paquete y utilizan tablas y algoritmos de enrutamiento para decidir el siguiente salto (next hop) al que reenviar cada paquete dentro de la red.

- **Switches (conmutadores):** estos dispositivos suelen operar dentro de redes de área local y dirigen los paquetes entre dispositivos de la misma red. Utilizan direcciones MAC para procesar y reenviar los paquetes.

- **Reensamblaje:** una vez que los paquetes llegan a su destino, se comprueba la información de secuencia y se vuelven a ensamblar en el archivo original en el orden correcto. Es importante destacar que, dado que no se garantiza que todos los paquetes sigan la misma ruta, no se puede asumir que lleguen en el orden correcto. Además, algunos paquetes pueden haberse perdido o corrompido durante la transmisión, por lo que es necesario solicitar al origen que los retransmita.
