---
layout: post
title: HUELLAS, MODELOS DE ENLACE Y PARÁMETROS DE SISTEMAS SATELITALES
abstract: La representación geográfica del patrón de radiación de la antena de un satélite se llama huella, o a veces mapa de huella. En esencia, una huella de un satélite es la zona, sobre la superficie terrestre, desde donde el satélite puede recibir o hacia donde puede transmitir.
---

# PATRON DE RADIACIÓN DE ANTENAS SATELITALES: HUELLAS

La representación geográfica del patrón de radiación de la antena de un satélite se llama **huella**, o a veces **mapa de huella**. En esencia, una huella de un satélite es la zona, sobre la superficie terrestre, desde donde el satélite puede recibir o hacia donde puede transmitir. La forma de la huella de un satélite depende de su trayectoria orbital, su altura y el tipo de antena que se use. Mientras más alto esté el satélite, podrá abarcar más superficie terrestre.

![Representación geográfica del patrón de radiación de la antena de un satélite]({{ site.baseurl }}/images/2023-6-13/huella.png)

Las antenas satelitales de enlace de bajada (o downlink, término utilizado para representar el enlace entre un satélite y la Tierra) emiten señales en frecuencias de microondas, hacia una región geográfica seleccionada, dentro de la línea de vista del satélite. **La potencia efectiva transmitida se llama potencia irradiada efectiva isotrópica** (**EIRP**, de effective isotropic radiated power) y se expresa, en general, en dBm o dBW. Se traza un mapa de huella dibujando líneas continuas entre todos los puntos que tengan EIRP iguales. Un mapa característico de huella es, en esencia, una serie de curvas de nivel sobre un mapa geográfico de la región servida. Podría haber distintos mapas de huella para cada haz de radiación de cada satélite de comunicaciones. 

Los satélites, como el **DBS-1** (de emisión directa) estadounidense han empleado antenas más complicadas de conformación de haz, en el enlace de bajada, que permiten a los diseñadores configurar las huellas para llegar sólo a áreas específicas y, así no desperdician potencia en áreas no planeadas. 

![DirecTV 1, 2, 3]({{ site.baseurl }}/images/2023-6-13/dbs1.png)

Es posible diseñar antenas satelitales de enlace de bajada que puedan difundir señales de microondas para cubrir áreas sobre la Tierra cuyo tamaño va desde ciudades extremadamente pequeñas hasta a un 40% de la superficie terrestre. El tamaño, forma y orientación de estas antenas, y la potencia generada por cada transpondedor, determinan la cobertura geográfica y los EIRP. Las distribuciones de radiación de una antena satelital se suelen caracterizar como localizados, zonales, hemisféricas o globales. 

### Haces locales y zonales
Los haces más pequeños son los haces localizados, y les siguen los haces zonales. Los localizados concentran su potencia en áreas geográficas muy pequeñas y, en consecuencia, suelen tener. EIRP mayores que los que abarcan áreas mucho mayores, porque determinada potencia de salida se puede concentrar más. Los haces localizados y los zonales cubren menos del **10% de la superficie terrestre**. Mientras mayor sea la frecuencia del enlace de bajada, un haz puede ser enfocado con más facilidad hacia una zona más pequeña. 

### Haces hemisféricos
El haz hemisférico concentra su potencia sobre una amplia región intentando cubrir por ejemplo toda América o Africa. Estas abarcan en forma característica hasta el **20% de la superficie terrestre** y, por consiguiente, tienen EIRP 3 dB o 50% menores que las transmitidas por haces localizados que abarcan el 10% de la superficie terrestre. 

### Haces globales
El haz global permite al satélite iluminar una tercera parte del globo terráqueo, lo que significa que con tres satélites queda comunicada toda la tierra.  Estas tienen un ancho aproximado de banda de 17°, y son capaces de abarcar hasta un **42% de la superficie terrestre**, que es la visual máxima de cualquier satélite geosíncrono. Los niveles de potencia son bastante menores en los haces globales que en los localizados, zonales o hemisféricos, y son necesarios grandes platos receptores para detectar en forma adecuada emisiones de video, audio y datos. 

![Haces]({{ site.baseurl }}/images/2023-6-13/haces.png)

- A = Haces locales y zonales
- B = Haz hemisférico
- C = Haz global

# MODELOS DE ENLACE DE SISTEMAS SATELITALES
En esencia, un sistema satelital consiste en tres secciones básicas: un enlace de subida, un satélite transpondedor y un enlace de bajada. 

### Modelo de enlace de subida
El enlace ascendente (**uplink**) se refiere al proceso de transmisión de señales desde una estación terrestre a un satélite en el espacio. El enlace ascendente es el primer paso en el proceso de comunicación e implica la codificación, modulación y transmisión de la señal desde la estación terrestre al satélite. A continuación, la señal se recibe y descodifica a bordo del satélite, y se realiza cualquier procesamiento de datos necesario. El enlace descendente es el proceso inverso, en el que el satélite transmite los datos de vuelta a la estación terrestre. 

