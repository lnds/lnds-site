---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Tres Buenas Prácticas para gestionar tu Código"
subtitle: "Y cómo automatizarlas"
summary: ""
authors: []
tags: []
categories: []
date: 2020-08-21T07:49:55-04:00
lastmod: 2020-08-21T07:49:55-04:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "version control. Ilustración tomada de undraw.co"
  focal_point: ""
  preview_only: false
  placement: 3

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

Algo importante en un equipo, o en un proyecto abierto (open source), es asegurar la comunicación. Algo que ayuda a mejorarla es mantener una serie de estándares, o prácticas comunes que faciliten la comunicación y el entendimiento mutuo.

Desde hace años las comunidades open source, en diversos proyectos, han adoptado una serie de prácticas muy sencillas, pero poderosas, que ayudan a gestionar mejor su código. 

Entre estas hay tres que me parece  deberían ser adoptadas por los equipos de desarrollo en ambientes corporativos.

Por cierto, estas prácticas funcionan mejor si usas GIT[^1].

## Mantener una bitácora de cambios

La bitácora de cambios, o changelog, es un archivo que describe todos los cambios relevantes en un proyecto.
Hay un proyecto que describe una forma estándar de mantener una bitácora de cambios, se trata de  [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)[^2]

La idea es muy sencilla, debes mantener un archivo llamado `CHANGELOG.md`, que se trata de un simple archivo en 
[markdown](https://en.wikipedia.org/wiki/Markdown) (el mismo formato que usamos para nuestro archivo `README.md`[^3]),
que contiene todos los cambios relevantes, pero descritos en forma correlativa.

Este es un fragmento de un típico archivo `CHANGELOG.md`


    # Changelog
    All notable changes to this project will be documented in this file.

    The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
    and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

    ## [Unreleased]

    ## [1.0.0] - 2017-06-20
    ### Added
    - New visual identity by [@tylerfortune8](https://github.com/tylerfortune8).
    - Version navigation.
    - Links to latest released version in previous versions.
    - "Why keep a changelog?" section.
    - "Who needs a changelog?" section.
    - "How do I make a changelog?" section.
    - "Frequently Asked Questions" section.

Todos los detalles de cómo gestionar este archivo están descritos en el sitio [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), 
así que su lectura es recomendada para tener clariddad de cómo escribir este archivo.

Pero notarán que el archivo marca las versiones según una notación, esta corresponde a Semantic Version, que es la segunda
práctica que les voy a recomendar.

## Versionado Semántico

El versionado semántico es una convención para enumerar las versiones de nuestro software. 
Su definición se mantiene en el sitio [SemVer.org](https://semver.org). Y en principio es muy sencilla.

En SemVer usamos tres números para designar una nueva versión, estos números se separan con un punto, así que el formato es
algo así:

    1.0.1

Al primer número le llamamos MAJOR, al segundo MINOR, y al tercero PATCH. Así que el formato es:

    MAJOR.MINOR.PATCH

- MAJOR: se incrementa cuando se agrega un cambio que es incompatible con versiones anteriores.
- MINOR: se incrementa cuando se agrega funcionalidad, pero sigue siendo compatible con versiones anteriores.
- PATCH: se incrementa cuando se corrigen errores en la versión vigente.

En el ejemplo anterior `1.0.1` podemos entender que corresponde a la versión 1.0 del producto, pero lleva una o varias correcciones
a errores (bugs).

Por cierto hay varios detalles sobre cómo gestionar las versiones, pero la guia en el sitio es bien completa, y se encuentra 
disponible en español también: https://semver.org/lang/es/

## Commits Convencionales

[Conventional Commits](https://www.conventionalcommits.org/) es una forma de escribir los mensajes cada vez que hacemos un commit en GIT de una forma estructurada.

La forma de un commit convencional es la siguiente:

    <tipo>[ámbito opcional]: <descripción>

    [cuerpo opcional]

    [nota de pie opcional]


El <tipo> puede ser al menos uno de estos:

- fix: en que documentamos una corrección
- feat: en que introducimos nuevas características al software
- BREAKING CHANGE: es un cambio que rompe la compatibilidad hacia atrás (y por lo tanto debería afectar el valor MAJOR).


Hay otros posibles tipos: chore, docs, style, refactor, perf, test y otros, que se describen en el sitio oficial de Conventional Commits[^4].

Un ejemplo de un commit convencional[^5]:

    fix(core): corrige algunos errores de tipeo en el nombre de las clases

    Ver el issue para más detalles

    Closes #45



## Automatizar todo lo anterior

Hay herramientas que permiten integrar los commits semánticos, con CHANGELOG.md y SemVer.

Una lista está descrita en el sitio de Semmantic Commits: https://www.conventionalcommits.org/en/v1.0.0/#tooling-for-conventional-commits

La idea es que al usar conventional commits ayudas a estas herramientas a determinar cuál es el siguiente número de versión 
que deberías generar para tu siguiente liberación (versión o release).

Además, estas herramientas mantienen actualizado el archivo CHANGELOG.md.

Mi favorita es una escrita en python, que se llama [commitizen](https://github.com/commitizen-tools/commitizen).

Cuando la instalas y la configuras adecuadamente la herramienta te ayuda a escribir tus commits, y después mantener
actualizado tu número de versión y CHANGELOG.md

![](commitizen.gif)

## Un último tip

Yo siempre recomiendo publicar el número de versión en el front de las aplicaciones. 
A veces puedes crear una página about que contenga un listado de todos los módulos, APIs, usadas, y obtener
el release number de cada una (usando SemVer) y mostrarlo en pantalla.
Esta práctica ayuda mucho a verificar qué versión está instalada en producción y aclarar y resolver
situaciones rápidamente. 
Automatizar el versionado es sencillo usando algo como commitizen, pero además puedes hacer que tu
herramienta de integración continua recoja esa información y la deje disponible en el siguiente `build`
de tu aplicación.

Espero que te sirva esta reseña y difundas estas prácticas en tu equipo, cuéntame si estás usándolas o planeabas 
hacer algo del estilo en tus proyectos.


[^1]: ¿Todavía no usan GIT en tu organización? Vamos, estamos en 2020, si aún están usando algo como SVN, o peor CVS, creo que estás en el lugar inadecuado. Pero peor sería que no usaran control de versiones, ¿no?

[^2]: Está disponible en varios idiomas, este es el enlace a la documentación en español: https://keepachangelog.com/es-ES/1.0.0/

[^3]: Porque en el repositorio de tus fuentes hay un archivo README.md ¿cierto? Si no lo usas, deberías leer esto: https://tom.preston-werner.com/2010/08/23/readme-driven-development.html


[^4]: También hay documentación en español: https://www.conventionalcommits.org/es/v1.0.0-beta.3/

[^5]: Acá he incluido la frase `Closes #45`, que es muy útil si usas los [issues de GitHub](https://guides.github.com/features/issues/)
