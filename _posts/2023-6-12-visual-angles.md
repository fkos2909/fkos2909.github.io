---
layout: post
title: ÁNGULOS VISUALES, POSICIONAMIENTO Y FRECUENCIA DE SATELITES
abstract: Los ángulos visuales de una antena son una consideración importante en el diseño y la implementación de sistemas de comunicación inalámbricos, ya que pueden afectar significativamente al área de cobertura y a la eficacia de la señal transmitida.
---

# ÁNGULOS VISUALES DE UNA ANTENA

El ángulo visual es una medida del ángulo formado entre la línea de visión desde la antena a un punto concreto de la superficie terrestre. El ángulo visual se mide normalmente en grados y suele representarse en un diagrama polar o diagrama de campo polar. 

En general, cuanto **mayor es el ángulo visual** de una antena, **mayor es la zona de cobertura** de la señal transmitida. Sin embargo, una antena más direccional con un ángulo visual más estrecho puede proporcionar una mayor intensidad de señal recibida para transmisiones en una dirección concreta, lo que la hace más adecuada para comunicaciones punto a punto o aplicaciones muy focalizadas como receptores GPS o comunicación por satélite. 

Los ángulos visuales de una antena son una consideración importante en el diseño y la implementación de sistemas de comunicación inalámbricos, ya que pueden afectar significativamente al área de cobertura y a la eficacia de la señal transmitida. 

![Ángulos de visión]({{ site.baseurl }}/images/2023-6-12/ejemplo.png)

Para optimizar el funcionamiento de un sistema de comunicaciones por satélite, la dirección de ganancia máxima de una antena de estación terrestre se debe apuntar directamente al satélite. Para asegurar que esté alineada la antena de la estación terrestre, se deben determinar dos ángulos: el azimut, y la elevación. 

### Ángulo de elevación
El ángulo de elevación se refiere al ángulo formado entre la línea de visión desde la antena hasta un punto concreto de la superficie terrestre. El **ángulo de elevación** suele expresarse en grados y puede medirse desde el plano horizontal, que es el plano perpendicular a la superficie terrestre. 

![Ángulo de elevación]({{ site.baseurl }}/images/2023-6-12/elevacion.png)

El ángulo de elevación óptimo para un determinado sistema de comunicación depende de varios factores, como la altura de las antenas transmisora y receptora, la distancia entre las antenas y el terreno sobre el que se transmite la señal. 

Mientras menor es el ángulo de elevación, la distancia que debe recorrer una onda propagada a través de la atmósfera terrestre es mayor. Como en el caso de cualquier onda propagada por la atmósfera terrestre, sufre absorción, y también se puede contaminar mucho con ruido. En consecuencia, si el ángulo de elevación es muy pequeño y la distancia que la onda viaja por la atmósfera terrestre es demasiado grande, la onda se puede deteriorar hasta el grado de ya no proporcionar una calidad aceptable de transmisión. En general, se considera que 5° es el ángulo de elevación mínimo aceptable. 

### Ángulo de azimut
El ángulo acimutal se refiere al ángulo formado entre la línea de visión desde la antena hasta un punto concreto de la superficie terrestre, medido desde el norte en un mapa plano o una brújula. El **ángulo acimutal** suele expresarse en grados y puede medirse desde el este, que es 0 grados, en el sentido de las agujas del reloj hasta el norte, que es 90 grados. 

![Ángulo de azimut]({{ site.baseurl }}/images/2023-6-12/azimut.png)

### Límites de visibilidad
Los límites de visibilidad se refieren a la distancia máxima a la que se puede recibir una señal fiable, dadas las características de las antenas transmisora y receptora y el terreno por el que se transmite la señal. 

