<h1 align="center">A1.3. Sistemas operativos y de control
<div align="center">

</div>

## Contenido:

- [A1.3.1. Describe el papel de los sistemas operativos](#A131-describe-el-papel-de-los-sistemas-operativos)  
- [A1.3.2. Describe las funciones de un sistema operativo](#A132-describe-las-funciones-de-un-sistema-operativo)
- [A1.3.3. Compara diferentes enfoques de planificación](#A133-compara-diferentes-enfoques-de-planificación)
- [A1.3.4. Evalúa el uso del manejo de interrupciones y del sondeo](#A134-evalúa-el-uso-del-manejo-de-interrupciones-y-del-sondeo)

<br>

## A1.3.1. Describe el papel de los sistemas operativos

Un sistema operativo (SO) es el software fundamental que gestiona los recursos de hardware y software de un ordenador y proporciona servicios comunes para los programas informáticos. Actúa como intermediario entre el usuario y el hardware del ordenador, garantizando un funcionamiento eficiente y seguro del sistema.

Los sistemas operativos simplifican la interacción de los usuarios con el hardware del ordenador al abstraer las complejidades subyacentes. Esto significa que los usuarios y las aplicaciones no necesitan comprender el funcionamiento detallado de componentes de hardware como la CPU, la memoria y los dispositivos de entrada/salida. En su lugar, el sistema operativo proporciona un conjunto de servicios e interfaces de alto nivel que ocultan estas complejidades, haciendo que el sistema sea más fácil de usar y de programar.

El papel principal de un sistema operativo es gestionar de forma eficaz los recursos del ordenador. Esto incluye:

- **Gestión de la CPU:** asignar tiempo de CPU a los distintos procesos y garantizar una ejecución eficiente.
- **Gestión de la memoria:** gestionar la asignación y liberación de memoria a las aplicaciones, así como la memoria virtual para ampliar la capacidad de la memoria física.
- **Gestión del almacenamiento:** organizar y gestionar los datos en los dispositivos de almacenamiento, asegurando un almacenamiento y una recuperación de datos fiables.
- **Gestión de dispositivos:** controlar y coordinar los dispositivos de hardware, proporcionando controladores e interfaces para un funcionamiento fluido.

Algunos de los sistemas operativos modernos más conocidos son Microsoft Windows, Apple macOS y Linux en ordenadores y portátiles, mientras que Android e iOS son más populares en dispositivos portátiles pequeños como los smartphones.

<br>

## A1.3.2. Describe las funciones de un sistema operativo

Las funciones de un sistema operativo son múltiples y garantizan que el sistema funcione de manera fluida, eficiente y segura. A continuación, se analizan las distintas funciones críticas de un sistema operativo, mostrando cómo mantiene la integridad del sistema mientras ejecuta procesos en segundo plano y gestiona los recursos.

### Gestión de la memoria

La gestión de la memoria es una función fundamental de un sistema operativo (SO) e implica el control y la coordinación de la memoria principal (RAM) de un ordenador. El SO se asegura de que la memoria se asigne de forma eficiente a los procesos y aplicaciones, mantiene la estabilidad del sistema y protege las áreas de memoria frente a accesos no autorizados.

Cuando se abre o ejecuta una aplicación, el SO la carga en la RAM. Primero, localiza la aplicación en el dispositivo de almacenamiento (normalmente un disco duro o una unidad de estado sólido) y lee el archivo ejecutable (.exe en Windows o .app en Mac). Este archivo contiene todo el código de la aplicación y sus datos iniciales.

A continuación, el SO asigna el espacio de memoria necesario para la aplicación. Esto incluye espacio para el código, los datos y cualquier otro recurso requerido. El SO garantiza que la aplicación disponga de suficiente espacio para ejecutarse sin interferir con otros procesos.

Una vez que la aplicación está cargada en la RAM, el SO gestiona continuamente la memoria para asegurar un funcionamiento eficiente y la estabilidad del sistema. Mientras la aplicación se está ejecutando, el SO puede asignar y liberar memoria dinámicamente según las necesidades de la aplicación. Además, el SO se asegura de que cada proceso opere dentro de su propio espacio de memoria. Esto evita que los procesos interfieran entre sí, lo que mejora la seguridad y la estabilidad del sistema.

Si las aplicaciones requieren más memoria de la disponible en la RAM, el SO puede utilizar **memoria virtual** para mantener el sistema funcionando correctamente. La memoria virtual consiste en que el SO asigna parte del espacio del disco duro (HDD) o de la unidad de estado sólido (SSD) para utilizarlo como si fuera RAM. Esta no es una situación ideal, ya que el acceso a un dispositivo de almacenamiento es mucho más lento que el acceso a la RAM; sin embargo, al intercambiar en la RAM los procesos con mayor prioridad y mover a la memoria virtual los de menor prioridad, el SO puede seguir ejecutando el sistema a un nivel óptimo.

> [!NOTE]  
> **Memoria virtual:** una técnica de gestión de memoria que permite a un ordenador utilizar más memoria de la que está físicamente disponible mediante la transferencia temporal de datos desde la RAM al almacenamiento en disco, lo que posibilita la ejecución de programas más grandes y la multitarea.

> [!TIP]  
> Piensa en la gestión de la memoria como en la organización de libros en una estantería. El sistema operativo asigna a cada libro (proceso) su propio espacio en la estantería (memoria). Del mismo modo que no permitirías que los libros se superpongan o se mezclen, el sistema operativo se asegura de que cada proceso tenga su propia área protegida en la memoria.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2071.%20Relaci%C3%B3n%20entre%20memoria%20virtual%20y%20memoria%20f%C3%ADsica.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 48: Relación entre memoria virtual y memoria física. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

### Gestión de archivos

La gestión de archivos es una función crucial de un sistema operativo (SO) y comprende el almacenamiento, la recuperación, la organización y la manipulación de datos en los dispositivos de almacenamiento. El SO proporciona una forma estructurada de gestionar archivos y directorios, garantizando la estabilidad y la seguridad del sistema.

El SO emplea un sistema de archivos jerárquico para organizar los archivos de manera lógica y estructurada. Los archivos se organizan en directorios (o carpetas), que pueden contener a su vez otros directorios, creando una estructura en forma de árbol. Esta organización facilita a los usuarios y a las aplicaciones la localización y gestión de los datos.

El SO permite una serie de operaciones estándar que los usuarios y las aplicaciones pueden realizar sobre archivos y directorios, entre las que se incluyen: crear nuevos archivos y directorios; leer y escribir datos en archivos; eliminar archivos; cambiar el nombre de archivos; y mover o copiar archivos y directorios a diferentes ubicaciones.

Para garantizar la coherencia y evitar conflictos, el SO impone reglas para la denominación de archivos, asegurando que no existan dos archivos con el mismo nombre dentro de un mismo directorio. Los archivos suelen tener extensiones, como .jpg o .exe, que indican el tipo de archivo y la aplicación asociada, aunque, dependiendo de la configuración del sistema operativo, estas extensiones pueden estar ocultas para el usuario.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2072.%20Windows%20File%20Explorer%20view.png" alt="Walden" width="350" height="auto"/>
    <p><em>Figura 49: Windows File Explorer. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2073.%20MacOS%20finder%20view.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 50: MacOS finder view. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2074.%20Los%20tipos%20de%20archivo%20m%C3%A1s%20comunes.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 51: Tipología de archivos. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>
  
Al gestionar el almacenamiento de archivos, el sistema operativo utiliza diversos métodos para mejorar el rendimiento; esto incluye la forma en que asigna los archivos en el medio de almacenamiento físico, gestiona el espacio libre y realiza tareas de mantenimiento sobre los datos almacenados.

Una tarea de mantenimiento importante es la desfragmentación, que reorganiza los datos fragmentados en un disco duro (HDD). La fragmentación se produce con el tiempo a medida que los archivos se crean, modifican y eliminan, provocando que queden dispersos en diferentes sectores del disco. La **desfragmentación** tiene como objetivo reorganizar estos fragmentos de archivos en secuencias contiguas, mejorando así el rendimiento del sistema.

> [!NOTE]  
> **Extensión de archivo:** un sufijo al final del nombre de un archivo que indica el tipo de archivo y el programa asociado para abrirlo o procesarlo (por ejemplo, .docx para documentos de Word, .jpg para imágenes).
> **Desfragmentación:** el proceso de reorganizar los datos en un disco duro para que los archivos se almacenen en bloques contiguos, reduciendo la fragmentación y mejorando la velocidad de acceso y el rendimiento general del sistema.

### Gestión de dispositivos

La gestión de dispositivos del sistema operativo garantiza que los dispositivos de hardware funcionen de manera eficiente y se integren sin problemas con las aplicaciones de software. El SO controla y coordina el uso de componentes de hardware como impresoras, unidades de disco, pantallas, teclados e interfaces de red mediante un software especializado llamado controladores de dispositivos (device drivers). Los **controladores de dispositivos** son programas esenciales que permiten al SO comunicarse con el hardware conectado. Cada componente de hardware requiere un controlador específico para funcionar de forma correcta y eficiente. El SO utiliza estos controladores para proporcionar una interfaz uniforme, permitiendo que las aplicaciones interactúen con el hardware sin necesidad de conocer sus características específicas.

- **Controladores de dispositivos (device drivers):** programas de software especializados que permiten al sistema operativo comunicarse y controlar dispositivos de hardware, como impresoras, tarjetas gráficas o adaptadores de red, proporcionando las instrucciones y protocolos necesarios.
- **Buffering (almacenamiento en búfer):** proceso de almacenamiento temporal de datos en un área de memoria (búfer) mientras se transfieren entre dos dispositivos o procesos, lo que ayuda a gestionar las diferencias en la velocidad de transferencia de datos y garantiza un funcionamiento fluido y sin interrupciones.
- **Caching (caché):** proceso de almacenamiento temporal de datos de acceso frecuente en un área de almacenamiento de alta velocidad (caché) para reducir el tiempo de acceso y mejorar el rendimiento del sistema, permitiendo una recuperación más rápida de los datos.
- **Spooling:** proceso de poner en cola datos o tareas en un búfer, normalmente para dispositivos de entrada/salida como impresoras, de modo que puedan procesarse de forma secuencial y a su propio ritmo, permitiendo que el sistema continúe trabajando en otras tareas simultáneamente.
- **Plug and Play (PnP):** tecnología que permite al sistema operativo detectar, configurar e instalar automáticamente los controladores de nuevos dispositivos de hardware cuando se conectan al ordenador, haciendo posible su funcionamiento sin necesidad de una configuración manual por parte del usuario.

El SO también se encarga de la gestión de entrada/salida (E/S) para coordinar la transferencia de datos entre el ordenador y los dispositivos periféricos. Para ello, emplea técnicas como el buffering, el caching y el spooling con el fin de optimizar el rendimiento y la fiabilidad del sistema. El buffering utiliza áreas de almacenamiento temporal para mantener los datos mientras se transfieren entre dispositivos, adaptándose a las diferencias de velocidad entre la CPU y los periféricos. El caching almacena datos de uso frecuente para reducir los tiempos de acceso y mejorar la eficiencia general del sistema. El spooling pone los datos en cola y los envía de forma ordenada a dispositivos como las impresoras, que no pueden manejar flujos de datos intercalados.

Los sistemas operativos modernos han incorporado formas más sencillas y amigables de conectar dispositivos, como la tecnología Plug and Play (PnP). Gracias a PnP, el SO puede identificar automáticamente un dispositivo que se ha conectado, instalar los controladores necesarios y configurar los ajustes sin necesidad de intervención del usuario. Además, el SO es capaz de detectar errores y actuar para recuperarse de ellos, reiniciando el dispositivo, reinicializando los controladores o notificando al usuario del problema.

Por último, el SO proporciona mecanismos de seguridad y control de acceso para garantizar que solo los usuarios y procesos autorizados puedan acceder a determinados dispositivos, manteniendo la integridad y la seguridad del sistema.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2075.%20Device%20drivers%20como%20intermediarios%20entre%20el%20sistema%20operativo%20y%20el%20hardware.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 52: Device drivers como intermediarios entre el sistema operativo y el hardware. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

### Planificación (Scheduling)

El sistema operativo planifica la ejecución de múltiples procesos determinando qué proceso se ejecuta en cada momento. El **planificador (scheduler)** es el responsable de asignar tiempo de CPU a los procesos, garantizando un uso eficiente y justo de los recursos del sistema. Esta función es fundamental en entornos de multitarea, donde múltiples aplicaciones y procesos en segundo plano se ejecutan de forma concurrente. Mediante la implementación de distintos algoritmos de planificación, el SO busca optimizar el rendimiento, reducir los tiempos de espera y mantener la estabilidad del sistema.

En la sección A1.3.3 se profundizará en enfoques concretos de planificación, como first come, first served (primero en llegar, primero en ser atendido), round robin, planificación por colas multinivel y planificación por prioridades. Cada método presenta sus propias ventajas y compromisos, y su idoneidad depende de los requisitos y objetivos específicos del sistema.

#### Seguridad

La seguridad del sistema operativo está diseñada para proteger la integridad, la confidencialidad y la disponibilidad de la información y de los recursos del sistema informático. Para ello, incorpora mecanismos que protegen frente a amenazas, evitan accesos no autorizados y garantizan que los usuarios y las aplicaciones puedan operar de forma segura.

#### Autenticación de usuarios

La autenticación de usuarios puede utilizarse de diversas formas. Inicialmente, el SO puede requerir que el usuario se autentique para iniciar sesión en el sistema, solicitando credenciales como un nombre de usuario y una contraseña, datos biométricos o tokens de seguridad. Una vez iniciada la sesión, y en función de la configuración del usuario, el SO puede permitir o denegar el acceso a determinados archivos, carpetas o aplicaciones del sistema. Esto posibilita que un mismo sistema tenga múltiples usuarios con distintos niveles de acceso, como un administrador y un usuario estándar.

> [!NOTE] 
> **Tokens de seguridad:** dispositivos físicos o digitales que generan o almacenan credenciales de autenticación, como contraseñas de un solo uso o claves criptográficas, utilizados para verificar la identidad de un usuario y asegurar el acceso a sistemas, redes o servicios en línea.

#### Cifrado

El sistema operativo puede proporcionar herramientas y marcos de trabajo para cifrar archivos, canales de comunicación y dispositivos. El cifrado garantiza que los datos, incluso si son interceptados o accedidos por personas no autorizadas, no puedan ser leídos sin la clave de descifrado correspondiente.

#### Auditoría y monitorización

Todas las actividades del sistema, como los inicios de sesión de los usuarios, el acceso a archivos, los errores del sistema y las acciones del administrador, son registradas por el SO en archivos de registro (logs). Estos registros se utilizan con fines de auditoría y monitorización, y pueden ayudar a los administradores a detectar actividades sospechosas y posibles brechas de seguridad. Asimismo, también pueden emplearse para identificar problemas y áreas de mejora en el rendimiento del sistema.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2076.%20Visor%20de%20eventos.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 53: Visor de eventos. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

#### Protección contra malware

El sistema operativo incluye mecanismos para detectar y prevenir infecciones de malware y accesos no autorizados. Entre estos mecanismos se encuentran el software antivirus, los cortafuegos (firewalls) y los sistemas de detección de intrusiones (IDS). Estas herramientas analizan la presencia de software malicioso, supervisan el tráfico de red y bloquean intentos de acceso no autorizados, protegiendo el sistema frente a virus, gusanos, troyanos y otras amenazas maliciosas.

- **Malware:** término general que engloba cualquier software diseñado con intención maliciosa, como virus, gusanos, troyanos, spyware y ransomware, que puede dañar sistemas, robar datos o interrumpir el funcionamiento normal.
- **Virus:** programas de software malicioso que se adjuntan a archivos o programas legítimos y se propagan a otros archivos o sistemas, a menudo causando daños o interrupciones.
- **Gusanos (worms):** malware autorreplicante que se propaga a través de redes sin necesidad de adjuntarse a otros programas, explotando vulnerabilidades para infectar múltiples sistemas.
- **Troyanos (trojans):** programas engañosos que aparentan ser legítimos, pero contienen código malicioso oculto que puede crear puertas traseras, robar datos o causar daños una vez que el usuario los ejecuta.

### Contabilidad (Accounting)

Las funciones de contabilidad del sistema operativo son esenciales para supervisar y gestionar el uso de los recursos del sistema. Estas funciones registran el consumo de recursos por parte de usuarios y procesos, proporcionando datos valiosos para que los administradores del sistema analicen el rendimiento, asignen costes y optimicen la utilización de los recursos. Los principales aspectos de la contabilidad en un SO incluyen:

#### Seguimiento del uso de recursos

El SO monitoriza de forma continua el consumo de distintos recursos por parte de usuarios y procesos. Esto incluye el seguimiento de:

- **Uso de la CPU:** la cantidad de tiempo de CPU consumido por cada proceso o usuario.
- **Uso de la memoria:** la cantidad de memoria RAM asignada y utilizada por cada proceso.
- **Uso del disco:** el espacio de almacenamiento ocupado por los archivos y directorios pertenecientes a cada usuario.
- **Uso de red:** el volumen de datos enviados y recibidos a través de la red por cada proceso o usuario.

#### Contabilidad de procesos

La contabilidad de procesos implica mantener registros detallados de cada proceso que se ejecuta en el sistema. Estos registros incluyen información como:

- **Identificador de proceso (process ID):** un identificador único para cada proceso.
- **Identificador de usuario (user ID):** el identificador del usuario que inició el proceso.
- **Tiempo de ejecución:** el tiempo total de CPU utilizado por el proceso.
- **Tiempos de inicio y fin:** marcas de tiempo que indican cuándo comenzó y cuándo finalizó el proceso.
- **Consumo de recursos:** detalles sobre la cantidad de memoria, E/S de disco y otros recursos utilizados por el proceso.

#### Contabilidad de usuarios

La contabilidad de usuarios registra el uso de recursos por parte de usuarios individuales o grupos de usuarios. Esta información es fundamental para:

- **Asignación de costes:** en entornos multiusuario, como universidades o empresas, los datos de uso de recursos pueden emplearse para asignar costes a distintos departamentos o proyectos en función de su consumo.
- **Gestión de cuotas:** aplicar límites al uso de recursos para evitar que un único usuario monopolice los recursos del sistema; esto puede incluir cuotas de disco (limitando el espacio de almacenamiento que puede usar un usuario) y cuotas de memoria.

#### Monitorización del rendimiento

Las funciones de contabilidad del SO son clave para la monitorización del rendimiento. Mediante el análisis de los datos de uso de recursos, los administradores del sistema pueden identificar:

- **Cuellos de botella:** áreas donde los recursos están siendo sobreutilizados, provocando una degradación del rendimiento.
- **Infrautilización:** recursos que se usan poco, lo que indica posibles áreas de optimización.
- **Tendencias:** patrones de uso de recursos a lo largo del tiempo, que pueden servir para la planificación de capacidad y futuras ampliaciones del sistema.

#### Auditoría e informes

El SO genera informes detallados a partir de los datos de contabilidad recopilados. Estos informes pueden utilizarse para:

- **Auditoría:** garantizar el cumplimiento de las políticas de la organización y de los requisitos normativos mediante la revisión del uso de recursos y los patrones de acceso.
- **Análisis de seguridad:** detectar actividades inusuales o sospechosas mediante el análisis de anomalías en el uso de recursos.
- **Gestión de recursos:** tomar decisiones informadas sobre la asignación de recursos, la configuración del sistema y futuras inversiones.

#### Facturación y repercusión de costes (Billing and chargeback)

En entornos donde el uso de recursos debe facturarse a usuarios o departamentos individuales, como en servicios de computación en la nube o instituciones académicas, las funciones de contabilidad del SO permiten:

- **Facturación basada en el uso:** cobrar a los usuarios en función de su consumo real de recursos, como horas de CPU, uso de memoria y ancho de banda de red.
- **Repercusión de costes (chargeback):** asignar los costes a distintos departamentos o proyectos según su uso de recursos, fomentando la responsabilidad y el uso eficiente de los recursos.

### Interfaz gráfica de usuario (GUI)

Al ofrecer elementos visuales como ventanas, iconos, menús y punteros, el sistema operativo proporciona un entorno fácil de usar para interactuar con el ordenador y permite al usuario ejecutar comandos, gestionar archivos y ejecutar aplicaciones.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2077.%20Ubuntu%20GUI.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 54: Ubuntu GUI. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

#### Elementos de la interfaz de usuario

Los elementos de la interfaz de usuario proporcionados por el sistema operativo permiten al usuario interactuar con el sistema de forma intuitiva. Estos elementos incluyen **ventanas**, que muestran el contenido de aplicaciones, documentos o información del sistema. Los **iconos** ofrecen una representación gráfica de aplicaciones, archivos y funciones del sistema, proporcionando un acceso rápido a los elementos más utilizados. Los **menús** presentan listas de comandos u opciones para acceder a distintas funciones, facilitando la navegación y el uso del sistema. Los **punteros**, normalmente representados por una flecha o cursor, se controlan mediante un dispositivo de entrada como el ratón y permiten seleccionar, arrastrar e interactuar con los elementos de la interfaz gráfica de forma fluida.

#### Gestión de aplicaciones

La interfaz gráfica facilita la gestión y la interacción con múltiples aplicaciones, mejorando la productividad y la experiencia del usuario. El cambio de tareas permite moverse rápidamente entre aplicaciones abiertas, con funciones como la barra de tareas o el conmutador de aplicaciones (Alt + Tab), que hacen posible una navegación eficiente. La gestión de ventanas ayuda a organizar el espacio de trabajo mediante la colocación, superposición y organización en mosaico de las ventanas. Funciones como el ajuste de ventanas a los bordes o esquinas de la pantalla crean un efecto de pantalla dividida para la multitarea. El entorno de escritorio, donde los usuarios pueden colocar iconos, accesos directos y widgets, permite personalizar y organizar el espacio de trabajo según las preferencias individuales.

#### Gestión de archivos y del sistema

La interfaz gráfica simplifica las tareas de gestión de archivos y del sistema mediante herramientas e interfaces visuales. Una herramienta de gestión de archivos basada en GUI, como el Explorador de archivos, permite navegar por los directorios, ver las propiedades de los archivos y realizar operaciones como copiar, mover, eliminar y cambiar el nombre de archivos y carpetas. Esta herramienta suele incluir funciones de búsqueda, ordenación y filtrado para facilitar la gestión de archivos. La GUI también proporciona acceso a la configuración del sistema y a los paneles de control, permitiendo a los usuarios configurar el hardware, el software y las preferencias del sistema a través de interfaces gráficas intuitivas. La funcionalidad de **arrastrar y soltar** ofrece un método sencillo y cómodo para transferir archivos y datos entre aplicaciones y directorios.

#### Accesibilidad

La interfaz gráfica incluye funciones que mejoran la accesibilidad para usuarios con discapacidad, garantizando que el sistema sea utilizable por todas las personas. Los **lectores de pantalla** convierten el texto y los elementos de la interfaz gráfica en voz o en Braille, ayudando a los usuarios con discapacidad visual a navegar por el sistema. Los **temas de alto contraste** y los **ampliadores de pantalla** mejoran la legibilidad para usuarios con baja visión.

Los **atajos de teclado** permiten realizar acciones rápidamente sin depender del ratón o del panel táctil, lo que beneficia a usuarios con movilidad reducida.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2078.%20MacOS%20accesibilidad.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 55: Accesibilidad MacOS. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

#### Retroalimentación visual

La interfaz gráfica de usuario proporciona retroalimentación visual inmediata a las acciones del usuario, mejorando la experiencia general de uso. Los **indicadores de progreso**, como las barras de progreso y las animaciones de carga, informan a los usuarios sobre el estado de operaciones en curso, como transferencias de archivos o instalaciones de software. Las **notificaciones**, en forma de mensajes emergentes y alertas, mantienen a los usuarios informados sobre eventos importantes, actualizaciones o errores. Los **tooltips** (pequeños cuadros de texto informativos que aparecen cuando el usuario pasa el cursor sobre iconos o elementos de la interfaz) ofrecen información adicional u orientación.

#### Personalización y adaptación

La interfaz gráfica permite a los usuarios personalizar su entorno informático según sus preferencias, haciendo que el sistema sea más agradable y eficiente de utilizar. Los usuarios pueden cambiar la apariencia de la GUI seleccionando distintos temas, fondos de pantalla y estilos de ventana, creando una experiencia más personalizada. Los **widgets** y **gadgets** —pequeñas aplicaciones que proporcionan acceso rápido a información y herramientas como el tiempo, calendarios y monitores del sistema— mejoran la funcionalidad y la estética del escritorio. Estas opciones de personalización permiten a los usuarios adaptar su espacio de trabajo a sus necesidades y preferencias, aumentando la satisfacción y la productividad generales.

### Virtualización

La **virtualización** es una característica clave de los sistemas operativos modernos que permite ejecutar múltiples **máquinas virtuales (VM)** en una sola máquina física. Cada máquina virtual funciona de manera independiente, con su propio sistema operativo y aplicaciones. El sistema operativo gestiona este proceso mediante un hipervisor, que asigna tiempo de CPU, memoria y almacenamiento a cada VM, garantizando un uso eficiente de los recursos y permitiendo que cada máquina virtual funcione como si estuviera en un equipo físico independiente.

> [!NOTE] 
> - **Hipervisor:** software que crea y gestiona máquinas virtuales permitiendo que múltiples sistemas operativos se ejecuten simultáneamente en una sola máquina física, compartiendo los recursos de hardware subyacentes.
> - **Balanceo de carga (load balancing):** proceso de distribución del tráfico de red o de aplicaciones entre varios servidores o recursos para garantizar un rendimiento, fiabilidad y disponibilidad óptimos, evitando que un único servidor se sobrecargue.

La virtualización mejora la seguridad y la estabilidad al aislar las máquinas virtuales entre sí, evitando que los problemas de una VM afecten a las demás. También permite la creación de **instantáneas (snapshots)** y copias de seguridad, lo que posibilita guardar el estado actual de una máquina virtual y restaurarlo si es necesario. Las **migraciones en vivo**, que trasladan máquinas virtuales de un host físico a otro sin interrumpir los servicios, son otra característica fundamental que facilita el balanceo de carga y el mantenimiento del hardware.

Además, la virtualización da soporte a la **recuperación ante desastres** y a los **servicios en la nube**. Al permitir que las máquinas virtuales se respalden y restauren fácilmente, el sistema operativo garantiza que las aplicaciones y los datos críticos puedan recuperarse con rapidez en caso de fallo. La virtualización también posibilita el escalado dinámico de la infraestructura informática en entornos cloud, permitiendo a las organizaciones adaptarse con rapidez a cambios en la demanda.

### Redes (Networking)

Los sistemas operativos gestionan y facilitan la comunicación en red. Una de las funciones principales del SO en el ámbito de las redes es establecer y mantener conexiones de red. El sistema operativo gestiona las interfaces y los protocolos de red, permitiendo que los dispositivos se conecten a redes de área local (LAN), redes de área amplia (WAN) y a Internet. Configura los parámetros de red, asigna direcciones IP mediante **DHCP (Dynamic Host Configuration Protocol)** y gestiona el hardware subyacente, como las tarjetas de red (NIC), asegurando una comunicación eficaz entre dispositivos.

El SO también proporciona servicios esenciales para la transmisión de datos y la comunicación entre dispositivos. Implementa diversos protocolos de red, como **TCP/IP (Transmission Control Protocol / Internet Protocol)**, que regulan cómo se fragmentan, direccionan, transmiten, enrutan y reciben los datos. El sistema operativo garantiza la integridad de los datos y una transmisión eficiente mediante el control de errores, el control de flujo y la prevención de la congestión. Además, da soporte a protocolos y servicios de nivel superior, como **HTTP** para la navegación web, **FTP** para la transferencia de archivos y **SMTP** para la comunicación por correo electrónico, facilitando la interacción fluida entre aplicaciones y recursos de red.

La **seguridad y el control de acceso** son funciones críticas de red gestionadas por el sistema operativo. El SO emplea **cortafuegos**, **cifrado** y **mecanismos de autenticación** para proteger los datos durante su transmisión por la red. Los cortafuegos supervisan y controlan el tráfico de red entrante y saliente según reglas de seguridad predefinidas, ayudando a prevenir accesos no autorizados y ataques. El sistema operativo también es compatible con **redes privadas virtuales (VPN)**, que cifran los datos y crean conexiones seguras sobre redes públicas, garantizando la privacidad y la seguridad de los usuarios remotos. Estas medidas protegen las comunicaciones de red y aseguran que solo los usuarios y dispositivos autorizados puedan acceder a los recursos de la red.

<br>

## A1.3.3. Compara diferentes enfoques de planificación

Un sistema operativo necesita métodos de planificación para gestionar de forma eficiente la ejecución de múltiples procesos, garantizando un uso óptimo de la CPU y de otros recursos. La planificación determina el orden en el que los procesos obtienen acceso a la CPU y durante cuánto tiempo, equilibrando las necesidades de las distintas aplicaciones y manteniendo la capacidad de respuesta del sistema. Sin una planificación eficaz, los procesos podrían sufrir retrasos significativos o **monopolizar recursos**, lo que daría lugar a un bajo rendimiento y a la frustración del usuario.

En la siguiente sección se analizarán varios métodos de planificación, entre ellos first come, first served (primero en llegar, primero en ser atendido), round robin, planificación por prioridades y planificación por colas multinivel, cada uno con sus propias ventajas y compromisos.

> [!NOTE] 
> **Monopolizar recursos:** control o dominio del uso de los recursos del sistema (por ejemplo, CPU, memoria o ancho de banda de red) por parte de un único proceso o usuario, a menudo en detrimento de otros procesos o usuarios, lo que provoca ineficiencias o ralentizaciones del sistema.

### Primero en llegar, primero en ser atendido (First Come, First Served – FCFS)

El método **first come, first served (FCFS)** es uno de los algoritmos de planificación más sencillos utilizados por los sistemas operativos para gestionar la ejecución de procesos. En la planificación FCFS, los procesos se ejecutan en el orden en que llegan a la **cola de listos**. Cuando un proceso llega, se añade al final de la cola. El planificador de la CPU selecciona el proceso que se encuentra al inicio de la cola y lo asigna a la CPU hasta que finaliza su ejecución o pasa a un estado de espera por entrada/salida (E/S). Una vez que el proceso actual termina, se selecciona el siguiente proceso de la cola, y así sucesivamente hasta que todos los procesos han sido ejecutados.

La simplicidad de FCFS hace que sea fácil de implementar y de comprender. Sin embargo, presenta algunos inconvenientes, como el **efecto convoy**, en el que procesos cortos pueden verse retrasados por procesos de larga duración, lo que provoca un aumento del tiempo de espera y una menor productividad del sistema. Este método es **no apropiativo (non-preemptive)**, lo que significa que, una vez que un proceso ha sido asignado a la CPU, no puede ser interrumpido hasta que finalice, lo que puede causar ineficiencias en determinados escenarios.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2079.%20FCFS.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 56: FCFS. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

| Ventajas | Desventajas |
|--------|-------------|
| Simple y fácil de implementar | El efecto convoy puede provocar retrasos significativos |
| Justo, ya que procesa las peticiones en el orden en que llegan | Su naturaleza no apropiativa puede provocar ineficiencias y tiempos de espera superiores a la media |

En este ejemplo, P1 llega primero y se ejecuta inmediatamente, seguido de P2 y P3 en el orden en que llegan. Cada proceso se ejecuta hasta completarse antes de que comience el siguiente.

| Process | Queue |
|------|------------------|
| Llega P1 | P1 |
| Llega P2 | P1, P2 |
| Llega P3 | P1, P2, P3 |

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2080.%20Orden%20de%20procesos.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 57: Ejecución de procesos. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

### Round Robin

**Round robin (RR)** es un algoritmo de planificación **apropiativo (pre-emptive)** diseñado para proporcionar un reparto justo del tiempo de CPU entre los procesos. A cada proceso se le asigna un intervalo de tiempo fijo, conocido como **cuanto (quantum)**, durante el cual puede ejecutarse. Cuando el cuanto de un proceso expira, el planificador de la CPU interrumpe (apropia) dicho proceso y lo coloca al final de la cola de listos, seleccionando a continuación el siguiente proceso de la cola para su ejecución. Este ciclo se repite hasta que todos los procesos han finalizado.

La principal ventaja de la planificación round robin es que garantiza un alto nivel de **capacidad de respuesta**, ya que ningún proceso puede monopolizar la CPU durante un periodo prolongado. Este enfoque es especialmente eficaz en sistemas de tiempo compartido, donde múltiples usuarios o aplicaciones necesitan interactuar con la CPU de forma frecuente.

La duración del **cuanto de tiempo** es un factor crítico: si es demasiado corto, el sistema pierde eficiencia debido al exceso de cambios de contexto; si es demasiado largo, el comportamiento del algoritmo se asemeja al de **FCFS**, perdiendo sus ventajas en cuanto a respuesta y equidad.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2081.%20Round%20Robin.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 58: Round Robin. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

| Ventajas | Desventajas |
|--------|-------------|
| Asignación justa del tiempo de CPU entre procesos | La elección del cuanto de tiempo es crítica para el rendimiento |
| Alta capacidad de respuesta y mejor interactividad del sistema | Alto coste de cambios de contexto si el cuanto es demasiado corto |
| Evita que un solo proceso monopolice la CPU | Posible ineficiencia si los procesos suelen completarse dentro de un solo cuanto |

En este ejemplo, cada proceso dispone de un cuanto de tiempo de 2 unidades:

- P1 se ejecuta de tiempo 0 a 2 y es interrumpido.
- P2 se ejecuta de 2 a 4 y es interrumpido.
- P3 se ejecuta de 4 a 6 y es interrumpido.

El ciclo se repite:

- P1 de 6 a 8.
- P2 de 8 a 10.
- P3 de 10 a 12.

| Process | Queue |
|------|------------------|
| Llega P1 | P1 |
| Llega P2 | P1, P2 |
| Llega P3 | P1, P2, P3 |

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2082.%20Orden%20de%20procesos%202.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 59: Ejecución de procesos. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

### Planificación por prioridades (Priority Scheduling)

La planificación por prioridades es un método en el que a cada proceso se le asigna un nivel de prioridad, y la CPU se concede al proceso con la prioridad más alta. Los procesos con mayor prioridad se ejecutan antes que aquellos con prioridad más baja. Si dos procesos tienen la misma prioridad, se planifican según su orden de llegada, normalmente utilizando FCFS.

La prioridad puede ser:

- **Estática:** se asigna cuando el proceso se crea y no cambia durante su ejecución.
- **Dinámica:** puede variar con el tiempo en función de distintos factores, como el envejecimiento (ageing).

El objetivo principal de la planificación por prioridades es garantizar que las tareas críticas se ejecuten lo antes posible, mejorando la capacidad de respuesta de los procesos de alta prioridad. Sin embargo, un inconveniente importante es el riesgo de **inanición (starvation)** de los procesos de baja prioridad, que pueden quedar sin tiempo de CPU si los procesos de alta prioridad dominan continuamente su uso.

Para reducir este problema, algunos sistemas implementan el **envejecimiento (ageing)**, una técnica que incrementa gradualmente la prioridad de los procesos que llevan mucho tiempo esperando, asegurando que finalmente obtengan acceso a la CPU.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2083.%20Cola%20de%20prioridad.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 60: Cola de prioridad. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

Un ejemplo de una **cola prioritaria en un aeropuerto**, donde los pasajeros con mayor prioridad (como los viajeros de primera clase o las personas con discapacidad) reciben un servicio más rápido.

| Ventajas | Desventajas |
|--------|-------------|
| Da prioridad a las tareas importantes, mejorando la capacidad de respuesta del sistema para aplicaciones críticas | Riesgo de inanición (starvation) para los procesos de baja prioridad |
| Flexible, ya que las prioridades pueden ajustarse dinámicamente según las necesidades del sistema | Más compleja de implementar y gestionar que los métodos de planificación más simples |
| Permite adaptarse a situaciones cambiantes del sistema | Posible inversión de prioridades, donde un proceso de baja prioridad mantiene un recurso necesario para uno de mayor prioridad si no se gestiona adecuadamente |

En este ejemplo, P1 y P4, ambos procesos de alta prioridad, se ejecutan primero. Una vez finalizados los procesos de alta prioridad, se ejecuta el proceso de prioridad media P2, seguido del proceso de baja prioridad P3.

| Process | Time | Priority |
|--------|------------------|-------------------|
| P1 | 0 | Alta |
| P2 | 1 | Media |
| P3 | 2 | Baja |
| P4 | 3 | Alta |

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2084.%20Orden%20de%20procesos%203.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 61: Ejecución de procesos. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

### Planificación por colas multinivel (Multilevel Queue Scheduling)

La planificación por colas multinivel es un algoritmo de planificación que divide la cola de listos en varias colas independientes, cada una con su propio algoritmo de planificación y nivel de prioridad. Los procesos se asignan de forma permanente a una de estas colas en función de determinadas características, como el tipo de proceso, su prioridad o sus requisitos de memoria. Cada cola puede utilizar un algoritmo de planificación diferente, como FCFS o round robin, y las colas se planifican entre sí siguiendo un orden específico, normalmente basado en la prioridad.

En este enfoque, las colas de mayor prioridad reciben más tiempo de CPU que las colas de menor prioridad. Por ejemplo, los procesos interactivos pueden situarse en una cola de alta prioridad planificada con round robin, mientras que los procesos por lotes (batch) se colocan en una cola de menor prioridad planificada con FCFS.

El planificador de la CPU selecciona primero los procesos de la cola de mayor prioridad y solo pasa a las colas de menor prioridad cuando las colas superiores están vacías.

| Ventajas | Desventajas |
|--------|-------------|
| Flexibilidad para gestionar distintos tipos de procesos | Inanición de los procesos de baja prioridad si las colas de alta prioridad están ocupadas con frecuencia |
| Prioriza procesos críticos e interactivos, mejorando la capacidad de respuesta | Implementación y gestión complejas |
| Permite adaptar distintos algoritmos de planificación a las necesidades de cada cola | Los procesos se asignan de forma permanente a una cola, lo que puede no ser óptimo si su comportamiento cambia con el tiempo |

En este ejemplo, los procesos de la cola de alta prioridad (P1 y P2) se planifican primero utilizando round robin. Ambos procesos se ejecutan y finalizan. A continuación, el planificador pasa a la cola de prioridad media (P3) y después a la cola de baja prioridad (P4), solo cuando la cola de alta prioridad no tiene procesos listos para ejecutarse. No obstante, el sistema comprueba con frecuencia la cola de alta prioridad, lo que explica por qué P2 (alta prioridad) vuelve a ejecutarse después de P4 (baja prioridad).

| Queue | Priority | process type | Algorithm | Queue |
|----|-----------|----------------|----------------------------|------------------|
| Q1 | Alta | Interactivos | Round Robin (cuanto = 2) | P1, P2 |
| Q2 | Media | Batch (por lotes) | FCFS | P3 |
| Q3 | Baja | Segundo plano / inactivos | FCFS | P4 |

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2085.%20Orden%20de%20procesos%204.png" alt="Walden" width="550" height="auto"/>
    <p><em>Figura 62: Ejecución de procesos. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

> [!CAUTION]
> No olvides que el **cambio de contexto (context switching)** —cuando la CPU cambia de una tarea a otra— puede ralentizar el sistema. Aunque permite la multitarea, un exceso de cambios de contexto puede reducir la eficiencia del sistema, ya que la CPU debe dedicar tiempo a guardar y restaurar el estado de las tareas en lugar de ejecutar procesos.

<br>

## A1.3.4. Evalúa el uso del manejo de interrupciones y del sondeo

La **gestión de interrupciones** y el **sondeo (polling)** son dos técnicas fundamentales que utilizan los sistemas operativos para gestionar la comunicación entre la CPU y los dispositivos periféricos. Cada método presenta sus propias ventajas e inconvenientes, que pueden afectar al rendimiento y a la eficiencia del sistema en función del contexto en el que se utilicen.

### Gestión de interrupciones (Interrupt handling)

La **gestión de interrupciones** es un mecanismo mediante el cual los dispositivos periféricos avisan a la CPU para captar su atención y solicitar servicio. Cuando ocurre un evento, como la entrada de datos desde un teclado o la llegada de información desde una interfaz de red, el dispositivo envía una **señal de interrupción** a la CPU. En ese momento, la CPU pausa la operación que estaba realizando, guarda su estado actual y ejecuta una **rutina de servicio de interrupción (ISR)** para atender el evento.

Este método permite que la CPU permanezca inactiva o ejecutando otras tareas hasta que realmente ocurre un evento, lo que lo hace muy eficiente en entornos donde los eventos se producen de forma esporádica o impredecible. La gestión de interrupciones garantiza que la CPU solo atienda eventos cuando es necesario, reduciendo el desperdicio de ciclos de CPU dedicados a comprobar constantemente si ha ocurrido algo.

> [!NOTE] 
> - **Rutina de servicio de interrupción (ISR):** función especial de un sistema informático que se ejecuta automáticamente en respuesta a una señal de interrupción, encargándose de tareas específicas, como procesar la entrada de dispositivos de hardware o gestionar eventos del sistema, antes de devolver el control al programa principal.
> - **Latencia:** retardo entre el inicio de una acción y la respuesta correspondiente; a menudo se refiere al tiempo que tarda la información en viajar desde su origen hasta su destino dentro de un sistema o una red.

Sin embargo, la aparición frecuente de interrupciones puede introducir **sobrecarga de procesamiento** debido al cambio de contexto que implican. Cada vez que se gestiona una interrupción, la CPU debe guardar su estado y restaurarlo posteriormente, lo que puede consumir tiempo y recursos si las interrupciones son demasiado frecuentes. Además, gestionar un gran volumen de interrupciones puede aumentar el consumo energético, un aspecto especialmente crítico en dispositivos alimentados por batería.

A pesar de estos posibles inconvenientes, la eficiencia de la gestión de interrupciones para tratar eventos esporádicos y minimizar el tiempo de inactividad de la CPU la convierte en el método preferido en muchos sistemas en tiempo real e interactivos, donde es esencial una respuesta inmediata a los eventos.

> [!TIP]
> Una **interrupción** es como el timbre de una puerta que suena mientras estás trabajando. Dejas lo que estás haciendo (pausas el proceso actual), atiendes la puerta (gestionas la interrupción) y luego vuelves a tu tarea. El sistema operativo gestiona estas interrupciones de forma eficiente para que tu trabajo (el proceso principal) no se retrase de manera significativa.

### Sondeo (Polling)

El **sondeo (polling)**, por el contrario, consiste en que la CPU comprueba periódicamente cada dispositivo periférico para verificar si requiere atención. Este método es sencillo y puede ser eficiente en sistemas donde los eventos ocurren a intervalos regulares y predecibles. El sondeo garantiza una **latencia controlada**, ya que la CPU revisa los dispositivos en momentos predeterminados, lo que lo hace adecuado para aplicaciones en tiempo real donde una respuesta puntual es crítica. Además, el polling es fácil de implementar y proporciona un mecanismo simple para asegurar que los dispositivos se revisen de forma regular.

No obstante, el sondeo puede generar una **sobrecarga significativa de procesamiento** en la CPU, ya que esta dedica una parte considerable del tiempo a comprobar repetidamente los dispositivos en lugar de realizar trabajo útil. Esta comprobación continua consume muchos recursos y puede reducir la eficiencia general del sistema.

Además, el sondeo es menos eficiente desde el punto de vista energético en comparación con la gestión de interrupciones, ya que la CPU permanece activa incluso cuando no hay eventos que procesar. Esta actividad constante puede agotar la batería de los dispositivos portátiles más rápidamente que en sistemas que utilizan interrupciones. En entornos donde la frecuencia de los eventos es baja o impredecible, el polling puede resultar muy ineficiente y derrochador, consumiendo ciclos de CPU sin detectar necesariamente nuevos eventos.

### Interrupciones vs sondeo (Interrupts vs Polling)

| Criterio | Interrupciones | Sondeo (Polling) |
|--------|----------------|------------------|
| Frecuencia de eventos | Eficiente para eventos poco frecuentes o impredecibles, ya que la CPU solo responde cuando ocurre un evento | Más efectivo para eventos regulares y predecibles, ya que la CPU comprueba los dispositivos a intervalos fijos |
| Sobrecarga de procesamiento de la CPU | Baja sobrecarga para eventos poco frecuentes, pero puede aumentar con interrupciones de alta frecuencia debido al cambio de contexto | Mayor sobrecarga debido a la comprobación constante de los dispositivos, consumiendo ciclos de CPU incluso cuando no hay eventos |
| Fuente de energía | Más eficiente energéticamente, especialmente en dispositivos alimentados por batería, ya que la CPU permanece inactiva hasta que ocurre un evento | Menos eficiente energéticamente, ya que la CPU permanece activa y comprueba continuamente los dispositivos, aumentando el consumo |
| Previsibilidad de eventos | Ideal para eventos impredecibles, ya que el sistema responde inmediatamente cuando ocurre un evento | Adecuado para eventos predecibles, garantizando comprobaciones regulares en intervalos establecidos |
| Latencia controlada | Puede ofrecer tiempos de respuesta rápidos, pero si las interrupciones son demasiado frecuentes puede haber variabilidad en la respuesta | Proporciona latencia controlada y tiempos de respuesta predecibles, al realizarse comprobaciones periódicas |
| Seguridad | Potencialmente más seguro, ya que el sistema puede responder rápidamente a eventos críticos, reduciendo la ventana de actividad maliciosa | Menos seguro si los intervalos de sondeo son largos, ya que puede retrasarse la detección de eventos críticos |

La elección entre **gestión de interrupciones** y **sondeo** depende de los requisitos y limitaciones específicas del sistema. La gestión de interrupciones suele ser más eficiente para eventos esporádicos y en dispositivos alimentados por batería, aunque puede introducir sobrecarga cuando los eventos son muy frecuentes. El sondeo ofrece una latencia predecible y es sencillo de implementar, pero puede provocar ineficiencias y un mayor consumo de energía. Comprender los compromisos entre ambos métodos es fundamental para diseñar sistemas eficaces y eficientes.

> [!CAUTION]
> Recuerda que el contexto específico es muy importante a la hora de decidir si el sondeo (polling) o la gestión de interrupciones es la mejor solución para un sistema. No se trata de una elección simple en la que uno sea siempre mejor que el otro. Las interrupciones son ideales para eventos que ocurren de forma impredecible, mientras que el sondeo es más adecuado para eventos regulares y predecibles. Asegúrate de comprender bien la diferencia para poder elegir el método correcto en cada situación.

### Escenarios del mundo real

#### Ratón y teclado

Cuando un usuario mueve el ratón o pulsa una tecla, estos dispositivos generan señales de interrupción que hacen que la CPU pause inmediatamente sus tareas actuales y ejecute la rutina de servicio de interrupción (ISR) correspondiente. Esto garantiza que las entradas del usuario se procesen en tiempo real, proporcionando una respuesta inmediata y una interacción fluida. Por ejemplo, al escribir, cada pulsación de tecla genera una interrupción que el sistema operativo gestiona de forma inmediata, asegurando que los caracteres aparezcan en pantalla sin retrasos.

Por el contrario, usar sondeo para estos dispositivos obligaría a la CPU a comprobar continuamente el estado del ratón y el teclado, lo que provocaría una sobrecarga innecesaria de procesamiento y un mayor consumo de energía, especialmente en dispositivos alimentados por batería como los portátiles. Además, el sondeo podría generar respuestas más lentas si la CPU está ocupada con otras tareas cuando se produce una entrada del usuario.

En sistemas embebidos básicos, como terminales sencillos de introducción de datos o quioscos, donde la interacción del usuario es poco frecuente y el sistema permanece mayoritariamente inactivo, el sondeo puede ser suficiente. Comprobar periódicamente la entrada del usuario simplifica el diseño del sistema y evita la sobrecarga asociada a la gestión de interrupciones. Esto es aceptable en entornos de baja actividad donde una respuesta inmediata no es crítica.

#### Comunicaciones de red

Cuando llegan paquetes de datos a una tarjeta de red (NIC), se generan interrupciones que avisan a la CPU para procesar inmediatamente los datos entrantes. Esta gestión rápida garantiza que los datos se reciban, procesen y entreguen a la aplicación correspondiente con eficiencia, manteniendo un buen rendimiento de red. Por ejemplo, durante una videoconferencia, las interrupciones permiten procesar audio y vídeo en tiempo real, asegurando una latencia mínima y una comunicación de alta calidad.

Si se utilizara sondeo en las comunicaciones de red, la CPU tendría que comprobar continuamente la NIC en busca de nuevos datos, lo que aumentaría la sobrecarga de procesamiento y podría provocar la pérdida de paquetes si la CPU está ocupada con otras tareas. Esto daría lugar a retrasos, un peor rendimiento de red y un mayor consumo de energía, especialmente en dispositivos como smartphones o tabletas.

En escenarios donde el tráfico de red es mínimo y predecible, como en un sistema de monitorización remota que envía pequeños paquetes de datos de forma periódica, el sondeo puede resultar más eficiente. Comprobar la actividad de red a intervalos regulares reduce la complejidad de la gestión de interrupciones y es suficiente para cubrir necesidades de comunicación poco frecuentes y previsibles.

#### Operaciones de entrada/salida en disco

Cuando una unidad de disco completa una operación de lectura o escritura, genera una interrupción que avisa a la CPU para gestionar inmediatamente la transferencia de datos. Este enfoque permite que la CPU ejecute otras tareas mientras espera a que finalice la operación de disco, mejorando la eficiencia general del sistema. Por ejemplo, al guardar un archivo, la CPU puede continuar ejecutando otras aplicaciones hasta que el disco indique que la escritura ha terminado.

Si se utilizara sondeo para las operaciones de E/S de disco, la CPU tendría que comprobar continuamente el estado de la unidad, lo que supondría una sobrecarga considerable y una pérdida de eficiencia. Se desperdiciarían muchos ciclos de CPU en comprobaciones repetidas, especialmente durante operaciones largas, provocando un peor rendimiento del sistema y un mayor consumo de energía.

En sistemas donde el acceso al disco es predecible e infrecuente, como un registrador de datos (data logger) que escribe información en disco a intervalos fijos, el sondeo puede ser una opción adecuada. Comprobar la disponibilidad del disco antes de escrituras programadas simplifica la implementación y elimina la complejidad asociada a las interrupciones.

#### Sistemas embebidos

Los sistemas embebidos, como los utilizados en unidades de control de automóviles o en maquinaria industrial, a menudo necesitan responder rápidamente a señales de sensores y eventos externos. Por ejemplo, en un sistema de airbag de un vehículo, los sensores que detectan una colisión generan interrupciones que provocan el despliegue inmediato de los airbags. Esta respuesta rápida es crucial para la seguridad y la eficacia del sistema.

Usar sondeo en este tipo de escenarios obligaría a la CPU a comprobar constantemente el estado de los sensores, aumentando la sobrecarga de procesamiento y con el riesgo de no detectar eventos críticos si la CPU está ocupada con otras tareas. En aplicaciones sensibles al tiempo, este retraso podría tener consecuencias catastróficas.

En situaciones donde los eventos ocurren a intervalos regulares y predecibles, y la sobrecarga de las interrupciones no está justificada, el sondeo puede ser más adecuado. Por ejemplo, en un sistema de control climático de un edificio, los sensores de temperatura pueden comprobarse periódicamente para mantener condiciones constantes, haciendo del sondeo una opción ventajosa.

#### Sistemas en tiempo real

En los sistemas en tiempo real, la elección entre sondeo e interrupciones depende de los requisitos concretos de la aplicación. Aunque las interrupciones suelen preferirse por su rápida capacidad de respuesta, existen casos en los que el sondeo resulta más apropiado.

Por ejemplo, en un sistema en tiempo real que controla un robot industrial que realiza tareas repetitivas a intervalos fijos, el sondeo puede ser más predecible y fácil de gestionar. El robot puede comprobar sensores y ajustar actuadores en momentos precisos y regulares, asegurando una ejecución controlada de las tareas. En este caso, el sondeo simplifica el diseño y evita la sobrecarga asociada a cambios de contexto frecuentes provocados por interrupciones.

En cambio, en sistemas críticos como el despliegue de airbags en automóviles, la gestión de interrupciones es imprescindible. El sistema debe responder de inmediato a señales que indican una colisión. Cuando los sensores detectan una desaceleración brusca o un impacto, generan interrupciones que hacen que la CPU ejecute instantáneamente la rutina de despliegue del airbag. En este tipo de aplicaciones críticas, la capacidad de las interrupciones para proporcionar una respuesta inmediata y de alta prioridad las convierte en la opción preferente, ya que cualquier retraso podría tener consecuencias graves.
