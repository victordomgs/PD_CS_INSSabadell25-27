<h1 align="center">A2.4. Seguridad de la red
<div align="center">

</div>

## Contenido:

- [A2.4.1 Discuta la eficacia de los cortafuegos para proteger una red](#A241-discuta-la-eficacia-de-los-cortafuegos-para-proteger-una-red)  
- [A2.4.4 Describir el proceso de cifrado y los certificados digitales](#A244-describir-el-proceso-de-cifrado-y-los-certificados-digitales)

<br>

## A2.4.1 Discuta la eficacia de los cortafuegos para proteger una red

Los **cortafuegos (firewalls)** desempeñan un papel clave en la protección de las redes informáticas, pero ¿qué hacen exactamente?

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2019.jpg" alt="Redes" width="650" height="auto"/>
    <p><em>Figura 19: Funcionamiento Firewall. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

Un firewall inspecciona los paquetes IP que pasan a través de él y filtra el tráfico entrante y saliente basándose en un conjunto de reglas de seguridad predefinidas. En la ilustración anterior, la Regla 1 permite que el tráfico procedente del PC2 en la LAN interna acceda a cualquier dirección IP externa que comience por 185.?.?.? en los puertos de destino 80 o 443. A continuación, la Regla 2 bloquea todas las demás solicitudes internas. Cada paquete individual se comprueba contra las reglas hasta que se encuentra una regla que permite o deniega el paso a través del firewall.

Algunos firewalls también son capaces de aplicar inspección con estado (stateful inspection), en la que se supervisa el estado de las conexiones activas y se utiliza esta información para determinar el paso del tráfico a través del firewall. Por ejemplo, una vez que se permite establecer una conexión, los paquetes pueden circular de ida y vuelta por esa conexión hasta que se cierre.

Las reglas se componen de un conjunto de listas de permiso (allow lists) y listas de denegación (deny lists). Estas listas contienen direcciones IP o rangos de direcciones IP y, opcionalmente, también pueden especificar números de puerto de aplicaciones.

Mediante estas listas de reglas, los firewalls controlan el acceso a la red interna desde fuentes externas y también pueden utilizarse para controlar qué destinos externos son accesibles desde el interior de la red. Además, los firewalls registran las solicitudes de tráfico, lo que puede resultar útil para detectar y responder a actividades sospechosas o para identificar una posible brecha de seguridad.

Los firewalls son solo una de las herramientas para asegurar una red y no son perfectos para proteger contra todos los tipos de ataques. Por ejemplo, son menos eficaces frente a amenazas internas, como un empleado malintencionado, o cuando una amenaza externa ha conseguido presencia local en la red mediante una conexión WiFi comprometida. Algunas amenazas pueden ser muy sofisticadas y llegar a imitar tráfico legítimo. Por último, un firewall es tan bueno como su configuración: si un administrador de red no mantiene actualizadas las listas de bloqueo y el firmware del firewall, pueden quedar expuestas vulnerabilidades.

### Traducción de direcciones de red (NAT)

Anteriormente se te presentó el concepto de traducción de direcciones de red en la Sección A2.3.1.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2020.jpg" alt="Redes" width="650" height="auto"/>
    <p><em>Figura 20: Network address translation. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>
  
Más allá de la comodidad que ha proporcionado NAT al permitir que Internet siga funcionando a pesar de que las direcciones IPv4 se agotaron prácticamente hace años, también ha aportado un beneficio adicional en términos de seguridad de red.

Dado que NAT modifica la información de direcciones IP en las cabeceras de los paquetes, este proceso ayuda a ocultar las direcciones IP internas de una red, lo que dificulta que un atacante externo pueda acceder directamente a los sistemas internos. Aunque técnicamente no fue diseñado como una función de seguridad, sí añade una capa extra de dificultad que los atacantes deben superar, ya que la estructura interna de la red y sus direcciones IP no quedan expuestas directamente. En este sentido, puede describirse como un caso de seguridad por ocultación (security by obscurity).

## A2.4.4 Describir el proceso de cifrado y los certificados digitales

### Cifrado simétrico

El cifrado simétrico es aquel en el que se utiliza la misma clave tanto para cifrar como para descifrar los datos. Esto significa que la clave debe compartirse entre el emisor y el receptor de forma segura.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2021.jpg" alt="Redes" width="550" height="auto"/>
    <p><em>Figura 21: Cifrado simétrico. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

> [!IMPORTANT]
> **Clave de cifrado:** una cadena de caracteres o números utilizada por un algoritmo de cifrado para codificar o decodificar datos. Son los valores que se introducen en las funciones matemáticas responsables de mezclar o desmezclar los datos.

El cifrado simétrico suele ser más rápido y menos exigente desde el punto de vista computacional que su equivalente asimétrico, por lo que resulta adecuado para cifrar archivos de gran tamaño.

Cuando existe una gran distancia física entre el emisor y el receptor, puede resultar difícil compartir la clave de cifrado de una manera que esté protegida frente a escuchas no autorizadas. Existen dos soluciones comunes a este problema:

- Utilizar cifrado asimétrico para establecer comunicaciones seguras. Emplear este método asimétrico para intercambiar y acordar una clave simétrica, y luego cambiar la comunicación al método simétrico, que es más rápido y eficiente.
- Utilizar un método matemáticamente seguro para intercambiar claves, como Diffie-Hellman (que se tratará más adelante en esta sección).

### Cifrado asimétrico

El cifrado asimétrico es aquel en el que la clave de seguridad utilizada para cifrar los datos es diferente de la clave utilizada para descifrarlos. Si funciona correctamente, ofrece ventajas significativas, ya que dos partes que desean comunicarse de forma cifrada no necesitan reunirse en privado para intercambiar una clave de cifrado acordada previamente, como ocurre en el cifrado simétrico. En su lugar, la clave de cifrado puede publicarse de forma pública, y cualquier persona que quiera enviar un mensaje puede usarla para cifrar los datos, de modo que solo el destinatario, que posee la clave privada correspondiente, pueda descifrarlos y leerlos.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2022.jpg" alt="Redes" width="550" height="auto"/>
    <p><em>Figura 22: Cifrado asimétrico. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

Por ejemplo: si Alicia quiere enviar un mensaje seguro a Bob, lo cifra utilizando la clave pública de Bob. Solo Bob puede descifrar este mensaje utilizando su clave privada.

### Función de los certificados digitales

Los **certificados digitales** se utilizan como un medio para certificar identidades en Internet. En el tráfico HTTPS, son emitidos por una tercera parte de confianza mutua conocida como autoridad certificadora (CA, Certificate Authority).

Cuando se presenta un certificado digital en una transacción de red, ayuda al receptor a verificar que la clave pública pertenece realmente al emisor y no a un impostor. Los certificados digitales forman una parte clave de la red de confianza en Internet. No basta con saber que tu comunicación con yourbank.com está cifrada si cualquier persona puede hacerse pasar por el servidor legítimo de yourbank.com. Lo que realmente quieres es saber que el servidor web en el que inicias sesión es aquel con el que deseas compartir tu información confidencial.

### Obtención de un certificado

El proceso comienza cuando yourbank.com solicita a una autoridad certificadora (que sea de confianza para ambas partes) la emisión de un certificado que pueda utilizarse para demostrar que, efectivamente, es el servidor legítimo de yourbank.com.

El banco genera una clave pública y una clave privada utilizando un proceso similar al descrito anteriormente con el algoritmo RSA. La clave privada se mantiene segura en el servidor del banco, mientras que la clave pública se envía a la autoridad certificadora junto con la solicitud de certificación.

Utilizando la clave pública proporcionada en la solicitud, la CA verifica la identidad y legitimidad del banco. Este proceso varía según la autoridad certificadora. En los primeros días de Internet, era necesario enviar documentos como identificaciones oficiales, certificados de propiedad empresarial y otros documentos legales. Las prácticas modernas han simplificado enormemente este proceso para fomentar una adopción más amplia de HTTPS, y hoy en día autoridades certificadoras como letsencrypt.org ofrecen este servicio de forma gratuita y sin trámites complejos.

Una vez que la CA está satisfecha con la verificación, utiliza su clave privada para firmar la clave pública del banco u otro sitio web. Este proceso de firma implica crear un hash del certificado, que luego se cifra utilizando la clave privada de la CA. Este hash cifrado se convierte en la firma electrónica. No puede generarse sin la clave privada de la CA, pero sí puede validarse utilizando la clave pública de la CA.

### Uso de certificados digitales

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2023.jpg" alt="Redes" width="550" height="auto"/>
    <p><em>Figura 23: Firmar con un certificado digital. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>
  
#### Firma con un certificado digital

Una vez emitido, el certificado digital puede adjuntarse a todas las comunicaciones del banco u otra organización y utilizarse para firmar criptográficamente dichas comunicaciones. Esto proporciona un mecanismo que permite a los receptores verificar algorítmicamente la autenticidad del origen de la comunicación.

Los certificados digitales también pueden generarse de forma autónoma para crear claves públicas y privadas que se utilizan para el inicio de sesión seguro en servicios de red, como por ejemplo mediante SSH (Secure Shell). En este caso, tu clave pública se carga en la máquina remota en la que deseas autenticarte posteriormente, y mantienes tu clave privada de forma segura en tu equipo local. La clave privada equivale a tu contraseña. Cuando deseas iniciar sesión mediante SSH, el servidor genera un desafío cifrado con la clave pública. Tú, como único poseedor de la clave privada, eres la única persona capaz de descifrar ese desafío y, de este modo, demostrar tu identidad.

Dada la importancia crucial de las claves criptográficas en la economía digital moderna e interconectada, el almacenamiento adecuado de las claves es esencial. Si alguien obtiene acceso no autorizado a las claves privadas de una organización, puede hacerse pasar por dicha organización en todas las transacciones electrónicas para las que esas claves estén configuradas. Por ello, la creación, distribución, uso, almacenamiento y eventual retirada y eliminación de las claves de cifrado constituyen una tarea fundamental de cualquier infraestructura informática eficaz.

Los certificados digitales también son una parte esencial de las tecnologías blockchain, como las criptomonedas. Todas las transacciones en una cadena de bloques están tanto firmadas como sometidas a funciones hash. Los emisores utilizan sus claves privadas para firmar digitalmente las transacciones como parte del proceso de validación que demuestra que son los propietarios de las criptomonedas que están gastando. Esta firma sirve para autenticar la identidad del emisor y garantizar la no repudio de la transacción, es decir, el emisor no puede negar posteriormente haber realizado dicha transacción.

  <div style="text-align: center;">
    <img src="https://github.com/victordomgs/PD_CS_INSSabadell25-27/blob/main/A2.%20Redes/images/Figura%2024.jpg" alt="Redes" width="550" height="auto"/>
    <p><em>Figura 24: Bob y Alice. Fuente: Computer Science IB. (Paul Baumgarten, Ioana Ganea, Carl Turland)</em></p>
  </div>

### Intercambio de claves Diffie-Hellman

Dado que los algoritmos de cifrado asimétrico requieren un procesamiento significativamente mayor que los algoritmos simétricos, resulta ideal que las sesiones de comunicación largas utilicen cifrado simétrico. El problema evidente que surge entonces es encontrar un método seguro para intercambiar y acordar la clave simétrica. Aunque podría utilizarse cifrado asimétrico para este propósito, este enfoque es más lento y consume más recursos de procesamiento. Una alternativa ampliamente utilizada es el intercambio de claves Diffie-Hellman.

La analogía utilizada para describir Diffie-Hellman es la dificultad de separar colores de pintura ya mezclados. Aunque podemos tener una idea aproximada de qué colores podrían haberse utilizado para obtener el color marrón, resulta prácticamente imposible descomponer exactamente los colores originales.

Desde una perspectiva algorítmica, Diffie-Hellman se basa en los mismos principios que el cifrado asimétrico en lo que respecta al uso de números primos y a la dificultad matemática de determinar los factores primos de un número una vez que se ha aplicado una operación módulo.
