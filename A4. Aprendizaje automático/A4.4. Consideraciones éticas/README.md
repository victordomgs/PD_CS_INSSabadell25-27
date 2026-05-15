<h1 align="center">A4.2. Consideraciones éticas
<div align="center">

</div>

## Contenido:

- [A4.4.1 Implicaciones éticas](#A441-implicaciones-éticas)
- [A4.4.2 Reevaluación de la ética a medida que las tecnologías se integran más](#A442-reevaluación-de-la-ética-a-medida-que-las-tecnologías-se-integran-más)


## A4.4.1 Implicaciones éticas

### TOK (Teoría del Conocimiento)
¿Todo conocimiento impone obligaciones éticas a quienes lo poseen?

Debata sobre el uso ético del aprendizaje automático (machine learning), especialmente en áreas sensibles como la vigilancia o la toma de decisiones.

En la vigilancia (como el reconocimiento facial), abundan las preocupaciones sobre la privacidad, el consentimiento y los sesgos de vigilancia. Los sistemas de vigilancia pueden utilizarse para monitorear, controlar y, a veces, discriminar a las poblaciones.

Con la participación del aprendizaje automático en la toma de decisiones —como en la contratación, la concesión de préstamos y la aplicación de la ley—, estos sistemas pueden influir significativamente en la vida de las personas, y se ha demostrado que heredan y amplifican los sesgos presentes en los datos de entrenamiento.

Los modelos de aprendizaje automático —sistemas inherentemente impulsados por el conocimiento— se basan en datos que encapsulan diversas formas de conocimiento, desde el comportamiento humano hasta patrones biológicos. Como creadores y usuarios de estos sistemas, existe la responsabilidad de garantizar que este conocimiento se utilice de manera ética.

El mundo está cambiando rápidamente. Los avances tecnológicos, incluidos los del aprendizaje automático, plantean desafíos y preguntas importantes para nosotros como sociedad. Es importante tomarse un tiempo para sopesar estas cuestiones éticas y no dejarse llevar por la "brillante nueva tecnología" sin reflexionar detenidamente sobre cómo nos afectará a nosotros y a quienes nos rodean.

A continuación se presentan algunos de los problemas éticos a considerar:

- **Responsabilidad (Accountability):** ¿En quién o en dónde recae la responsabilidad de las decisiones tomadas por los sistemas de aprendizaje automático? ¿Es de la empresa que produjo la IA o de las personas que la utilizan? ¿Es una mezcla de ambas? ¿Es posible determinar cómo y por qué un sistema de aprendizaje automático tomó una decisión en particular?

  Un incidente que resalta el problema de la responsabilidad involucró a un automóvil autónomo. El conductor que estaba al volante de un coche autónomo cuando este atropelló y mató a un peatón en 2018 se declaró culpable de imprudencia temeraria y fue sentenciado a tres años de libertad condicional supervisada.

- **Equidad algorítmica y sesgo (Algorithmic fairness and bias):** El aprendizaje automático puede perpetuar los sesgos sociales existentes si estos se encuentran en los datos de entrenamiento, o si el diseño del modelo favorece, a sabiendas o no, a ciertos grupos. La equidad requiere identificar y mitigar activamente el sesgo en el conjunto de datos y en los algoritmos.
  
  COMPAS es un algoritmo de reincidencia utilizado por muchos sistemas judiciales de EE. UU. Se descubrió que presentaba un sesgo racial, ya que predecía un mayor riesgo de reincidencia para las personas negras y un menor riesgo para las personas blancas.
  
  Otro ejemplo es que, en 2018, Amazon descartó una herramienta "secreta" de contratación por IA que estaba sesgada contra las mujeres.
  
  Por último, las IA generativas se enfrentan al desafío constante de reforzar y exacerbar los estereotipos y los sesgos.

- **Consentimiento (Consent):** Los grandes conjuntos de datos utilizados para el entrenamiento suelen contener información recopilada sin el consentimiento explícito. Muchas grandes empresas están aplicando el aprendizaje automático en sus bases de datos de clientes o vendiendo los datos de estos a otras empresas de emparejamiento de datos (data-matching). ¿Cuánto control deberían conservar las personas sobre su información personal?
  
  Se determinó que DeepMind de Google infringió las leyes de privacidad del Reino Unido tras no informar adecuadamente a los pacientes sobre el uso de sus datos de salud de identificación personal en el desarrollo de una aplicación para detectar lesiones renales.

- **Impacto ambiental (Environmental impact):** Los modelos de aprendizaje automático requieren una enorme potencia de cálculo, especialmente en la fase de entrenamiento. Esto conlleva un consumo sustancial de energía e implicaciones en las emisiones de carbono.

Científicos de la Universidad de Cornell descubrieron que el entrenamiento de LLM (grandes modelos de lenguaje) como GPT-3 consumía una cantidad de electricidad equivalente a 500 toneladas métricas de carbono. De hecho, DatacenterDynamics informa que el uso global de energía por parte de los centros de datos se duplicará con creces, pasando de 460 TWh en 2022 a más de 1000 TWh en 2026.

- **Privacidad (Privacy):** Los sistemas de aprendizaje automático pueden predecir o clasificar el comportamiento personal de formas que invaden la privacidad. La capacidad de estos sistemas para aplicar la inferencia significa que la privacidad puede verse aún más comprometida si el sistema deduce condiciones de salud que ni siquiera se le proporcionaron al modelo.

En 2018, la aplicación de seguimiento de actividad física Strava publicó un mapa de calor global de las actividades de los usuarios que, sin darse cuenta, reveló la ubicación de bases militares secretas y rutas de patrullaje, lo que evidenció una filtración significativa de privacidad.

- **Seguridad (Security):** Los sistemas de aprendizaje automático pueden ser vulnerables a ataques por diversos medios. Tres ataques comunes incluyen:

1. **Envenenamiento de datos (data poisoning):** consiste en introducir datos falsos o dañinos en el conjunto de datos de entrenamiento para manipular el modelo con fines maliciosos.

2. **Evasión del modelo (model evasion):** donde se utilizan entradas (como prompts o instrucciones) para "engañar" al modelo y hacer que genere respuestas incorrectas en contra de su entrenamiento (a veces conocido como "jailbreaking" o desbloqueo, en el contexto de la IA generativa).

3. **Inversión del modelo (model inversion):** se refiere a obtener acceso a datos sensibles contenidos dentro de los datos de entrenamiento.

A las 24 horas de su lanzamiento, el bot de Twitter Tay de Microsoft fue manipulado mediante datos de entrada maliciosos para producir tuits sumamente inapropiados y ofensivos.

Cuando OpenAI lanzó GPT-3 por primera vez, este carecía de muchos de los filtros actuales y resultaba sumamente sencillo diseñar prompts que generaran contenido obsceno, tóxico o ilegal.

- **Impacto social (Societal impact):** El aprendizaje automático altera cada vez más los mercados laborales e influye en la opinión pública. Existe un delicado equilibrio entre el avance tecnológico y el mantenimiento del bienestar social que debe ser considerado.

Clearview AI, que recopila miles de millones de fotos de internet para el reconocimiento facial, ha despertado la preocupación de la sociedad sobre la vigilancia, el consentimiento y las libertades civiles.

- **Transparencia (Transparency):** La mayoría de los ingenieros no pueden explicar cómo generan sus sistemas los resultados que crean, especialmente aquellos que utilizan redes neuronales. Lo mejor que se puede hacer es señalar los datos de entrenamiento en lugar del algoritmo en sí. Esta falta de transparencia, o de comprensibilidad humana sobre qué son estos algoritmos y cómo funcionan, plantea interrogantes importantes.

En 2019, el empresario tecnológico David Heinmeier Hansson escribió en X (antes Twitter) que Apple Card le ofrecía un límite de crédito 20 veces superior al de su esposa, a pesar de que tienen activos compartidos y ella tiene una puntuación crediticia más alta, lo que generó dudas sobre la transparencia de los algoritmos utilizados para la toma de decisiones financieras.

- **Sesgo en los datos de entrenamiento (Bias in training data):** El sesgo en los datos de entrenamiento es un desafío fundamental para el aprendizaje automático. La sobre- o subrepresentación de grupos demográficos específicos afectará a las predicciones y a la fiabilidad del modelo. Se requieren métodos rigurosos de recopilación, procesamiento y evaluación de datos para garantizar una representación amplia y justa.

- **Desinformación (Misinformation):** El aprendizaje automático puede generar y difundir información falsa con facilidad, lo que dificulta enormemente garantizar una comunicación en línea precisa y fiable. A medida que la IA generativa, en particular, se vuelve cada vez más realista y convincente en sus resultados, será casi imposible evitar ser víctima de noticias falsas (fake news), imágenes falsas y vídeos falsos.

Se cree que la desinformación en Facebook recibió seis veces más clics que las noticias reales durante las elecciones de EE. UU. de 2020, según un estudio de la Universidad de Nueva York (NYU).

A medida que los deepfakes de IA generativa se convierten en armas del debate político, la confusión sobre qué creer solo planteará desafíos más complejos en el futuro.

- **Sesgo en la comunicación en línea (Bias in online communication):** Los sistemas de recomendación basados en aprendizaje automático están diseñados para maximizar la participación del usuario (engagement) en una plataforma. Un método para lograrlo es recomendar una mayor cantidad del mismo tipo de contenido con el que los usuarios han interactuado previamente. Esto puede crear "cámaras de eco" que refuerzan las creencias existentes y minimizan los puntos de vista alternativos.

Tanto los algoritmos de la sección de noticias (newsfeed) de Facebook como los sistemas de recomendación de YouTube han sido criticados por crear burbujas de filtro y cámaras de eco, donde se muestra a los usuarios principalmente contenido que se alinea con sus creencias actuales, polarizando potencialmente la opinión pública.

- **Acoso en línea (Online harassment):** El aprendizaje automático puede utilizarse para automatizar el acoso a gran escala. Los bots pueden trollear y dirigirse a individuos o grupos con facilidad, y cada vez pueden hacer que parezca más real que los ataques provienen de personas. La IA generativa se está utilizando para crear deepfakes de forma hiriente y abusiva, un ritmo que a las autoridades les cuesta seguir.

 **Privacidad y anonimato en las comunicaciones en línea (Privacy and anonymity in online communications):** Los usuarios a menudo no son conscientes o no entienden completamente cómo los algoritmos de aprendizaje automático utilizan y procesan sus datos. Los usuarios pueden pensar que sus acciones son anónimas, pero cada vez más los algoritmos de aprendizaje automático pueden realizar la desanonimización con un alto grado de fiabilidad. Existe muy poca conciencia de esto en la comunidad en general.

En 2006, Netflix publicó un conjunto de datos que contenía 100 millones de calificaciones de películas de 500.000 suscriptores, destinado a ser utilizado en un concurso global para mejorar la precisión del algoritmo de recomendación de Netflix. Supuestamente, los datos se habían anonimizado eliminando cualquier información de identificación personal. Investigadores de la Universidad de Texas en Austin demostraron que era posible volver a identificar a los usuarios comparando los datos anonimizados de Netflix con las calificaciones de películas disponibles públicamente en Internet Movie Database (IMDb). Utilizando solo una pequeña cantidad de información adicional sobre las preferencias de un individuo, los investigadores pudieron identificar hábitos de visualización personales e información potencialmente sensible.

<br>

## A4.4.2 Reevaluación de la ética a medida que las tecnologías se integran más

A medida que la inteligencia artificial y otras tecnologías sigan avanzando y evolucionando en los próximos años, la sociedad necesitará reevaluar periódicamente las implicaciones desde un punto de vista ético. Son muchos los desafíos que nos aguardan; la siguiente lista es solo un punto de partida para el debate:

- **Computación cuántica (Quantum computing):** La computación cuántica podría romper potencialmente muchos de los sistemas criptográficos que actualmente aseguran las comunicaciones digitales y las criptomonedas. El desarrollo de la criptografía resistente a la cuántica es un área de investigación importante a la que se le debe dar prioridad.

- **Realidad aumentada (Augmented reality - AR):** La realidad aumentada puede recopilar enormes cantidades de datos personales sobre el entorno de los usuarios. Además, ¿cuál es la ética en torno a alterar la percepción de la realidad de una persona? ¿Les desconecta esto de la sociedad de la que forman parte, provocando una pérdida de empatía?

- **Realidad virtual (Virtual reality - VR):** A medida que la realidad virtual se vuelve más realista, ¿cuáles son las preocupaciones de salud mental para quienes utilizan estos sistemas de forma excesiva o como evasión? ¿Cuáles deberían ser los límites cuando se trata de utilizar la realidad virtual para acceder a material violento o explícito?

- **IA omnipresente (Pervasive AI):** ¿Cómo nos protegemos de la vigilancia intrusiva y de la recopilación aparentemente interminable de nuestros datos personales para su uso en conjuntos de datos de aprendizaje automático?

- **Privacidad (Privacy):** ¿A quién pertenecen los datos sobre ti? ¿A ti o a la empresa que los recopiló? A medida que la recopilación de datos se vuelve más compleja, ¿habrá una tendencia hacia un consentimiento más transparente e informado sobre lo que ocurre con nuestra información personal?

- **Equidad (Equity):** ¿Cómo podemos garantizar que los avances tecnológicos reduzcan, en lugar de magnificar, la brecha en el acceso equitativo a la tecnología entre los diferentes grupos socioeconómicos, raciales, de género, sociales y geográficos?

> [!TIP]
> Esta sección ha compartido casos de estudio de la vida real sobre el impacto de muchas de las cuestiones éticas planteadas por este tema. Familiarízate con casos de estudio a los que puedas hacer referencia en tus respuestas del examen. Si puedes debatir con especificidad una situación relevante que haya ocurrido, esto ayudará mucho a demostrar que te importa el tema.

> [!ERROR]
> Los estudiantes cometen una serie de errores habituales al abordar preguntas relacionadas con la ética, lo que se extiende al debate sobre el aprendizaje automático:
> - **No simplifiques demasiado los problemas.** Evita reducir cuestiones éticas complejas a respuestas simples de "correcto" o "incorrecto". Las implicaciones éticas del aprendizaje automático tienen muchos matices y a menudo implican consideraciones interconectadas de responsabilidad, equidad e impacto social.
> - **No confundas el sesgo técnico con el sesgo ético.** Distingue entre el sesgo técnico (desviación en un algoritmo que conduce a predicciones menos precisas) y el sesgo ético o social (prejuicios en los datos que conducen a resultados injustos para ciertos grupos).
> - **No limites tus respuestas a cuestiones de privacidad y seguridad.** Considera una gama más amplia de problemas éticos, como el impacto ambiental, los cambios sociales y las implicaciones para la salud mental. Demuestra que tienes una comprensión profunda de las complejidades implicadas, en lugar de tomar el camino fácil de recurrir a una respuesta de examen que hable de la privacidad o la seguridad de forma superficial.
> - **No descuides la importancia de la reevaluación.** Las directrices éticas nunca pueden ser estáticas, ya que la tecnología y su impacto en la sociedad tampoco lo son.
