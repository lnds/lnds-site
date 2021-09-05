---
title: "El Señor de los Archivos"
date: 2012-02-22T08:25:11-03:00
slug: "el-senor-de-los-archivos"
tags: ["github", "historia"]
draft: false
math: false
---

Esta es una traducción al artículo de Wired sobre GitHub titulado "The
Lord of The Files: How GitHub Tamed Free Software (And More)",
publicado el 21 de febrero. El "código" de este artículo fue publicado
por Wired en el mismo GitHub con el permiso para ser re mezclado,
traducido usando una licencia creative commons. Mi traducción está
disponible en [una rama en mi cuenta en GitHub](https://github.com/lnds/Lord-of-the-Files). Desde ya agradezco
los comentarios para mejorar esta traducción, pues requiere mucho
trabajo aún.

## **El Señor de los Archivos: Cómo GitHub Domesticó al Software Libre (Y Más)**

por Robert McMillan, Wired Enterprise

Publicado originalmente
en: <http://www.wired.com/wiredenterprise/2012/02/github/>

SAN FRANCISCO --- Cuando los fundadores de GitHub se trasladaron a su
ostentoso loft en South-of-Market el año pasado, lo primero que hicieron
fue redecorar. Convirtieron la oficina más grande del piso en la parodia
de una suite ejecutiva, completamente incluyendo una chimenea falsa,
sillones de felpa y un globo terráqueo de madera que se abre para
revelar una botella de whisky escocés de malta. Colgado de la pared está
una pintura de un gato, vestido como Napoleón, con cinco piernas de
pulpo. Lo llaman el Octocat.

Lo cierto es que esta no es una suite ejecutiva. Es una sala de
reuniones comunal donde cualquiera puede juntarse con alguien más, y
tener algo de diversión al mismo tiempo.

"Todos pueden traer a sus amigos a esta sala y tratar de impresionarlos
y ese tipo de cosas", dice Scott Chacon, CIO de GitHub y cofundador.
Verán, Chacon, el CEO Chris Wanstrath y el resto del equipo ejecutivo no
tienen oficinas privadas. Trabajan en el piso abierto junto a los
programadores, pegados a los monitores con el resto del equipo,
escuchando a LCD Soundsystem. Fuerte.

![](github.jpg)

El fantástico loft de 1.300 metros cuadrados refleja su misión:
democratizar la programación de computadores. GitHub.com puede ser visto
como un Facebook para geeks. En vez de subir videos de tu gato, subes
software. Cualquiera puede comentar tu código y agregarle algo, y
construir sobre este algo mejor. El truco es la programación
descentralizada, dándole a cada uno un nuevo tipo de control. GitHub ha
remecido la manera en que el software se escribe, haciendo la
codificación un poco más anárquica, un poco más divertida, y mucho más
productiva.

El mundo del software lo ama. GitHub ahora tiene más de 1.3 millones de
usuarios, y sobre 2 millones de repositorios de código fuente, ocho
veces la cantidad de hace dos años atrás. Si cuentas secciones de código
y páginas Wiki que están almacenadas en el sitio, hay más de 4 millones
de repositorios. Dos años atrás, GitHub era un equipo de ocho,
sosteniendo reuniones de la compañía en los cafés de San Francisco.
Hacia el principio de 2011, había crecido a 14 "hubbernautas" (como se
llaman afectuosamente a los empleados de GitHub) y un años después,
están en 57. En julio tomaron las antiguas oficinas de la empresa de
blogging Six Apart. GitHub está creciendo rápido, y no ha tomado un
centavo de fondos de riesgo.

Una vez que has escuchado sobre GitHub, comienzas a verlo casi en todos
lados. A veces está alojando el código que soporta un website de
renombre. Otras veces está impulsando un secreto proyecto dentro de una
compañía Fortune 500. Ha llevado el software abierto mucho más cerca de
cumplir su promesa, pero no se detienen allí. Está democratizando la
creación de páginas web y herramientas de análisis de ADN y tal vez
incluso las leyes de la tierra.

"GitHub ha cambiado la manera en que la gente se aproxima al
desarrollo," dice Tom Preston-Werner, el director de tecnología de la
compañía. "Se dan cuenta que no tiene que ser tan complejo."

## **Git Rasca la Comezón**

Como tantos otros proyectos geek exitosos, GitHub comenzó con
programadores rascando su propia picazón. Hace cinco años atrás,
Wanstrath y su colega programador P.J. Hyett estaban escribiendo código
en Cnet, el sitio de noticias y comentarios sobre tecnología. El
lenguaje que eligieron fue Ruby on Rails, un ambiente de programación
que facilita desarrollar aplicaciones web.

En la medida que construían sus sitios en Cnet, Wanstrath y Hyett
comenzaron a construir una cantidad de mejoras a Ruby on Rails en si
mismo. Pero encontraron que no era fácil lograr integrar estos cambios
de vuelta en el proyecto de código abierto. Siguiendo el modelo de
desarrollo de código abierto dominante entonces, Rails era administrado
por un cuadro de desarrolladores de confianza a quienes se le había dado
el permiso para "enviar" cambios al código fuente del proyecto. Para
lograr que sus cambios fueran agregados al código central, Wanstrath y
Hyett tendrían que hacer lobby a uno de estos programadores de confianza
y convencerle de que sus cambios valían la pena para ser incorporados.
Eso a menudo era más trabajo que escribir el código en primer lugar.

Ellos no eran los únicos desarrolladores con problema con el modelo del
Cuidador de Confianza del código abierto. Una década atrás, Linus
Torvalds se encontraba lidiando con su rol de cuidador del sistema
operativo Linux que él había inventado. En el principio, Torvalds alojó
Linux en un sitio web que pertenecía a la Universidad de Helsinki. Si la
gente encontraba un error en el código, le enviaban un archivo con los
cambios vía email. Si Torvalds leía el email y le gustaban los cambios,
el incorporaría los cambios en Linux. Pero Torvalds es conocido por no
leer todos sus emails, así que en la medida que el proyecto se hacía
popular, más y más propuestas se escurrían por las grietas.

Este era el pequeño secreto sucio del software de fuente abierta. Con el
proyecto de software libre promedio, grandes cantidades de código,
quizás demasiado código, nunca llegaban a ser usadas. Era a menudo
demasiado difícil para el usuario casual mostrarle a los desarrolladores
los cambios que había hecho y después integrar fácilmente estos cambios
de vuelta a la base de código.

## **La Segunda Venida de Linus**

Así que en el 2005, Torvalds crea Git, un software de control de
versiones específicamente diseñado para librarse del pesado trabajo de
administrar proyectos de software. Usando Git, cualquiera puede
manipular su propia versión de Linux, o en realidad de cualquier
proyecto de software, y luego, presionando un botón, compartir esos
cambios con Torvalds o cualquier otro. No hay guardián. En términos
prácticos, Torvalds creó una herramienta que facilita a cualquiera la
creación de alternativas a su proyecto Linux. En términos técnicos, esto
se llama un "fork".

En los 1990s, el "forking" se consideraba algo malo. Era lo que había
creado todas esas versiones incompatibles de Unix. Por un tiempo, había
un gran temor de que alguien pudiera crear su propia versión de Linux,
una versión que no pudiera correr los mismos programas o trabajara de la
misma forma. Pero en el mundo de Git, el "forking" es bueno. El truco
es asegurarse que los cambios que la gente realiza puedan ser
compartidos de vuelta con la comunidad. Es mejor dejar que la gente
versione un proyecto y lo manipule con sus propios cambios, que cerrarlo
todo permitiéndole a unas pocas autoridades confiables que toquen el
código.

En un día soleado poco habitual en Portland, Torvalds demostró Git a
Wired en la oficina de su casa. Con unos pocos golpes de teclado, el
pudo revisar dos nuevos aportes al kernel que cambiaban el mismo código
de formas diferentes, un potencial problema en el fuente.

{{<figure caption="¿Por qué Git? Es el término popular británico para estúpido, persona despreciable, asno. El chiste \"Nombro todos mis proyecto por mi mismo, primero Linux, después git.\" era demasiado bueno para dejarlo pasar. Pero también es algo corto, fácil de decir, y escribir en un teclado estándar. Y razonablemente único y no como cualquier comando estándar, lo que es inusual. - Linus Torvalds" src="linus1-e1329349353889.jpg">}}

El viejo régimen "hace muy difícil empezar una rama radical porque
generalmente tienes que convencer a la gente comprometida con el status
quo desde el principio sobre la necesidad de soportar este cambio
radical", dice Torvalds. "En contraste, Git facilita esto para que
simplemente \'lo hagas\' sin pedir permiso, y entonces puedas volver y
mostrar como resultó todo, diciéndole a la gente \'miren lo que hice, y
tengo los números para mostrar que mi aproximación es mucho mejor.\'"

Puede haber sido hecho para Linux, pero Git rápidamente resultó ser una
bendición para cualquier organización grande manejando bases de código
gigantescas. Hoy en día Facebook, Staples, Verizon e incluso Microsoft
son usuarios. En Google, Git es tan importante que la compañía le paga a
Junio Hamano, quien se hizo cargo del proyecto después de Torvalds, para
que trabaje en Git a tiempo completo, y también paga el salario para el
segundo a cargo, Shawn Pearce.

## **Git sin el 'dolor en el trasero'**

El problema es que no todos son Linus Torvalds, y no todas las compañías
son Google. Para el 99 por ciento, la interfaz de linea de comandos de
Git es notoriamente difícil de usar. Ahí es donde viene GitHub.
Simplifica Git. Un montón. Su primer eslogan era: "Git hosting: No
longer a pain in the ass." (Alojamiento Git sin las molestias)

Tom Preston-Werner soñó sobre GitHub e involucró a Chris Wanstrath en el
proyecto una noche de octubre de 2007, en un encuentro de programadores
en Zeke, un bar deportivo en San Francisco, a unas cuadras del estadio
donde juegan los Gigantes de San Francisco.

Al principio, GitHub era un proyecto lateral. Wanstrath y Preston-Werner
se encontrarían los sábados para planificar, mientras que escribirían
código durante su tiempo libre y sus trabajos diarios. "No se suponía
que GitHub fuera una startup o una compañía startup. GitHub era sólo una
herramienta que necesitábamos," dice Wanstrath. Pero, inspirados por
Gmail, hicieron una beta privada del proyecto y lo abrieron a otros.
Pronto se pudo de moda en el mundo exterior.

Para enero de 2008, Hyett estaba a bordo. Y tres meses después de esa
noche en el bar deportivo, Wanstrath recibió un mensaje de Geoffrey
Grosenbach, el fundador de PeepCode, un sitio educativo en linea, que
había empezado a usar GitHub. "Estoy alojando el código de mi compañía
aquí", les dijo Grosenbach. "No me siento cómodo sin pagarles chicos.
¿Puedo enviarles un cheque?"

Fue el primero de muchos. En julio de 2008, Microsoft adquirió Powerset,
la startup que le proveía a Preston-Werner de un trabajo de día. El
gigante del software le ofrecieron a Preston-Werner a $300,000 dólares
y opciones de acciones para que se quedara a bordo por otros tres años.
Pero el se retiró, apostando todo a GitHub.

"Daba un poco de miedo en ese tiempo rechazar algo así, pero no
cambiaría nada de esa decisión en absoluto", dice ahora.

Cuando Wired visitó las oficinas de GitHub's a principios de este año,
encontramos una suerte de paraíso geek. Hay un quacóptero controlado por
un iPhone y un dispensador de cerveza de cuatro grifos, una sala de
conferencias que como una escenografía de bajo presupuesto de la sala de
situaciones de la Casa Blanca, completa con unos enormes teléfonos rojos
al estilo de los 1970s. Pero los juguetes no son lo que hacen a GitHub
diferente. Es la abierta hostilidad de la startup a comando y control
corporativo lo que la diferencia.

"No llevamos un registro de los días de vacaciones, no tenemos registro
de las horas. No nos importa", dice el CIO Scott Chacon. "He estado acá
a la medianoche y hay cinco personas aquí. Y he estado al mediodía de un
jueves y no hay nadie."

Y aún así es el equipo de desarrollo de software más productivo con el
que he trabajado, dice Chacon.

## **Git hacia el futuro**

La apuesta de Preston-Werner's se ha pagado. GitHub es ahora rentable.
Los usuarios pueden firmar gratuitamente y comenzar a contribuir, pero
deben pagar dinero si quieren que su código sea alojado de forma
privada, comenzado a los $7 dólares al mes. GitHub también vende una
versón empresarial del producto que permite a las compañías correr su
propia versión de GitHub detrás del cortafuegos corporativo. 

Esto empieza a los  $5,000 dólares por año, pero puede costar cientos de
miles de dólares anualmente para compañías con cientos de programadores.

Irónicamente, sin embargo, los fans más duros de GitHub no incluyen a
Torvalds, quien brevemente movió el kernel de desarrollo a GitHub el
pasado septiembre después de una falla de seguridad en su antiguo hogar.

"Me gusta mucho GitHub," dice. "Hay una razón por la que llegó a ser uno
de los repositorios de código fuentes más grandes en forma tan rápida".
Pero luego desenrolla una larga lista de todos los problemas "serios"
que ha tenido con él cuando ha alojado su código en el sitio, muchos de
los cuales han sido reparados desde entonces. No podía filtrar
comentarios, la interfaz de correo perdía anexos, la interfaz web
desordenaba las contribuciones al código, y así. El balance: GitHub
facilita escribir código. Pero también facilita generar basura."

Eso podría ser cierto, pero el sitio no ha vuelto atrás. Los usuarios
GitHub están aparentemente por todos lados. En una tarde reciente en la
vecindad de la Playa Norte de San Francisco, Wired estaba discutiendo el
sitio con el director de ingeniería de GitHub Ryan Tomayko. De repente
la persona en la mesa próxima se acercó e interrumpió, como un
adolescente escuchando a dos extraños hablar de su banda favorita. "Les
tengo que decir", dijo, "GitHub es asombroso."

Incluso apoya al movimiento Occupy. Cuando Jonathan Baldwin quiso
escribir la versión para teléfonos celulares del Micrófono del Pueblo,
usado por Occupy para pasar mensajes a través de grandes multitudes, el
publicó su código directamente en GitHub. El sitio le deja compartir el
código fácilmente, y rápidamente conectar con otros desarrolladores para
trabajar en los asuntos técnicos. "GitHub es lo mejor. Si no alojas en
GitHub, entonces no existe", dice Baldwin, un estudiante en Parsons, La
Nueva Escuela de Diseño en Nueva York.

Y el software es sólo parte de la historia. Los geeks están aprendiendo
que GitHub puede ayudar para manejar otros proyectos. Libros, incluso
transcripciones de charlas han aparecido en el sitio. Un usuario GitHub,
Manu Sporny, publicó la información de su ADN en el sitio el año pasado,
con la esperanza de estimular el desarrollo de software de análisis de
ADN de código abierto proveyendo datos reales para el análisis.

Cuando Scott Chacon escribió un libro sobre GitHub, el primer fork
apareció en un mes. Era una traducción al alemán de su libro. Ahora,
tres años después, ha sido traducido a 10 lenguajes, con otras 10
traducciones en trabajo. La mitad del tráfico al sitio web del libro
viene de China. "Miles de personas en China están aprendiendo Git porque
pueden leer \[el libro\] en chino en mi sitio web, porque alguien lo ha
provisto,", dice

Ryan Blair, un tecnólogo con el Senado del Estado de Nueva York, piensa
que aún puede darle a los ciudadanos una manera de versionar la ley,
proponiendo sus propias enmiendas a los oficiales electos. Una
herramienta como GitHub podría facilitar a los constituyentes rastrear y
aún tener voz para sus opiniones en los cambios del complejo código
legal. "Cuando realmente lo piensas, un proyecto de ley es una rama de
la ley", dice. "Me encanta la idea de que un constituyente sea capaz
de enviar a su senador estatal un pull request."

GitHub es el regalón del mundo open source, pero este año la compañía ha
puesto su vista sobre Microsoft. La compañía recientemente contrató a un
par de desarrolladores del gigante del software, y está trabajando en
nuevo software para atraer al aún considerable ejército de codificadores
que programan usando las herramientas de desarrollo de Microsoft.

"Quiero vivir en un mundo donde es más fácil trabajar juntos que
trabajar solos\... donde cada parte del proceso de desarrollo de
software es un placer", dice el CEO Wanstrath. "Y creo que GitHub puede
ayudar a que eso pase."

![](Octocat-300x300.jpg)

Imágenes obtenidas del [artículo de Wired](http://www.wired.com/wiredenterprise/2012/02/github/), usadas de acuerdo a licencia CC.
