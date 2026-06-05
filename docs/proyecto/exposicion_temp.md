
# **EXPOSICION**

## Atril exibidor interactivo.

![](../images/PF-A.jpg)

Atril o vitrina para exhibición de maquetas impresas en 3D. Es un equipamiento interactivo de forma cúbica, ensamblada en dos partes, una encastrada en la otra y en la parte superior una campana rectangular de acrílico transparente con un baño de luz desde abajo hacia arriba. Tendrá electrónica y programación para control de iluminación, audio, giro y ajuste de altura. Las funcionalidades estrategicas son fácil montaje y desmontaje, una vez montadas es de fácil traslado, y acopio en espacios reducidos.

![](../images/PF-A-a.jpg)

Dimensiones: 40x40x80 cm, extendible hasta 110 cm en altura.
Peso que soportará: entre 50 y 2500 g
Materialidad: Placa compensada, terminación melamínico de madera de 15 mm de espesor, en dos partes; una encaja en la otra; la interior es móvil, se levanta con un pistón eléctrico accionado con un botón y tiene tres posiciones.

![](../images/PF-A-b.jpg)

1- La interacción con el observador es la siguiente: cuando se acerque la persona, que se intensifique la iluminación automáticamente; mientras no hay observador delante, la luz late suavemente. 

2- Ajuste de altura: El atril o vitrina tiene que ajustarse a la altura del observador mediante un sensor o un botón con tres posiciones: bajo, medio, alto.

3- El disco rotatorio debe girar a la izquierda o a la derecha con dos botones; presionando el botón, gira; al soltar, se detiene.

4- Tiene una pantalla táctil de 10" que inicia automáticamente el audio descriptivo y las imágenes si se detecta que el observador permanece 10 segundos frente a la vitrina. La pantalla debe permitir pausar el audio, reiniciarlo o ir hacia atrás como los videos de YouTube. 

5- Luego de detectar por 20 segundos que no hay personas frente al atril, vuelve todo al modo inicial. la luz late suavemente y el audiovisual vuelve al inicio y espera.


6-La alimentación es con batería recargable y tiene que tener encender las luces en color rojo como indicador de bateria baja cuando quede solo un 10% de la energia total.

Protitipado, maquetación impresa en 3D

La maquetación del prototipo se imprimió aproximadamente a escala 1/5. Se busca un tamaño que permita reproducir el proceso de montaje. Evaluar las olguras y analizar la resistencia estructural. Es necesario verificar las partes móviles que van encastradas una dentro de otra. Por otro lado, se proyecta los espacios donde se alojarán los componentes electrónicos, baterías y elementos que deben quedar incluidos en el equipamiento.   

![](../images/PF-A-c.jpg)

La fabricación está proyectada en madera contrachapada, terminación natural de 15 mm cortada con láser o con rúter CNC. El mobiliario está compuesto por 20 piezas más las 4 ruedas. Es totalmente desmontable.


![](../images/PF-A-d.jpg)

Estimé el tiempo de fabricación usando Easel, en 7 horas estarian todas las piezas cortadas con el rúter CNC.

![](../images/PF-A-e.jpg)

Ensamblar la maqueta del prototipo con todas las piezas impresas en 3D insume 10 minutos; con las piezas reales, el encastre y el montaje se estima en un máximo de 2 horas, incluida la instalación de las ruedas. Como herrajes de seguridad para un cierre que le dé firmeza y solidez al sistema, se pretende usar tornillos con tuercas incrustadas ocultas.

![](../images/PF-A-f.jpg)

---

Prototipado del Atirl

![](../images/PF-ProtoAtr-a.jpg)

Un cambio de logística nos hizo reconfigurar la estrategia de prototipado del atril exhibidor. Cambiamos la idea original de cortar las piezas con CNC de sustracción con fresa a corte con ruter láser. En el laboratorio de Minas había disponible MDF de 3 mm y decidí adaptar el diseño. Lo primero fue pasar de 10 a 3 mm en todas las piezas CAD. Luego pasamos al CAM distribuyendo las piezas en planchas de 600x900 mm. 

![](../images/PF-ProtoAtr-c.jpg)

![](../images/PF-ProtoAtr-b.jpg)

![](../images/PF-ProtoAtr-d.jpg)

![](../images/PF-ProtoAtr-e.jpg)

![](../images/PF-ProtoAtr-f.jpg)

![](../images/PF-ProtoAtr-g.jpg)

![](../images/PF-ProtoAtr-h.jpg)

![](../images/PF-ProtoAtr-i.jpg)

![](../images/PF-ProtoAtr-j.jpg)

![](../images/PF-ProtoAtr-k.jpg)

![](../images/PF-ProtoAtr-l.jpg)

![](../images/PF-ProtoAtr-m.jpg)



---

![](../images/PF-Ex-Elec-a.jpg)

## Electrónica

La incorporación de la electrónica está orientada a mejorar la experiencia del usuario en la interacción con el objeto en exhibición. Permitir que el observador pueda adaptar el mobiliario a su curiosidad con tres variables programadas electrónicamente.

