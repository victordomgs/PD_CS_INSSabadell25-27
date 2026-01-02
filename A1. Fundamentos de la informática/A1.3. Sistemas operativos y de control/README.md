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
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2072.%20Windows%20File%20Explorer%20view.png" alt="Walden" width="250" height="auto"/>
    <p><em>Figura 49: Windows File Explorer. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2073.%20MacOS%20finder%20view.png" alt="Walden" width="250" height="auto"/>
    <p><em>Figura 50: MacOS finder view. Fuente: Computer Science for the IB Diploma 2025 (Baumgarten P.)</em></p>
  </div>

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A1.%20Fundamentos%20de%20la%20inform%C3%A1tica/images/Figura%2074.%20Los%20tipos%20de%20archivo%20m%C3%A1s%20comunes.png" alt="Walden" width="350" height="auto"/>
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
