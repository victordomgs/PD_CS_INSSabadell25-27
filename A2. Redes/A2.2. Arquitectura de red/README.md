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