Una estación transmisora terrestre suele consistir de un modulador de FI, un convertidor elevador de frecuencia de FI a microondas RF, un amplificador de alta potencia (HPA, de high-power amplifier) y algún medio de limitar la banda del espectro final de salida (es decir, un filtro pasabandas de salida). El modulador de FI convierte las señales de banda base que entran a una frecuencia intermedia modulada FM, PSK o QAM. El convertidor elevador, que es un mezclador y filtro pasabandas, convierte la FI a una RF adecuada de portadora. El HPA proporciona la sensibilidad adecuada de entrada y la potencia de salida para propagar la señal hasta el satélite transpondedor.

### Modelo de enlace de bajada

El enlace descendente (**downlink**) se refiere al proceso de envío de señales desde un satélite a una estación terrestre o a otro satélite. El enlace descendente se utiliza para transmitir datos, voz, vídeo y otras señales desde el satélite a la Tierra, lo que permite una comunicación bidireccional. 

Los satélites suelen tener varios canales de enlace descendente, que se utilizan para transmitir señales a distintas partes del planeta. La frecuencia de la señal de enlace descendente determina el alcance de la señal: las frecuencias más altas requieren más potencia, pero permiten un área de cobertura más amplia. 

Un receptor en la estación terrestre comprende un BPF de entrada, un LNA y un convertidor descendente de RF a FI. El BPF limita la potencia de entrada de ruido al LNA. Éste es un dispositivo de gran sensibilidad y bajo ruido, como un amplificador de diodo túnel o un amplificador paramétrico. El convertidor descendente de RF a FI es una combinación de mezclador y filtro pasabandas, que convierte la señal de RF recibida a una frecuencia FI. 

![Modelo de enlace]({{ site.baseurl }}/images/2023-6-13/links.png)

### Transpondedor

En transpondedor es un dispositivo que se encargan de recibir las señales de la estación terrestre, procesarlas y enviarlas de vuelta al satélite para su difusión o distribución. 
Los transpondedores suelen utilizarse junto con un módem, que se utiliza para modular la señal antes de transmitirla al transpondedor. El módem toma la señal de datos digital y la convierte en una señal modulada en frecuencia que puede transmitirse por aire. A continuación, el transpondedor procesa la señal y la reenvía al satélite. Un transpondedor satelital típico consiste en un dispositivo limitador de banda de entrada (filtro pasabandas), un amplificador de bajo ruido (LNA, de low-noise amplifier) de entrada, un desplazador de frecuencia, un amplificador de potencia de bajo nivel y un filtro pasabandas de salida. 

![Satelite]({{ site.baseurl }}/images/2023-6-13/satelite.png)

### Enlaces cruzados

Los enlaces satelitales cruzados o **enlaces intersatelitales** (ISL, de intersatellite links) se utilizan cuando es necesario comunicarse entre satélites. Una desventaja de usar un ISL es que tanto el transmisor como el receptor están acotados por espacio. En consecuencia, tanto la potencia de salida del transmisor como la sensibilidad de entrada del receptor son limitadas. 

![enlaces satelitales cruzados]({{ site.baseurl }}/images/2023-6-13/enlace.png)

# PARÁMETROS DEL SISTEMA DE SATELITES
### Pérdida por reducción

La pérdida en reducción (o LOR, por sus siglas en inglés) se refiere a la pérdida de señal que se produce cuando una señal se convierte de una frecuencia más alta a una más baja antes de su transmisión. 

En el enlace descendente de un sistema de comunicación por satélite, la señal recibida de un satélite se convierte de una frecuencia más alta a una más baja antes de transmitirse a la estación terrestre. Esto se hace para reducir la cantidad de datos que hay que transmitir, ya que las señales de frecuencia más baja pueden viajar distancias más largas con menos ruido que las señales de frecuencia más alta. Sin embargo, este proceso de conversión provoca cierta pérdida de señal, lo que se conoce como pérdida en la reducción. La cantidad de pérdida de señal depende de diversos factores, como la frecuencia de la señal, el tipo de convertidor utilizado y las condiciones del medio de transmisión. 

Para compensar la pérdida de señal causada por la LOR, los operadores de satélites pueden utilizar diversas técnicas, como aumentar la potencia de la señal transmitida, utilizar amplificadores de alta eficiencia o diseñar sistemas de recepción más robustos. 

### Potencia de transmisión y energía de bit
La potencia de transmisión se refiere a la cantidad de energía que transmite un satélite o una estación terrestre para enviar una señal a otra entidad. En un sistema de comunicación por satélite, la potencia de transmisión de un satélite viene determinada por la distancia entre el satélite y la estación terrestre, así como por las condiciones atmosféricas o de otro tipo que puedan afectar a la señal. Cuanto mayor sea la distancia entre el satélite y la estación terrestre, mayor será la potencia necesaria para enviar una señal clara. 

La energía binaria, por su parte, se refiere a la cantidad de energía necesaria para transmitir un solo bit de información. Se calcula dividiendo la potencia total consumida por un sistema de comunicación por la tasa total de bits del sistema. Una energía binaria menor significa que el sistema puede transmitir **más información con menos potencia**, mientras que una energía binaria mayor significa que se necesita más potencia para transmitir la misma cantidad de información. 

