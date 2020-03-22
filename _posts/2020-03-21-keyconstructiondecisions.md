---
layout: post
author: Kenar716
title: "Key Construction Decisions"
date: 2020-03-21 12:00:00 +0545
cover: assets/images/posts/2020-03-21-keyconstructiondecisions/decisions.jpg
cover_author_link: https://unsplash.com/photos/IFLgWYlT2fI
cover_author_name: Kyle Glenn
categories: blog
summary:
---
#### Decisiones clave de la construcción de software

Si bien los prerequisitos necesarios para la construcción de software es algo que en parte esta fuera de nuestro control, existen preparaciones que nosotros como programadores o lideres técnicos podemos considerar antes de iniciar el trabajo.

El lenguaje de programación en el cual el sistema será implementado debe de ser de gran interés ya que te encontrarás inmerso en el desde el inicio hasta el final del proyecto.

La selección de un lenguaje de programación afecta la productividad y la calidad del código de varias maneras, los programadores son mas productivos utilizando un lenguaje con el cual se encuentra familiarizados que con uno que no conocen.

En software de alta calidad se puede observar la relación entre la integridad conceptual de la arquitectura y su implementación a bajo nivel, la implementación debe de ser consistente con la arquitectura lo cual lo guía y es consistente de manera interna.

En un programa complejo, las pautas arquitectonicas le dan al programa un balance en su estructura mientras que las pautas de construcción proveen una armonía a bajo nivel, articulando cada clase como una parte fiel del diseño integral. Una clave para la programación exitosa es evitar variaciones arbitrarias para que tu cerebro se pueda enfocar en las variaciones realmente importantes.

Antes de que inicie la construcción, define las convenciones a seguir, los detalles de codificación se encuentran a un nivel tal de precisión que es casi imposible modificarlos o actualizarlos una vez que el software se ha escrito.

Los programadores gastan una cantidad de tiempo significante intentando aprender como funciona un lenguaje en lugar de escribir nuevo código, también gastan incontables horas trabajando en soluciones a bugs en el lenguaje, en el sistema operativo, o en otras herramientas. Los lenguajes de programación en sus inicios de desarrollo tienden a tener ambientes primitivos, o con falta de herramientas en comparación con lenguajes con un mayor tiempo en el mercado o madurez.

Si bien lo anterior parece una recomendación para evitar lenguajes de programación en su etapa inicial, esa no es la intención. Algunas de las aplicaciones innovadoras han surgido de utilizar lenguajes en sus primeras etapas. Lo importante a considerar es el momento en que se encuentra la tecnología a utilizar ya que de ello dependerá el tiempo invertido, ya sea en escribir nuevo código, aprender nuevas características sin documentar, errores de debugging, etcétera.

Los programadores que desarrollan "en" un lenguaje limitan sus pensamientos para construir alrededor de lo que el lenguaje soporta, si las herramientas son primitivas, sus pensamientos tambien lo serán.

Los programadores que desarrollan "dentro" de un lenguaje primero deciden que pensamientos quieren expresar, y luego determinan como expresar sus ideas usando las herramientas proporcionadas por ese lenguaje en especifico.

Comprender la diferencia entre programar en un lenguaje y programar dentro de un lenguaje es critico para entender los principales principios de programación, ya que la mayoría de ellos no son específicos a un lenguaje si no dependen de la forma en que son implementados. Si el lenguaje a utilizar carece de algunas funcionalidades que deseas utilizar o es propenso a otro tipo de problemas, trata de compensarlos. Inventa tus propias convenciones de codificación, estándares, librerías clase, y otras mejoras.

La siguiente lista de verificación resume prácticas específicas que tu deberias decidir de manera conciente para incluirlas o excluirlas durante la construción de software.

### Lista: Principales Prácticas de Construcción.

**Codificación**
 - ¿Haz definido que tanta parte del diseño se hará por adelantado y que tanta parte se realizará mienstras se escribe el código?
 - ¿Haz definido convenciones de código para nombres, comentarios y plantillas?
 - ¿Haz definido practicás de código especificas que son implícitas de la arquitectura, como son las condiciones de errores, como será administrada la seguridad, que convenciones se utilizarán para las clases de interfaces, que estándares se aplicarán para la reutilización de código, que tanto se debe de considerar el desempeño mientras de codifica, entre otras?
 - ¿Haz definido tu ubicación en la tecnología y ajustado tu acercamiento a ella? de ser necesario ¿haz identificado como programarar "dentro" del lenguaje en lugar de estar limiitado tan solo programando "en" el lenguaje?

**Trabajo en equipo**
 - ¿Se han definido los procedimientos de integración -es decir, los pasos especificos a seguir antes de aplicar cambios en el sistema de control de versiones?
 - ¿Los programadores desarrollaran en pares, de manera individual, en una combinación de ambas?

**Control de Calidad (Quality Assurance)**
 - ¿Los programadores escribirán casos de prueba para su código antes de escribir el código en si?
 - ¿Los programadores escribirán pruebas unitarias para su código, ya sea al inicio o al final?
 - ¿Los programadores revisarán su código con un debugger antes de aplicar sus cambios en el sistema de control de código fuente?
 - ¿Los programadores realizarán pruebas de integración antes de aplicar sus cambios?
 - ¿Los programadores revisarán o inspeccionarán el código de otros programadores?

**Herramientas**
 - ¿Haz seleccionado una herramienta para el control de código fuente?
 - ¿Haz seleccionado un lenguaje, su versión de lenguaje y su versión de compilador?
 - ¿Haz seleccionado un framework, o decido de manera explícita no utilizar alguno?
 - ¿Haz decidido si permitir el uso de características no estándares del lenguaje?
 - ¿Haz identificado y adquirido otras herramientas que se utilizarán -editores, herramientas de refactorización, debuggers, frameworks de prueba, revisores de sintaxís, entre otros?

Extracto/resumen del libro _**Code Complete**_ 2nd Edition de **Steve McConnell**, Chapter 4: _Key Construction Decisions_.

Estimado visitante, si haz llegado al final de esta entrada te lo agradezco y te invito a que _**aprendamos algo nuevo juntos...**_