---
comments: true
date: 2005-11-04 19:18:15
layout: post
slug: ulpn-2
aliases: [/2005/11/ulpn_2.html]
title: ULPN 2
wordpress_id: 2020
categories:
- Educación
tags:
- OLPC
- ULPN
---

Sobre el prototipo, [nos informa Zuckerman](http://www.worldchanging.com/archives/003707.html), se está trabajando activamente, hay una demo programada para el 16 de noviembre en[WSIS](http://www.itu.int/wsis/). El pudo ver una especie de maqueta (mockup) en la oficina de Negroponte.

El sistema está diseñado para trabajar en 3 modos, laptop mode, book mode y game mode.


Parece que el diseño aún está en discusión, pero lo que vio Zuckerman se parece mucho a la imagen siguiente:
![ulpn.jpg](prototipo.jpg) 


El prototipo tendría el tamaño de un libro grande, tiene una protección de goma rígida por los bordes, la que se puede doblar para formar un apoyo. Un problema no menor son las "bisagras", que deben permitir unos 340 grados de libertad entre el teclado y la pantalla. De acuerdo a Negroponte el costo de este accesorio es de unos 5 dolares, y tienen un mecanismo bastante complejo para permitir la rotación. Lo interesante va a ser bajar el costo de este accesorio a centavos.

El teclado que Zuckerman vio en el prototipo es desmontable, probablemente porque se tiene la idea de que los teclados variarán según el país de destino. En China por ejemplo, en vez de teclado se usará un lápiz y un área para poder dibujar los ideogramas (!?).

Una de las mayores preocupaciones y sobre lo que mas se ha hablado en el MIT es sobre la pantalla, una de las componentes más caras en los laptops. Los diseños preliminares mencionaban el uso de [e-Ink](http://www.eink.com/). Este se habría dejado para una segunda generación, principalmente por los requerimientos energéticos de este tipo de displays.

La primera generación usará pantallas LCD, pero de un tipo bastante distinto al que estamos acostumbrados a ver en los laptops. La pantalla tiene una luz trasera, como las pantallas de las PDAs, pero es una tecnología denominada transmisive display. Normalmente estos display tienen los típico 3 filtros rojo, verde y azul que se aplican a cada pixel, pero esto los hace muy consumidores de energia. La solución final es bastante complicada, y consiste en tener 3 luces traseras rojo verde y azul y mediante microscópicos lentes estas luces se enfocarán para producir el color final de cada pixel. La verdad es que cuesta imaginar este mecanismo, pero aparentemente es la solución más barata que encontraron.

Como el display es totalmente a medida se está negociando con proveedores en China para producir estos display a una fracción del costo normal de estos dispositivos. Es probable que por las restricciones energéticas estas pantallas sean menos brillantes de lo que estamos acostumbrados a ver.

La idea de Negroponte es que la energía proporcionada por la manivela sea de 100:1, es decir, por 1 minuto de carga con la manivela, se tengan 100 minutos de operación.

Zuckerman cuestionó intensamente a Negroponte con respecto a la energía del sistema, y este parecía tener respuestas para todo: ¿ 12 volt de potencia ? Hay adaptadores para eso; ¿Sobrecargas de voltaje? no hay problema dado el modesto uso de energia del sistema. ¿ Enfriamiento ? La máquina no usará ventilador, pues no tiene disco duro y el procesador es relativamente lento.

La única área en que Zuckerman no quedó satisfecho con la respuesta de Negroponte fue sobre el soporte de la red inalámbrica. Recordemos que el modelo propuesto es una red que se arma a partir de la unión entre todos los laptops formando una malla. Todos los trabajos en redes tipo mallas requieren de 2 radios por máquina para proveer un backbon robusto de comunicaciones, y la máquina propuesta sólo tiene 1 radio, probablemente para horar costos. Hay que ver si esto va a funcionar de este modo, se me ocurre que algún esquema de time sharing y de cambio de frecuancias, al estilo de las redes TDMA en telefonía celular podría funcionar.

Esta serie continua con el software del ULPN...