### Potencia efectiva irradiada isotrópicamente
La potencia efectiva radiada isotrópicamente (EIRP, de effective isotropic radiated power) es una medida de la potencia radiada de un satélite, en relación con un radiador isotrópico, que es una antena teórica que irradia potencia uniformemente en todas las direcciones. 
La EIRP es un factor importante a la hora de evaluar el rendimiento de un sistema de comunicación por satélite, ya que afecta directamente al alcance y la calidad de la señal. Cuanto mayor sea la EIRP de un satelite de comunicación, más lejos podrá llegar la señal y mejor será la calidad de la señal recibida. La EIRP se expresa como sigue: 

`EIRP = Pent(At)`

- EIRP = potencia efectiva irradiada isotrópicamente (watts)
- Pent =  potencia de entrada a la antena (watts)
- At = ganancia de la antena de transmisión (relación adimensional)

# SATÉLITES MULTIMISIÓN

Los satélites multimisión son naves espaciales diseñadas para realizar varias misiones simultáneamente, en lugar de una sola. Estos satélites combinan las capacidades de varios satélites diferentes en uno solo, lo que puede suponer un ahorro de costes y una mayor eficacia. Un ejemplo de satélite multimisión es la nave espacial europea **Copernicus Sentinel-2**, que se utiliza para la vigilancia del medio ambiente. 

![Copernicus Sentinel-2]({{ site.baseurl }}/images/2023-6-13/coper.png)

La misión **[Copernicus SENTINEL-2](https://sentinels.copernicus.eu/documents/247904/4180891/Sentinel-2-infographic.pdf)** comprende una constelación de dos satélites de órbita polar situados en la misma órbita heliosincrónica, en fase de 180° entre sí. Su objetivo es vigilar la variabilidad de las condiciones de la superficie terrestre, y su gran anchura de barrido (290 km) y su elevado tiempo de revisita (10 días en el ecuador con un satélite, y 5 días con 2 satélites en condiciones de ausencia de nubes, lo que se traduce en 2-3 días en latitudes medias) contribuirán a la vigilancia de los cambios de la superficie terrestre. 

La nave proporciona imágenes de alta resolución de la superficie terrestre, incluida la vegetación, las masas de agua y las zonas costeras. 

![Copernicus Sentinel-2]({{ site.baseurl }}/images/2023-6-13/sentinel.png)

Los satélites multimisión son especialmente útiles en situaciones en las que varias agencias u organizaciones necesitan recoger datos en una zona o región específica. Al combinar varias misiones en un solo satélite, se reducen los costes y la complejidad del lanzamiento y la explotación de varios satélites, al tiempo que se mejora la eficacia y la coordinación de la misión global. 

Además de para la vigilancia del medio ambiente, los satélites multimisión pueden utilizarse para otros fines, como la predicción meteorológica, la respuesta ante catástrofes o la recopilación de información. Es probable que el uso de satélites multimisión aumente en los próximos años, a medida que crezca la necesidad de recopilar datos fiables y eficientes en diversos sectores y aplicaciones. 

La comunicación por satélite ha contribuido a grandes avances a lo largo de los años, por ejemplo los teléfonos por satélite, también conocidos como sistemas móviles por satélite, permiten a los usuarios hacer llamadas telefónicas, enviar mensajes de texto e incluso acceder a Internet desde lugares remotos donde no hay cobertura celular. El primer sistema de telefonía por satélite, lanzado en 1999, ofrecía una cobertura limitada y una calidad de voz deficiente, pero los sistemas más recientes, como Iridium y GlobalStar, ofrecen una cobertura mundial y una calidad de voz mejorada. 

![Satélite]({{ site.baseurl }}/images/2023-6-13/sate.png)

Un avance notable en esta era tecnológica es la transmisión de datos a alta velocidad, los primeros sistemas por satélite se limitaban a la transmisión de datos a baja velocidad, pero los satélites modernos pueden transmitir datos a alta velocidad, lo que permite aplicaciones como videoconferencias y streaming. Esto ha hecho que la comunicación por satélite sea más práctica para empresas y personas que necesitan acceso a Internet de alta velocidad en lugares remotos. 

Para poder seguir evolucionando, se han desarrollado diseños avanzados de antenas, estas mejoras en el diseño y la tecnología de las antenas han hecho posible que los satélites admitan un mayor número de usuarios y ofrezcan mayores velocidades de transmisión de datos. Y así mismo, como el Copernicus SENTINEL-2 , lo satélites multimisión, muestran como los satélites son cada vez más versátiles y pueden desempeñar múltiples misiones. 

El desarrollo de la tecnología de comunicación por satélite ha tenido un impacto significativo en la forma en que nos comunicamos e intercambiamos información. Con la innovación continua, podemos esperar ver aún más mejoras en los sistemas de comunicación por satélite, desbloqueando potencialmente nuevas aplicaciones y oportunidades en los próximos años.






