El control del giro 360 del objeto en ambos sentidos, controlar la altura del mobiliario para acceder a una perspectiva personalizada según la altura del observador. Y la última variable es la iluminación automatizada de bienvenida; el objeto se ilumina cuando el observador se acerca al atril.

Este desafío en tres etapas inicia con un motor paso a paso para el disco giratorio, donde dos botones irán posicionados en los costados del panel frontal informativo. Para lograrlo, se usó un módulo ESP32, dos pulsadores de dos bornes y un motor paso a paso 28BY-48 de 5 V con su correspondiente placa. La plataforma de programación que usé es Arduino IDE y los códigos de programación los obtuve con ChatGPT Plus. 

![](../images/PF-Ex-Elec-b.jpg)

![](../images/PF-Ex-Elec-c.jpg)

Basado en los esquemas, logré una conexión exitosa, no sin muchas horas de pruebas, práctica de soldaduras con estaño y las dificultades del trabajar domésticamente; como ejemplo, no disponer de pinzas que sujeten los elementos es un obstáculo que genera un estrés importante. Que no se pegue el estaño en los cables es otro; evitar el humo tratando de mirar; hagas lo que hagas, siempre busca la nariz. Los terminales hembra de los cables Dupont se agrandan y no hacen buen contacto, y el más grave, quemar la placa Arduino en el camino del LabDom. Todo es parte del aprendizaje y las dificultades van dando paso a la experiencia. 

![](../images/PF-Ex-Elec-d.jpg)

El sistema de motor paso a paso para el disco tiene dos pulsadores a los que solde cables dupon MM y MH. El modulo ESP32 es ideal para controlar el giro en dos sentidos. el giro inicia cuando se mantiene presionado el boton y se detiene cuando se suelta. El giro debe ser muy suave y la forma de lograrlo es usando este tipo de motor. Los cuatro cabres que conectan la placa del motor al modulo

![](../images/PF-Ex-Elec-e.jpg)

El sistema de motor paso a paso para el disco tiene dos pulsadores a los que soldé cables Dupont MM y MH. El módulo ESP32 es ideal para controlar el giro en dos sentidos. El giro inicia cuando se mantiene presionado el botón y se detiene cuando se suelta. El giro debe ser muy suave y la forma de lograrlo es usando este tipo de motor. Los cuatro cables que conectan la placa del motor al módulo van en secuencia consecutiva y positivo al VIN y el negativo al GND; es como una regla constante. El prompt para el código de programación es el siguiente: 

1- Necesito que generes una imagen con boceto, tipo TinkerCAD, para conectar un motor paso a paso a un módulo ESP32 como los de la imagen.
2- Necesito el código de programación para controlar el giro del motor hacia la derecha y hacia la izquierda con los dos pulsadores.

Con eso logré un funcionamiento adecuado para el disco; próximo paso, modificar el diseño para incorporar la electrónica.

---
Para la iluminación del atril necesito trabajar con tiras LED y el objetivo es lograr que se enciendan automáticamente con el acercamiento de una persona. Use el sensor de distancia que usamos en el módulo 4. El primer desafío fuerte es que las tiras usan una fuente externa que lleva el voltaje de 220 a 12 V. Disponía de una tira tipo NEON y otra cinta de 8 mm de ancho. La fuente que tengo sirve para ambas, pero el Chatgpt me recomendaba usar un interruptor MOSFET para interconectar la fuente y la tira LED. 

![](../images/PF-Ex-Elec-f.jpg)

![](../images/PF-Ex-Elec-g.jpg)

Inicié trabajando con la placa Arduino UNO y tuve que ir a comprar el MOSFET. Primer paso: preparar los terminales para conectar los componentes, salida de fuente y ficha para conectar la fuente al tomacorriente. En el extremo de la tira, soldé terminales macho para trabajar en la protoboard. Después seguí con descifrar la conexión del MOSFET entre la fuente y la tira LED. 

![](../images/PF-Ex-Elec-h.jpg)

![](../images/PF-Ex-Elec-i.jpg)

Entre los bornes de entrada VIN + y VIN -, los de salida OUT + y OUT -, el GND y el TIRG/PWN, más los cuatro terminales del sensor de distancia, en algún momento conecté en un pin incorrecto y quemé la placa de Arduino.

![](../images/PF-Ex-Elec-j.jpg)

Sin un diagnóstico claro, antes de hacerle el acta de defunción al Arduino, lo conecté a otras PC y la luz de alimentación prendía y en dos segundos se apagaba. Recién tuve cereza cuando en Eneka me lo probó un técnico; midiendo temperatura, me dijo que no solo era el zócalo, sino que tenía resistencias sobrecalentadas.

![](../images/PF-Ex-Elec-k.jpg)

Me pasé a ESP32; las conexiones se simplificaron y las dos tiras encendían, pero no respondían a la programación, por lo que empecé a sospechar que el interruptor MOSFET también estaba dañado. Cambié por un transistor sugerido por ChatGPT, IRLZ44N, con tres patas. Otra visita al proveedor. El frente del componente es el que tiene las escrituras; en base a eso se conecta en la pata izquierda G, centro D y derecha S. 

