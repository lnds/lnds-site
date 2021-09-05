---
title: "Flame y MD5"
date: 2012-06-29T08:25:11-03:00
slug: "flame-y-md5"
tags: ["computación", "basic", "lenguajes de programación", "historia"]
draft: false
math: false
---
 
En 2005 escribí una [prueba de
concepto](http://www.codeproject.com/Articles/11643/Exploiting-MD5-collisions-in-C)
donde usé una conocida  vulnerabilidad de MD5  descubierta por Xiaoyun
Wang en 2004[^1], para engañar cualquier sistema que valide la firma
digital de un archivo usando MD5. Posteriormente Peter Selinger
desarrolló una mejora de mi esquema lo que permite automatizar aún más
el proceso.

Mi prueba de concepto permite que dos programas distintos (uno "bueno"
y otro "malvado") tengan la misma firma MD5.  Para que funcione mi
esquema se requiere un tercer programa extractor. Sin embargo, Selinger
mejoró mi esquema eliminando este tercer programa. En esencia lo que
hace Selinger es crear un "programa esquizofrénico", que contiene las
dos personalidades del programa (la buena y la malvada).

En 2009 Didier Stevens usó el programa de Selinger para crear dos
programas con la misma firma digital Authenticode, un programa usado por
Microsoft para firmar digitalmente archivos.

Los mismos conceptos fueron usados por Marc Stevens, Arjen K. Lenstra y
Benne de Weger para crear programas que tienen la misma firma digital,
en este caso estos investigadores determinaron un conjunto de bytes que
se deben agregar al final de cada archivo para lograr el efecto.

Lo interesante de todo esto es que estos esquemas han sido usados en la
elaboración del temible virus conocido como
[Flame](http://blogs.elpais.com/cronica-negra/2012/06/virus-flame-la-primera-bomba-atomica-de-la-ciberguerra.html).

[Flame](http://es.wikipedia.org/wiki/Flame_(malware)) aparentemente es
una arma cibernética, al igual que
[Stuxnet](http://es.wikipedia.org/wiki/Stuxnet), cuyo objetivo es atacar
potencias extranjeras, en particular Irán y su programa atómico.

Marc Stevens [investigó el código de Flame](http://www.cwi.nl/news/2012/cwi-cryptanalist-discovers-new-cryptographic-attack-variant-in-flame-spy-malware)
y descubrió que este usa un esquema similar a los descritos para hacer
pasar su código como una actualización válida de Windows:

> The first cryptographic collision attack against the cryptographic
> hash function MD5 was invented by Xiaoyun Wang et al. in 2004 , which
> however did not pose a serious immediate threat due to technical
> limitations. Subsequently, we have devised a more flexible collision
> attack against MD5 in 2007, a so-called chosen-prefix collision attack
> . This posed a greater threat due to the removal of the most important
> technical limitation. Finally, we refined our attack in 2008 and used
> it to construct a rogue Certification Authority, thereby demonstrating
> a serious vulnerability in internet security. Our demonstration
> convinced Microsoft and various governments to raise the security
> standards for Certification Authorities, by disallowing the use of
> MD5-based signatures effective 15 January 2009.

> It is clear that Microsoft, at that time, should have also disallowed
MD5-based signatures in their Terminal Server Licensing Service (TSLS).
As apparently the Flame collision attack was executed in February 2010,
it now turns out they did not; this has been an important oversight. The
result of this collision attack on a Microsoft TSLS Certification
Authority was a code-signing certificate appearing to be from Microsoft
that may be used to sign Windows Updates.  This attack avenue was
essentially open to any knowledgeable attackers since June 2009, when,
under the belief that MD5-based signatures had indeed been disallowed,
we made the program sources for a chosen-prefix collision attack
publicly available. Furthermore, it should be noted that, even without a
collision attack, Microsoft has unsuspectingly been providing its TSLS
customers with unwarranted code-signing abilities.

> We have developed a forensic tool for collision attacks \[7\] that can
efficiently detect a wide range of known and unknown collision attacks
against MD5 as well as MD5\'s successor SHA-1. Moreover, this tool may
also be used to online detect fraudulent certificates constructed using
a collision attack.

Using our forensic tool, we have indeed verified that a chosen-prefix
collision attack against MD5 has been used for Flame. More
interestingly, the results have shown that not our published
chosen-prefix collision attack was used, but an entirely new and unknown
variant. Therefore it is not unreasonable to assume that the particular
chosen-prefix collision attack variant underlying Flame had already been
in development before June 2009. This has led to our conclusion that the
design of Flame is partly based on world-class cryptanalysis. Further
research will be conducted to reconstruct the entire chosen-prefix
collision attack devised for Flame.

Lo que demuestra, una vez más, que no importa cuanta investigación se
haga en criptografía, estos resultados no son adoptados por la industria
hasta que ocurre un desastre\...


[^1]: "How to break MD5 and other hash functions", Xiaoyun Wang and
Hongbu Yu, EUROCRYPT 2005, Lecture Notes in Computer Science, vol. 3494,
Springer, 2005, pp. 19--35.
