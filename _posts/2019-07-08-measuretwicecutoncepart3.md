---
layout: post
author: Kenar716
title: "Measure Twice, Cut Once - Part 3/3"
date: 2019-07-08 12:00:00 +0545
cover: assets/images/posts/2019-07-08-measuretwicecutoncepart3/architecture-design.jpg
cover_author_link: https://unsplash.com/photos/-FPFq_trr2Y
cover_author_name: Daniel McCullough
categories: blog
summary:
---
**Prerequisitos para la construcción de software - Parte 3**

La arquitectura de software es una parte de alto nivel del diseño de software, es el marco que sostiene las partes mas detalladas del diseño, una arquitectura bien pensada provee la estructura necesaria para mantener la integridad conceptual de todos los componentes del software. 

La arquitectura provee una guía para lo desarrolladores a un nivel de detalle apropiado a sus habilidades y del trabajo a realizar, asi como tambien separa el trabajo de manera que multiples desarrolladores o equipos puedan trabajar de manera independiente.

Una buena arquitectura hace una construcción fácil, una mala arquitectura hace la construción casi imposible.

Los cambios arquitectónicos son costosos de realizar durante y despúes de la construcción. El tiempo necesario para corregir un error arquitectónico se encuentra al mismo nivel que la corrección de un error de requerimientos, y mucho mas costoso que la corrección de un error de codificación. Los cambios en la arquitectura al igual que los cambios de requerimientos incluso si son pequeños pueden tener un gran alcance.

Muchos componentes son comunes para la buena arquitectura de sistemas, la siguiente lista muestra algunos componentes arquitectónicos a considerar, ya sea si nosotros mismos definimos la arquitectura o bien si está fue definida por alguien más.

- Organización del programa
- Clases mayores
- Diseño de datos
- Reglas de negocio
- Diseño de interfaz de usuario
- Administración de recursos
- Seguridad
- Desempeño
- Escalabilidad
- Interoperabilidad
- Internacionalización/Localización
- Entradas/Salidas
- Procesamiento de errores
- Tolerancia a fallos
- Viabilidad arquitectónica
- Sobre-engeniería
- Decisiones de Compra -vs Construcción
- Decisiones de reusabilidad
- Cambio de estrategia

Una buena especificación de arquitectura esta caracterizada por las discusiones de las clases en el sistema, de la información oculta en cada clase, y de la racionalización por incluir o excluir los posibles diseños alternativos, una buena arquitectura debe de encajar en el problema. 

Los objetivos de la arquitectura deben de estar claramente definidos. El diseño para un sistema en donde su principal objetivo es la modificabilidad será diferente de un sistema en donde su principal objetivo sea el desempeño, incluso si ambos sistemas tienen la misma función. 

La arquitectura debe de describir las motivaciones para las decisiones mayores, y no simplemente justificarlo con frases del tipo “siempre se ha realizado de esa manera”. 

La aquitectura debe de identificar de manera explícita las áreas de riesgo, debe de explicar por que son peligrosas y que pasos se han realizado para mitigar dicho riesgo. 

La siguiente lista de verificación muestra una serie de cuestionamientos que una buena arquitectura debe de abordar, esta lista es una referencia para evaluar el contenido de los de las especificaciones arquitectónicas realizadas.

**Tópicos Específicos de la Arquitectura**
- ¿Es clara la organización general del programa, incluyendo un buen panorama arquitectónico y su justificación?
- ¿Se han definido los bloques de construcción mayores, incluyendo sus áreas de responsabilidad y sus interfaces con otros bloques de construcción?
- ¿Todas las funciones enumeradas en los requerimientos se han cubierto de manera sensata, ni por demasiados ni por muy pocos bloques de construcción?
- ¿Se han descrito y justificado la mayoría de las clases críticas?
- ¿Se ha descrito y justificado el diseño de los datos?
- ¿Se ha especificado el contenido y la organización de la base de datos?
- ¿Se han identificado las reglas clave del negocio y su impacto en el sistema descrito?
- ¿Se ha descrito una estrategia para el diseño de la interfaz de usuario?
- ¿Se ha modularizado la interfaz de usuario de manera tal que los cambios no afectarán el resto del programa?
- ¿Se ha descrito y justificado la estrategia para al manejo de las entradas y salidas?
- ¿Se han descrito y justificado las estimaciones de uso de recursos, asi como tambien una estrategia para la administración de recursos, y recursos escasos como subprocesos, conexiones de base de datos, identificadores, ancho de banda de la red, etc.?
- ¿Se han descrito los requerimientos de seguridad de la arquitectura?
- ¿La arquitectura establece el espacio y los presupuestos de velocidad para cada clase, subsistema o área de funcionalidad?
- ¿La arquitectura describe cómo se logrará la escalabilidad?
- ¿La arquitectura aborda la interoperabilidad?
- ¿Se ha descrito una estrategia para la internacionalización/localización?
- ¿Se ha previsto una estrategia coherente para el manejo de errores?
- ¿Se ha definido un enfoque de tolerancia a fallos (si es necesariio)?
- ¿Se ha establecido la factibilidad técnica de todas las partes del sistema?
- ¿Se ha especificado un enfoque para la sobreingeniería?
- ¿Se han incluido las decisiones necesarias de compra -vs- construcción?
- ¿La arquitectura describe cómo se reusara código para cumplir otros objetivos arquitectónicos?
- ¿La arquitectura está diseñada para adaptarse a posibles cambios?

**Calidad General de la Arquitectura**
- ¿La arquitectura considera todos los requerimientos?
- ¿Alguna parte de la arquitectura se ha sobre especificado o se ha definido pobremente? ¿Se han establecido las expectativas de manera explícita en esta área?
- ¿Se enlaza conceptualmente toda la arquitectura?
- ¿El diseño de alto nivel es independiente de la computadora y del lenguaje que se utilizará para implementarlo?
- ¿Se proporcionan las motivaciones para todas las decisiones importantes?
- _**¿Tú,**_ como el programador que implementará el sistema, _**estás cómodo con la arquitectura?**_

Extracto/resumen del libro _**Code Complete**_ 2nd Edition de **Steve McConnell**, Chapter 3: _Measure Twice, Cut Once: Upstream Prerequisites_.

Estimado visitante, si haz llegado al final de esta entrada te lo agradezco y te invito a que _**aprendamos algo nuevo juntos...**_