Para una estación terrestre en determinado local, la curvatura de la Tierra establece los límites de visibilidad, es decir, los límites de la línea de vista, que determina el máximo alejamiento del satélite que se puede ver en dirección este u oeste de la longitud de la estación. Teóricamente, se alcanza la distancia máxima de línea de vista cuando la antena de la estación terrestre apunta en el plano horizontal (0° de elevación). Sin embargo, en la práctica el ruido que se capta de la Tierra, y la atenuación de la señal por la atmósfera terrestre con 0° de elevación, son excesivos. Por consiguiente, se suele aceptar que 5° es el ángulo mínimo de elevación útil. Los límites de visibilidad dependen, en parte, de la elevación del satélite y de la latitud y longitud de la estación terrestre. 

# POSICIONAMIENTO Y FRECUENCIAS DE SATÉLITES

Las dos clasificaciones principales de los satélites de comunicaciones son giratorios y con estabilizador de tres ejes. Los ***satélites de comunicaciones giratorios**  aprovechan el momento angular de su masa giratoria para obtener estabilización de balanceo y cabeceo. 

![satélites de comunicaciones giratorios]({{ site.baseurl }}/images/2023-6-12/tiros.png)

**TIROS-7** era una nave espacial meteorológica estabilizada por rotación diseñada para probar técnicas experimentales de televisión y equipos de infrarrojos.

Los **satélites de comunicaciones con estabilizadores de tres ejes** son un tipo de satélite de comunicaciones que utiliza tres ejes mecánicos para estabilizar la posición y orientación del satélite en órbita. Los tres ejes suelen incluir un eje de cabeceo, un eje de guiñada y un eje de balanceo, que permiten al satélite mantener una actitud estable con respecto a la superficie terrestre. 

![satélites de comunicaciones con estabilizadores de tres ejes]({{ site.baseurl }}/images/2023-6-12/3ejes.png)

Los satélites geosíncronos deben **compartir un espacio y un espectro de frecuencias limitados**, dentro de determinado arco de órbita estacionaria. A cada satélite de comunicaciones se le asigna una longitud aproximada, en el arco geoestacionario, de 35888.371 km sobre el ecuador. La posición en el intervalo depende de la banda de frecuencias de comunicaciones que se use. Los satélites que trabajan la misma o casi la misma frecuencia deben tener una separación suficiente en el espacio para evitar interferir entre sí. Hay un límite realista de la cantidad de satélites que pueden estacionarse en determinada área del espacio. La **separación espacial requerida** depende de las siguientes variables: 

1. Anchos de banda y lóbulos laterales de radiación de las antenas, tanto de la estación terrestre como del satélite.
2. Frecuencia de portadora de RF.
3. Técnica de codificación que se use
4. Límites aceptables de interferencia.
5. Potencia de la portadora de transmisión.

En general, se requiere una separación espacial de 3° a 6°, que depende de estas variables. 

![Separación espacial]({{ site.baseurl }}/images/2023-6-12/separacion.png)

Las frecuencias de portadora más comunes que se usan en comunicaciones vía satélite son las bandas de 6/4 y de 14/12 GHz. El primer número es la frecuencia de enlace de subida (estación terrestre a transpondedor), y el segundo es la frecuencia de enlace de bajada (transpondedor a estación terrestre). Se usan frecuencias distintas de enlace de subida y de bajada para evitar que haya radiación de pérdida. 

La mayoría de los satélites domésticos usa la banda de 6/4 GHz. Desafortunadamente, esta banda también se usa mucho en sistemas terrestres de microondas. Se debe tener cuidado al diseñar una red satelital, para evitar interferencias con otros enlaces existentes de microondas. Algunas posiciones de órbita geosíncrona tienen mayor demanda que otras. 

# STARLINK
Los satélites **Starlink** son una red de satélites diseñados y operados por **SpaceX**, una empresa aeroespacial privada. La red está diseñada para proporcionar cobertura mundial de banda ancha y rápidas velocidades de internet a zonas rurales y de difícil acceso. 

![Starlink]({{ site.baseurl }}/images/2023-6-12/logo.png)

El sistema Starlink consta de *miles de pequeños* satélites en órbita terrestre baja (LEO) que se lanzan al espacio en cohetes Falcon 9 de SpaceX. Los satélites trabajan juntos en una red mallada que permite la transferencia de datos a alta velocidad entre ellos. 