![](../images/PF-Ex-Elec-l.jpg)

![](../images/PF-Ex-Elec-m.jpg)

![](../images/PF-Ex-Elec-n.jpg)

Otro aprendizaje importante es que la tira que estoy usando no es direccional, por lo que no es posible lograr efectos de recorridos progresivos de la luz. Solo lograría control de intensidad en intervalos de tiempo. El ESP32 se conectó y corrió la programación sin problemas y los resultados fueron visibles y muy buenos. 

![](../images/PF-Ex-Elec-ñ.jpg)

![](../images/PF-Ex-Elec-o.jpg)

Por último, le pedí a la IA generativa que me hiciera un boceto de la placa con todos los circuitos y así me tiró la primera edición dimensionada de lo que podría llegar a ser.

![](../images/PF-Ex-Elec-p.jpg)

Ahora falta solo resolver la elevación telescópica del atril mediante un eje con roscado y otro motor paso a paso.

---

Prensas tipograficas que se ponen en exibición.

Prenas Plana Comon Press de 1810 - 
Prensa Plana Minerva Cropper 1890 -
Prensa Plano Cilindrica Werfedale de 1890 -
Prensa Plana Minerva Heidelberg de 1920 -
Chivalete tipográfico -
Guillotina manual -

---

![](../images/PF-Ex-Min-a.jpg)

## Prensa Plana

Esta búsqueda experimental para explicar el marco tecnológico donde se generó la cultura gráfica, la comunicación visual en una época pasada, provocó un giro importante en el énfasis del Proyecto Final.

Se materializó un producto híbrido entre un modelo mecánico, una pieza didáctica y un objeto de autor. 

![](../images/PF-Ex-Min-b.jpg)

El proceso inicia con un prototipo estático de una minerva basado en un afiche promocional del modelo Cropper de origen inglés fechado en 1875. El modelado realizado en CAD comienza con la traducción de la imagen a dibujo técnico bidimensional, seguido por la individualización de partes para conseguir las piezas tridimensionales por separado. Una vez lograda, cada parte se ensambla virtualmente usando herramientas para mover y rotar objetos.

![](../images/PF-Ex-Min-c.jpg)

El desafío es lograr que un modelo estático se convirtiera en un modelo funcional con todo su sistema de piezas móviles. Para lograrlo, hay que trabajar el modelo en otro programa. Es así que llevé el archivo STL original a Fusion y comencé el proceso de adaptación del modelo. Pasar de malla a sólido y mejorar toda la geometría de las partes, sobre todo las curvas, que en su mayoría hay que redibujarlas. En la siguiente imagen están el prototipo estático a escala 1/13 con la referencia humana y el prototipo cinético a escala 1/8.

![](../images/PF-Ex-Min-d.jpg)

Todo el proceso para conseguir una vinculación cinemática del sistema, con engranajes, bielas, pivotes, cigüeñales, requiere mucha observación de modelos reales y ensayos con piezas fabricadas. Encastres con holguras precisas, resistentes y tolerancias suaves en las geometrías y una buena dosis de intuición de autor. 

![](../images/PF-Ex-Min-e.jpg)

Fueron aproximadamente unas 50 horas de estudio para lograr el primer prototipo funcional con 55 piezas. Esto permitió corregir el modelo final ajustado para fabricar una pieza más acabada, con un mecanismo más funcional y suave en sus movimientos.

![](../images/PF-Ex-Min-f.jpg)

En el laminador se organizan las piezas, planificando los tiempos de impresión y el registro de las distintas piezas que fueron cambiando su forma para lograr el objetivo. El otro componente que tiene influencia en la forma de las piezas es el ensamblaje del objeto.

![](../images/PF-Ex-Min-g.jpg)

El prototipo se fabricó a una escala aproximada de 1/8; el modelo real mide 50 cm de ancho por 148 cm de altura. El prototipo mide 20 cm de altura por 13 de ancho; corresponde al aprovechamiento máximo de la cama de impresión que disponemos, que es de 22x22x22 cm.

![](../images/PF-Ex-Min-i.jpg)

![](../images/PF-Ex-Min-h.jpg)

Iniciamos el proceso de fabricación de modelo final a escala 1/5; corresponde a un modelo de 28 cm de altura. Se imprimió en el laboratorio de la sede UTEC de Minas. Donde surge la idea de imprimir la colección completa y le da un nuevo giro al PF.

![](../images/PF-Ex-Min-k.jpg)

![](../images/PF-Ex-Min-l.jpg)

![](../images/PF-Ex-Min-n.jpg)

![](../images/PF-Ex-Min-m.jpg)

---

## Referencias

<iframe width="560" height="315" src="https://www.youtube.com/embed/a5UFos_ysz8?si=KZxNokWpNHow3Wtb" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


[Restauración prensa cropper](https://typeandstyle.blogspot.com/2014/08/letterpress-restoration-done.html?m=1)