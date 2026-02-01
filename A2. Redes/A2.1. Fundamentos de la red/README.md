<h1 align="center">A2.1. Fundamentos de la red
<div align="center">

</div>

## Contenido:

- [A2.1.1 Describir la finalidad y las características de las redes](#A211-describir-la-finalidad-y-las-características-de-las-redes)  
- [A2.1.2 Describir la finalidad, las ventajas y las limitaciones de las infraestructuras digitales modernas](#A212-describir-la-finalidad-las-ventajas-y-las-limitaciones-de-las-infraestructuras-digitales-modernas)
- [A2.1.3 Describir la función de los dispositivos de red](#A213-describir-la-función-de-los-dispositivos-de-red)
- [A2.1.4 Describir los protocolos de red utilizados para el transporte y la aplicación](#A214-describir-los-protocolos-de-red-utilizados-para-el-transporte-y-la-aplicación) 

<br>

## A2.1.1 Describir la finalidad y las características de las redes

Bienvenido a las redes de computadoras. En las últimas décadas, las redes se han convertido en una parte omnipresente e integral de nuestras vidas modernas. Usamos las redes para:

- comunicarnos y colaborar instantáneamente con personas de todo el mundo
- acceder a una gran cantidad de información, entretenimiento y servicios al alcance de nuestros dedos
- realizar transacciones comerciales, operaciones bancarias y compras en línea con facilidad
- aprender nuevas habilidades, asistir a clases virtuales y ampliar nuestros conocimientos
- controlar y supervisar de forma remota nuestros hogares, coches y otros dispositivos conectados
- compartir fotos, vídeos e historias con familiares y amigos en tiempo real.

> [!IMPORTANT]  
> - **Red de computadoras:** un sistema que conecta computadoras y otros dispositivos para compartir recursos (digitales o físicos) e información.
> - **Red de área local:** un sistema que conecta computadoras y otros dispositivos dentro de un área geográfica pequeña, como una oficina o un hogar.

El poder y la ubicuidad de las redes de computadoras han transformado verdaderamente la forma en que vivimos, trabajamos y nos divertimos. En este capítulo, profundizaremos en el funcionamiento interno de estos complejos sistemas que se han vuelto tan comunes que apenas les prestamos atención, excepto cuando algo sale mal.

### Redes de área local (LAN)

Una **red de área local** es una red de computadoras que están interconectadas en una ubicación geográfica pequeña, normalmente limitada a una sola propiedad, como una casa, un edificio o un campus. Estos son los tipos de redes más antiguos, aunque el equipo utilizado en las versiones modernas no se parece en nada a las versiones históricas.

El propósito de estas redes es facilitar el intercambio de recursos entre las diferentes computadoras, como archivos, impresoras, aplicaciones y acceso a redes externas, como Internet.

Las LAN suelen tener un alto ancho de banda interno, con velocidades que van desde 100 Mbps (megabits por segundo) hasta 10 Gbps (gigabits por segundo). Su reducido alcance geográfico hace que, por lo general, no existan problemas de latencia (el tiempo de retraso para que los datos se transmitan a través de la red).

La mayoría de los hogares y muchas LAN corporativas utilizan actualmente una combinación de cables Ethernet cableados y tecnologías de redes inalámbricas. Las LAN inalámbricas dedicadas a veces pueden denominarse WLAN.

### Redes de área amplia (WAN)

Una **red de área amplia** permite la interconexión de múltiples redes de área local a lo largo de una distancia geográfica mayor. Esta distancia de conexión puede ser dentro de una misma ciudad, entre diferentes ciudades o incluso entre distintos continentes. Por ejemplo, esto podría utilizarse para compartir recursos entre diferentes sucursales de una empresa.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%201.jpg" alt="WAN" width="450" height="auto"/>
    <p><em>Figura 1: WAN. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

> [!IMPORTANT]  
> - **Red de área amplia:** un sistema que conecta computadoras y otros dispositivos a lo largo de una gran área geográfica, normalmente conectando varias LAN entre sí.
> - **Red de área personal:** una red para dispositivos personales dentro del alcance de una persona, generalmente conectados mediante Bluetooth.

Tradicionalmente, una WAN no utiliza Internet para esta interconexión; en su lugar, cuenta con su propia infraestructura de red dedicada para conexiones de larga distancia, como cableado de fibra óptica o transmisión por microondas punto a punto.

En la práctica, la mayoría de las WAN modernas utilizan la infraestructura existente de Internet de alta velocidad y establecen una WAN virtualizada mediante el uso de tecnología de redes privadas virtuales (VPN), que se tratará más adelante.

### Redes de área personal (PAN)

Una red de área personal se refiere a los dispositivos que están interconectados y centrados alrededor de una persona. Una PAN cubre un rango muy pequeño y normalmente se limita a unos 10 metros.

Aunque los dispositivos conectados mediante cable USB podrían considerarse parte de la PAN de una persona, Bluetooth es la tecnología de conectividad más comúnmente asociada con las PAN. La naturaleza interconectada de tus auriculares, teléfono, cámara, reloj y cualquier otro dispositivo que puedas llevar contigo es lo que forma tu PAN.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%202.jpg" alt="PAN" width="450" height="auto"/>
    <p><em>Figura 2: PAN. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

### Redes privadas virtuales (VPN)

Las redes privadas virtuales hacen referencia al uso de infraestructura de red pública para establecer un túnel seguro y privado con fines propios de comunicación. El cifrado permite a los usuarios enviar y recibir datos a través de Internet público como si sus dispositivos informáticos estuvieran conectados directamente a su propia red privada.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%203.jpg" alt="VPN" width="450" height="auto"/>
    <p><em>Figura 3: VPN. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

> [!IMPORTANT]  
> - **Red privada virtual:** una conexión segura que funciona a través de Internet para proporcionar comunicación privada entre tu red y un servidor remoto.
> - **Internet:** una red global de redes de computadoras que están interconectadas entre sí y se comunican mediante protocolos estandarizados.

Existen muchas “empresas de VPN” que anuncian sus servicios a consumidores particulares para utilizar esta tecnología y hacer que sus actividades de navegación por Internet parezcan realizarse desde una ubicación geográfica diferente a la real. Aunque esto es una tecnología útil para evitar bloqueos geográficos y situaciones similares, se trata de un caso de uso distinto al uso corporativo de las VPN.

Las empresas utilizan el túnel seguro de una VPN para proporcionar a los empleados acceso remoto a sus redes corporativas como si estuvieran físicamente presentes en su sede central.

Las VPN ayudan a reducir la necesidad de contar con infraestructura de red dedicada y costosa a largas distancias, como históricamente se habría requerido para una WAN.

<br>

## A2.1.2 Describir la finalidad, las ventajas y las limitaciones de las infraestructuras digitales modernas

### Internet

Sugerir que **Internet** es un componente central de la infraestructura digital moderna es un poco como decir que el agua está mojada. Internet es la red global. Conecta millones de redes privadas, públicas, académicas, empresariales y gubernamentales en una enorme red global. Proporciona un acceso fácil a una gran cantidad de información y servicios, además de facilitar comunicaciones casi instantáneas. El comercio, las empresas y los mercados globales dependen ahora enormemente de ella.

Dicho esto, Internet está lejos de ser perfecta. En las décadas de 1970 y 1980, cuando se estaban desarrollando los componentes clave de lo que acabaría convirtiéndose en Internet, no existía un plan maestro, y la enorme escala del resultado habría sido imposible de imaginar o prever. Esto significa que existen vulnerabilidades integradas en las tecnologías fundamentales de las que depende Internet. Es susceptible a ataques informáticos, denegación de servicio, phishing y muchas otras amenazas que veremos más adelante en este capítulo.

### Computación en la nube

La nube es un nombre de sonido misterioso para una parte crítica de la infraestructura moderna, ideado por algún experto en marketing. En esencia, se trata de servicios informáticos que grandes empresas tecnológicas ponen a disposición en régimen de alquiler, de modo que no necesitas comprar tus propios sistemas informáticos físicos para servidores y otras infraestructuras. Las empresas y los particulares pueden usar Internet para acceder al software y hardware proporcionados por estas compañías tecnológicas en sus enormes centros de datos.

Existen algunos beneficios de este enfoque. Permite escalar fácilmente el uso de recursos hacia arriba o hacia abajo sin una gran inversión financiera. También reduce los costes de mantenimiento informático para las pequeñas empresas, ya que todo forma parte del servicio contratado.

Debido a que la comunicación con los sistemas alquilados en la nube se realiza a través de Internet, es evidente que contar con una conectividad a Internet fiable, estable y de alta velocidad es imprescindible. Las preocupaciones sobre la seguridad y la privacidad de los datos almacenados en estos sistemas de terceros también pueden ser un motivo legítimo de inquietud, ya que estos sistemas están fuera de tu control.

Amazon Web Services, Google Cloud y Microsoft Azure son tres de los principales proveedores de servicios en la nube en el momento de redactar este texto.

### Sistemas distribuidos

Un sistema distribuido conecta múltiples computadoras, o redes de computadoras, para alcanzar objetivos comunes. Son más tolerantes a fallos que otros sistemas, ya que, si un nodo falla, existen otras rutas de conectividad a través de las cuales el resto de la red puede seguir funcionando. Esta resiliencia tiene como coste una mayor complejidad, lo que significa que son más difíciles de diseñar, gestionar y mantener. En particular, garantizar la consistencia de los datos entre los distintos nodos puede ser un desafío.

Las herramientas de redes entre pares (peer-to-peer), como BitTorrent, son ejemplos de sistemas distribuidos, al igual que las cadenas de bloques (blockchains).

Los sistemas distribuidos utilizados por algunas grandes redes corporativas incluyen las redes de distribución de contenido (Content Delivery Networks) para ayudar a distribuir contenido a usuarios de todo el mundo.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%204.jpg" alt="Redes" width="450" height="auto"/>
    <p><em>Figura 4: Redes Distribuidas. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

Con cada punto representando un nodo en la red, un sistema distribuido tiene muchos caminos diferentes para recorrer entre dos puntos cualesquiera.

### Computación en el borde (Edge computing)

La computación en el borde acerca la capacidad de procesamiento y almacenamiento de datos a la ubicación física donde se necesita, para reducir la latencia y ahorrar ancho de banda.

Las grandes empresas de distribución de contenidos, como Netflix, Spotify y otras similares, pueden utilizar el modelo de computación en el borde para desplegar clústeres de servidores en ciudades clave, con el fin de reducir la cantidad de tráfico que debe viajar de ida y vuelta a sus centros principales. Estos servidores pueden almacenar en caché los archivos más solicitados en cada región, acelerando significativamente el servicio para esos clientes, al mismo tiempo que se preserva el ancho de banda para obtener archivos solicitados ocasionalmente que no están en la caché local.

Este aumento de puntos finales en la red supone un incremento de los vectores de ataque para un adversario, por lo que conlleva una mayor complejidad en términos de seguridad y mantenimiento.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%205.jpg" alt="Redes" width="550" height="auto"/>
    <p><em>Figura 5: Computación en el borde. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

La computación en el borde sitúa los recursos computacionales más cerca del punto de demanda, lo que reduce la carga de red para los servidores centrales en la nube.

### Redes móviles

Las redes de telecomunicaciones móviles son ahora omnipresentes a nivel mundial. Hay muchas partes del mundo donde la conectividad móvil es la única disponible, ya que las redes móviles pueden desplegarse sin el coste de excavar el terreno para instalaciones de cableado.

La movilidad que facilitan estas redes permite un acceso cómodo a la información y a la comunicación en movimiento, y da servicio a regiones muy amplias. Dicho esto, la necesidad de instalar torres en numerosos lugares y las complejidades geográficas hacen que las redes de telefonía móvil tengan zonas muertas, es decir, áreas sin cobertura de red. La intensidad de la señal puede variar, lo que afecta a la calidad del servicio y al rendimiento del ancho de banda.

En el momento de redactar este texto, muchos países están en proceso de desplegar redes móviles de quinta generación (5G), que aumentarán las velocidades hasta 10 Gbps en picos de datos, con una media de 100 Mbps.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%206.jpg" alt="Redes" width="550" height="auto"/>
    <p><em>Figura 6: Redes móviles. Fuente: Universitat Internacional de Valencia</em></p>
  </div>

<br>

## A2.1.3 Describir la función de los dispositivos de red

Muchas redes domésticas o de pequeñas oficinas pueden tener un único dispositivo físico que conecta todos sus dispositivos con su proveedor de servicios de Internet. Este único dispositivo suele denominarse coloquialmente router o módem. La realidad es que existen varios dispositivos lógicos funcionando, aunque todos estén integrados en una sola unidad física. Ahora examinaremos las funciones de estos diferentes dispositivos.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%207.jpg" alt="Redes" width="550" height="auto"/>
    <p><em>Figura 7: Dipositivos en una pequeña red local. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

> [!TIP]  
> **¡Comprende el propósito!
Existen muchos dispositivos diferentes que desempeñan distintos roles dentro de una red de computadoras. Puede resultar fácil confundirlos porque la mayoría de las redes domésticas tienen un único dispositivo físico que desempeña muchos de estos roles. Concéntrate en comprender el propósito y la funcionalidad de cada tipo de dispositivo. Pregúntate por qué se necesita este tipo de dispositivo y qué problemas resuelve.
