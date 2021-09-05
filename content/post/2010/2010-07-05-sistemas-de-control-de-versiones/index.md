---
title: "Sistemas de Control de Versiones"
date: 2010-07-05T08:25:11-03:00
slug: "sistemas-de-control-de-versiones"
tags: ['control de versiones', 'desarrollo', 'software']
draft: false
---

[![Subversion project visualization
image.](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Subversion_project_visualization.svg/300px-Subversion_project_visualization.svg.png)](http://commons.wikipedia.org/wiki/File:Subversion_project_visualization.svg)

Image via [Wikipedia](https://commons.wikipedia.org/wiki/File:Subversion_project_visualization.svg)

¿Usaron alguna vez
[SCCS](http://en.wikipedia.org/wiki/Source_Code_Control_System)? ¿No?
¿Que tal [RCS](http://en.wikipedia.org/wiki/Revision_Control_System)?
¿Tampoco? Bah, son ustedes muy jóvenes. Pero, usan un 
[sistema de control de versiones](http://es.wikipedia.org/wiki/Control_de_versiones), ¿verdad?

Hoy es raro que un desarrollador no use un sistema de control de
versiones como [CVS](http://www.nongnu.org/cvs) o
[Subversion](http://en.wikipedia.org/wiki/Subversion_%28software%29)
(conocido también como SVN).

Lo que no me explico es ¡por qué no lo usa todo el mundo!

Verán, mucha gente escribe un archivo word,
*"aburrido*informe*para*el*auditor.doc"*, empiezan a trabajar en este,
si son astutos, y tienen experiencia, antes de realizar una modificación
hacen una copia y empiezan a trabajar en
*"aburrido*informe*para*el*auditor-version-2.doc"*, y después en
"*aburrido*informe*para*el*auditor-version-3.doc"* y sigue la cosa, y
la carepta se llena de archivos como *"informe*auditor*4.doc",
informe-auditor-final.doc",
"informe-para-el-auditor-revisado-por-mi-jefe.doc",
"informe-ups-me-equivoqué-en-losplazos.doc"* y así, la carpeta de
trabajo es un desastre, si es que usan carpeta, y no lo tienen
desparramado en el escritorio (los lectores de LNDS no hacen eso, por
supuesto).

Los programadores tenemos este problema, pero multiplicado por mil,
porque los usuarios están llenos de ideas creativas y el software va
cambiando todo el tiempo, y a veces hay que volver atrás. O tienes
código que implantas para un cliente, y luego se crea una rama de código
con modificaciones ad hoc para un cliente. Los escenarios son múltiples.

Es por eso que desde 1972 tenemos sistemas de gestión de versiones de
código. Los primeros eran los que mencioné en la primera parte de este
artículo. Estos primeros sistemas estaban orientados al trabajo
individual de cada programador.

El problema era cuando un equipo de programadores trabajaban en el mismo
proyecto, ahí nacieron sistemas centralizados, como CVS, SourceSafe (de
Microsoft), Perforce, y el más famoso de todos Subversion.

No les voy a explicar acá qué es un [sistema de control de
versiones](http://es.wikipedia.org/wiki/Control_de_versiones), sólo les
voy a sugerir, si no son programadores, que investiguen sobre estas
cosas, y las utilicen en su trabajo, es una buena estrategía (para los
diseñadores web esta es una herramienta muy útil).

En lo que si me quiero meter es en el tema de los sistemas de control de
versiones distribuidos, que son, en mi opinión ([y no estoy sólo en
esto](http://joelonsoftware.com/items/2010/03/17.html)), un gran avance
en nuestro campo. Pero eso lo vamos a dejar para el próximo post.