![Red Starlink]({{ site.baseurl }}/images/2023-6-12/starlink1.png)

El principal objetivo de la red Starlink es proporcionar acceso a Internet a zonas desatendidas que no disponen de una buena conexión con redes terrestres. El bajo coste y la facilidad de despliegue de los satélites Starlink la convierten en una opción atractiva para comunidades rurales y países en desarrollo. 

La red Starlink ya han llegado más de **2.000** satélites a sus órbitas de **550** kilómetros, y en los próximos años se añadirán otros **2.400** a esta constelación de primera generación (GEN-1). Además, la Comisión Federal de Comunicaciones de EE.UU. (FCC) ya ha dado a SpaceX su aprobación para la constelación de **40.000** satélites de la Generación 2 (GEN-2), que se completará en **2027**. La constelación final de *10.000 millones* de dólares generará más de *30.000* millones anuales por suscripciones y ventas de hardware. 

![Red Starlink]({{ site.baseurl }}/images/2023-6-12/red.png)

La red Starlink ha sido recibida con **elogios y críticas** por su posible impacto en el medio ambiente y la astronomía. Por ejemplo, la situación de los satélites de la NASA. Un simple cálculo matemático indica que *4.000 satélites de Gen-1* repartidos en una envoltura con un radio de *550 km*conducen a una distancia media entre satélites de unos **400 km**. Para la constelación Gen-2, esta distancia es de sólo unos **120 km**. En febrero de 2022, la NASA y la National Science Foundation enviaron cartas a la Comisión Federal de Comunicaciones (FCC) advirtiendo de que la constelación Gen-2 aumenta drásticamente el **riesgo de colisión de naves espaciales y satélites LEO**.	

La regulación de las órbitas y frecuencias de los satélites artificiales es extremadamente importante por varias razones:

Primeramente, evitar el **síndrome de Kessler**, el cual es un escenario hipotético donde el número de objetos en órbita terrestre baja (LEO) es tan elevado que las colisiones entre objetos podrían crear una cascada de desechos, dificultando o incluso imposibilitando la realización de actividades en LEO. Para evitarlo, es importante una normativa que controle el número y la colocación de los satélites en LEO y minimice el riesgo de colisiones. 

Siguiendo esta idea, es importante limitar el riesgo de colisión entre satélites y otros objetos en el espacio es real, y la normativa es importante para limitar el riesgo de catástrofes. La **Oficina de Asuntos del Espacio Ultraterrestre de Naciones Unidas** ha publicado unas directrices para la sostenibilidad a largo plazo de las actividades espaciales, que incluyen principios para las actividades espaciales responsables y la prevención de interferencias perjudiciales.

Así mismo, ayuda a el uso eficiente de las frecuencias, la comunicación por satélite y otras actividades en el espacio debe supervisarse y regularse para evitar interferencias entre distintos sistemas. La **Unión Internacional de Telecomunicaciones (UIT)** es la encargada de asignar bandas de frecuencias a los diferentes servicios para garantizar un uso eficiente del espectro radioeléctrico. 

Por otro lado, es importante recordar la protección de la astronomía, el número de satélites artificiales en órbita ha crecido rápidamente en los últimos años, lo que puede afectar a la capacidad de los astrónomos para observar el universo. La reglamentación puede ayudar a minimizar el impacto de los satélites en la astronomía, garantizando que se diseñen y operen de forma que se reduzca al mínimo su impacto en las observaciones científicas. 

![Red Starlink]({{ site.baseurl }}/images/2023-6-12/luces.png)

*Los satélites Starlink pueden parecer un tren de luz*

La regulación de las órbitas y frecuencias de los satélites artificiales es crucial para garantizar el desarrollo seguro y sostenible de las actividades en el espacio. Sin una regulación adecuada, el riesgo de colisión e interferencia entre distintos sistemas sería demasiado alto, así como el impacto sobre la astronomía y otras actividades científicas. 

























