<h1 align="center">A2.2. Arquitectura de red
<div align="center">

</div>

## Contenido:

- [A2.2.1 Describir las funciones y aplicaciones prácticas de las topologías de red](#A221-describir-las-funciones-y-aplicaciones-prácticas-de-las-topologías-de-red)  
- [A2.2.3 Comparar y contrastar modelos de redes](#A223-comparar-y-contrastar-modelos-de-redes)
- [A2.2.4 Explicar los conceptos y las aplicaciones de la segmentación de redes](#A224-explicar-los-conceptos-y-las-aplicaciones-de-la-segmentación-de-redes)

<br>

## A2.1.1 Describir la finalidad y las características de las redes

La **topología de red** se refiere a la disposición física y la estructura de los nodos y las conexiones dentro de una red.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2013.jpg" alt="Redes" width="650" height="auto"/>
    <p><em>Figura 13: Topología en estrella. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

En la **topología en estrella**, todos los nodos individuales parten de un punto central.

### Topología en estrella (Star topology)

En una topología en estrella, todos los nodos se conectan a un único dispositivo central (como un conmutador de red o switch). El conmutador central gestiona la tarea de enrutar los mensajes entre los distintos nodos. Este enfoque es muy común en hogares y pequeñas oficinas, donde un único switch proporciona toda la capacidad necesaria para los diferentes dispositivos conectados.

Algunos factores a tener en cuenta en la topología en estrella son:

- **Fiabilidad:** si el dispositivo central falla, la red deja de funcionar.
- **Velocidad de ancho de banda:** aunque cada dispositivo tiene su propia conexión dedicada al nodo central, el rendimiento total depende de la capacidad de procesamiento de dicho nodo central.
- **Escalabilidad:** el switch central suele tener un número limitado de puertos o conexiones que puede gestionar, lo que puede limitar la expansión para satisfacer necesidades futuras.
- **Colisiones:** existe un riesgo mínimo de colisión de datos, ya que cada nodo tiene su propia conexión dedicada.
- **Coste:** bastante bajo si solo se necesitan unos pocos nodos; sin embargo, los costes pueden aumentar si se superan los límites de capacidad del nodo central y se requieren actualizaciones.

> [!TIP]  
> Cada topología (estrella, malla, híbrida) responde a necesidades diferentes. Asegúrate de comprender por qué cada una es más adecuada que otra para situaciones específicas. Aprende los diagramas de las distintas topologías para visualizar cómo se conectan los nodos, ya que esto proporciona una comprensión crucial de cómo se ve afectado el flujo de datos si un nodo falla.

### Topología en malla (Mesh topology)

En una topología en malla, cada nodo tiene una conexión directa e inmediata con todos los demás nodos. Aunque normalmente se representa como una malla completa, también existen mallas parciales.

Las mallas son adecuadas para entornos grandes en los que la fiabilidad de las rutas individuales puede ser un problema. Las infraestructuras críticas, como los entornos militares y de aviación, suelen utilizar topologías en malla para garantizar una alta resiliencia de la red frente a cualquier punto de fallo.
  
Los sistemas de malla inalámbrica, como Meshtastic, también han empezado a ganar popularidad entre aficionados a la tecnología y como medio para proporcionar conectividad en zonas remotas y propensas a desastres.

En una topología en malla, todos los nodos están interconectados entre sí.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2014.jpg" alt="Redes" width="650" height="auto"/>
    <p><em>Figura 14: Topología en malla. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

Algunos factores a considerar en un entorno de malla incluyen:

- **Fiabilidad:** muy alta y robusta frente al fallo de cualquier nodo individual o ruta de comunicación.
- **Velocidad de ancho de banda:** alta, ya que cada nodo puede comunicarse directamente con el nodo de destino.
- **Escalabilidad:** añadir nuevos nodos es costoso, ya que es necesario instalar cableado e infraestructura hacia todos los demás nodos de la red.
- **Colisiones:** riesgo mínimo de colisiones debido a las conexiones directas disponibles.
- **Coste:** alto, debido a todo el cableado adicional y la infraestructura de red necesaria para las conexiones redundantes.

### Topología híbrida (Hybrid topology)

La topología híbrida combina una mezcla de dos o más topologías diferentes. Aprovecha al máximo las ventajas de cada enfoque y minimiza sus desventajas. Los enfoques híbridos son adecuados para grandes empresas y redes de telecomunicaciones.

En la ilustración, se utiliza un enfoque de malla para la interconexión de diferentes estaciones base con el fin de proporcionar fiabilidad y durabilidad entre ellas, y después cada estación base gestiona una topología en estrella para los dispositivos individuales conectados a ella.

Los factores a considerar en un enfoque híbrido incluyen:

- **Fiabilidad:** generalmente bastante alta; si un nodo falla, solo afecta a los clientes conectados directamente a él, pero no a otras partes de la red.
- **Velocidad de transmisión:** depende de la configuración exacta y de la combinación de topologías implementadas; pueden aparecer cuellos de botella si no se diseña cuidadosamente.
- **Escalabilidad:** normalmente muy alta y adaptable a necesidades y circunstancias cambiantes; una pequeña ampliación de la red puede comenzar como un nodo secundario (spoke) en una estrella y posteriormente actualizarse a un nodo completo dentro de una malla si es necesario.
- **Colisiones:** nuevamente, depende de la configuración y de la combinación de topologías utilizadas.
- **Coste:** probablemente más alto al inicio, pero generalmente más eficiente a largo plazo.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2015.jpg" alt="Redes" width="650" height="auto"/>
    <p><em>Figura 15: Topología híbrida. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

La **topología híbrida** es una combinación de las topologías en malla y en estrella: los puntos clave de la red están interconectados como una malla y, a su vez, cada uno de esos puntos actúa como centro de su propia estrella de nodos conectados.

<br>

## A2.2.3 Comparar y contrastar modelos de redes

### Cliente–servidor

El **modelo cliente–servidor** es aquel en el que los dispositivos adoptan el rol de cliente, que solicita un servicio de red, o de servidor, que proporciona un servicio de red.

Ventajas:

- **Control centralizado:** es más fácil gestionar y actualizar los sistemas desde un punto central.
- **Escalabilidad:** resulta más sencillo añadir un servidor más potente (por ejemplo, con mayor capacidad de procesamiento, memoria o almacenamiento) si se trata de un sistema centralizado.
- **Eficiencia:** un servidor puede optimizarse para una tarea específica.
- **Seguridad:** es mucho más fácil gestionar los riesgos de seguridad cuando todo se ejecuta desde un punto central.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2016.jpg" alt="Redes" width="450" height="auto"/>
    <p><em>Figura 16: Cliente-servidor. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>
  
Desventajas:

- **Punto único de fallo:** si el servidor deja de funcionar, todos los servicios asociados a él también fallan.
- **Punto único de riesgo:** si la seguridad del servidor se ve comprometida, todos los datos y servicios gestionados por el punto central quedan expuestos y vulnerables.
- **Coste:** crear un punto central para gestionar todas las solicitudes implica una inversión significativa en hardware y software costosos para soportar esa demanda.

Aplicaciones en el mundo real:

- **Navegación web:** los clientes (navegadores) solicitan páginas web a los servidores.
- **Correo electrónico:** los servidores de correo gestionan el envío y la recepción de mensajes desde y hacia las aplicaciones cliente.
- **Banca en línea: los servidores centrales gestionan las transacciones, la autenticación y el almacenamiento de datos, ofreciendo alta seguridad y fiabilidad.

### Peer-to-peer (P2P)

En el **modelo peer-to-peer** no existe un servidor que coordine los servicios de red; cada dispositivo actúa tanto como cliente como servidor y se comunica con los demás pares. La provisión de servicios de red se distribuye entre los propios dispositivos.

El principal reto del modelo peer-to-peer es la coordinación, ya que no existe una fuente “autoritaria” clara a la que consultar para encontrar determinados servicios.

Ventajas:

- **Descentralización:** no existe un único punto de fallo ni de riesgo.
- **Rentabilidad:** no es necesario invertir en hardware o software costoso, ya que la carga se reparte entre todos los clientes.
- **Escalabilidad:** a medida que crece el tamaño de la red, también aumenta la capacidad de los servicios que puede ofrecer. Cada nuevo par añade capacidad adicional.
- **Compartición directa:** los servicios pueden proporcionarse directamente de un ordenador a otro, reduciendo cuellos de botella.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2017.jpg" alt="Redes" width="450" height="auto"/>
    <p><em>Figura 17: Peer-to-peer. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>
  
Desventajas:

- **Coordinación:** mantener la configuración, los parches de seguridad y la sincronización de datos entre múltiples nodos de la red puede ser muy complicado.
- **Fiabilidad:** dado que los servicios son proporcionados por pares, que son simplemente dispositivos cliente de la red, si un usuario apaga su dispositivo, deja de ofrecer los servicios que estaba proporcionando. La disponibilidad de sistemas y recursos en la red puede variar sin previo aviso.

Aplicaciones en el mundo real:

- **BitTorrent:** los archivos se comparten directamente entre usuarios sin un centro de coordinación centralizado.
- **Voz sobre IP (VoIP):** los datos de llamadas y videoconferencias se enrutan directamente de cliente a cliente, en lugar de crear grandes cuellos de botella en un servidor centralizado.
- **Blockchain:** Bitcoin y otras cadenas de bloques operan bases de datos descentralizadas distribuidas entre muchos nodos para ayudar a proteger el registro de transacciones frente a manipulaciones.

<br>

## A2.2.4 Explicar los conceptos y las aplicaciones de la segmentación de redes

La **segmentación de red** se refiere a la división lógica de una red más grande en partes más pequeñas y manejables. Cada uno de estos segmentos puede aislarse de los demás para proporcionar mayor seguridad, mejor rendimiento o una gestión más eficiente de los recursos del sistema.

- **Segmentación de red:** división de una red informática en subredes más pequeñas y diferenciadas para mejorar el rendimiento, la seguridad y la administración.

Dos enfoques comúnmente utilizados para la segmentación de redes son el **subnetting (subredes)** y las **redes de área local virtuales (VLAN)**.

El **subnetting** divide una red en subredes basándose en rangos únicos de direcciones IP. Por ejemplo, una escuela puede ubicar los dispositivos del personal en el rango 192.168.0.X y los dispositivos del alumnado en el rango 192.168.1.X. Cada subred puede compartir la misma infraestructura de red, como puntos de acceso inalámbricos, switches y cableado, pero no “verá” los dispositivos de la otra subred. Este enfoque permite agrupar dispositivos de forma lógica según el departamento, la función o la ubicación geográfica, y posibilita aplicar diferentes políticas de seguridad según las necesidades de la organización.

Las **VLAN (Virtual LAN)** son otra forma de separar una red física en dos o más redes lógicas sin necesidad de duplicar la infraestructura. Crean dominios de difusión (broadcast domains) distintos que están aislados entre sí, a menos que se permita explícitamente su comunicación mediante enrutamiento. El tráfico queda aislado únicamente a los miembros de la VLAN. Mientras que un dispositivo cliente puede cambiar de subred modificando manualmente su dirección IP, las VLAN son más seguras y normalmente utilizan direcciones MAC o credenciales de inicio de sesión para determinar a qué VLAN se conecta un dispositivo. Dado que una VLAN es una construcción lógica y no física, es importante tener en cuenta que puede extenderse a través de múltiples redes físicas (por ejemplo, mediante un enlace VPN).

Independientemente del método utilizado, la segmentación reduce el tráfico global de la red dentro de cada segmento, permitiendo una transmisión de datos más eficiente. La congestión de red causada por aplicaciones de alto ancho de banda puede limitarse a un segmento concreto, de modo que el resto de segmentos no se vean afectados. La seguridad también mejora de forma significativa, ya que la visibilidad de los servidores y sus servicios puede restringirse a VLAN específicas.
