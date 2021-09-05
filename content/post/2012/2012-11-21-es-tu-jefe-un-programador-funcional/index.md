---
title: "¿Es tu jefe un programador funcional?"
date: 2012-11-21T12:25:11-03:00
slug: "es-tu-jefe-un-programador-funcional"
tags: ["programación funcional", "excel"]
draft: false
math: false
---

Probablemente tu jefe, y mi jefe, sin ser informáticos, ni programadores
o ingenieros de software, sean mejores programadores funcionales que tu
mismo, claro, porque es probable que ellos utilicen uno de los lenguajes
funcionales más populares que existen: Excel.

Sí, Excel, ese que usan muchos de tus colegas no informáticos, soporta
perfectamente el paradigma funcional.

Primero en Excel tienes **valores**, números, o a veces textos, que
colocas en celdas. Por ejemplo, puedes colocar en la celda A1 el valor
2, y en la celda A2 el valor 3.

Después tienes **funciones**, u operaciones que trabajan sobre valores
que se encuentran en una celda, por ejemplo, puedes definir que el valor
de la celda A3 se calcula como A3 = A1 \* A2. Excel te mostrará el valor
de aplicar esta operación a los valores disponibles en ese momento en
las celdas A1 y A2, en nuestro caso se verá en A3 el número 6.

{{<figure caption="Definiendo el valor de una celda en función de otras dos" src="Captura-de-pantalla-2012-11-21-a-las-20.54.00.png">}}

Lo \"*interesante\"* es que esta operación  no cambia el valor de las
celdas que son usadas como **argumentos. *\*Esto quiere decir que en
Excel no hay \**efectos laterales**, el resultado de la función sólo
afecta a aquellos que usen el resultado, pero no a los argumentos de
entrada.

Veamos que pasa si agregamos otras ecuaciones a nuestra planilla,
haciendo que unos valores dependan de resultados previos.

Por ejemplo: A4=A1+2, B3=A2*A2, B4=A1-A2, C3 = B3-B4, C4 = B3*B4.

Excel nos permte ver las dependencias de esta secuencia de cálculos:

{{<figure caption="Dependencias entre las celdas" src="Captura-de-pantalla-2012-11-21-a-las-21.03.11.png">}}


Decimos que el orden de evaluación está dado por las dependencias de los
datos.

Otra cosa interesante es que dados los mismos valores de entrada el
resultado final no cambia, en nuestro caso, si A1 contiene el valor 1, y
A2 contiene el valor 2, entonces la celda C4 siempre tendrá el valor -4,
*no hay sorpresas*, el valor de la celda C4 depende sólo de los
argumentos de entrada y la secuencia de cálculos intermedios.

Consideren la siguiente función en C:

```c
int calc(int x, int y) { 
    static int z = 0;
    z = z + x * y;
    return z;
}
```

Si invocamos esta función la primera vez con los valores 1 y 2, el
resultado será 2, pero si lo invocamos por segunda vez, con los
argumentos 2 y 3, el resultado será 8, si la invocamos por tercera vez,
con los valores 1 y 2, ¡el resultado será 10!

Esto pasa porque C permite efectos laterales, en particular al declarar
la variable z como static hace que ese valor se mantenga a lo largo de
cada invocación a la función.

Los lenguajes de programación funcional prohiben esta opción, no pueden
haber efectos laterales como estos, el resultado de la función solo debe
ser el mismo para los mismos argumentos de entrada.

Ahora bien, excel, usada a este nivel, junto con algunas funciones pre
definidas, opera como lenguaje funcional, pero no todo excel es
funcional, por ejemplo, cuando se usan macros, o se crean funciones con
lenguajes de extensión en VBA u otros lenguajes (como C\#).

Pero la mayor parte de los usuarios la usan a este nivel, y sin darse
cuenta, programan usando el paradigma funcional.

Las propiedades más importantes de la programación funcional están
disponibles en Excel a nivel básico. Lo demás, todo lo complicado, que
asusta a tantos programadores, como los combinadores, la monadas, el
currying,  las reducciones, el lambda cálculus, etc, son temas más
avanzados, que a pesar de sus nombres intimidantes, y de la costumbre de
la comunidad funcional de \"hablar en difícil\", son temas perfectamente
abordables por cualquier programador.

Pero si nunca te has animado a aprender la programación funcional,
quizás es hora de que abras una planilla de cálculo y empieces a jugar
con ella, verás que es muy iluminador.

Te propongo los siguientes ejercicios:

-   Calcula la [sucesión de
    Fibonacci](http://es.wikipedia.org/wiki/Sucesi%C3%B3n_de_Fibonacci)
    en Excel

-   ¿Es posible crear funciones recursivas en Excel? (sin usar VB  o
    algún lenguaje de programación para \"extender\" excel).

(Este post [está disponible también en La Sombra de
Dijkstra](https://www.programando.org/blog/2012/11/22/tu-jefe-es-un-programador-funcional.html))
