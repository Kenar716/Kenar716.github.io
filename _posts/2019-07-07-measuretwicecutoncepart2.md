---
layout: post
author: Kenar716
title: "Measure Twice, Cut Once - Part 2/3"
date: 2019-07-07 12:00:00 +0545
cover: assets/images/posts/2019-07-07-measuretwicecutoncepart2/checklist-requirements.jpg
cover_author_link: https://unsplash.com/photos/UtPC_kz8CAc
cover_author_name: Daniel McCullough
categories: blog
summary:
---
**Prerequisitos para la construcción de software - Parte 2**

La siguiente lista de verificación contiene una serie de preguntas que debemos realizarnos acerca de los requerimientos del proyecto, si bien esta no es una lista exhaustiva nos provee una base sólida para el proceso de construcción de software.

No todas las preguntas son aplicables para todos los proyectos, esto dependerá de la formalidad de este mismo, del tamaño o del contexto.

**Requerimientos Funcionales**
- ¿Todas las entradas al sistema han sido especificadas, incluyendo su fuente, precisión, rango de los valores, y frecuencia?
- ¿Todas las salidas del sistema han sido especificadas, incluyendo sus destino, precisión, rango de valores, y frecuenciia?
- ¿Se han definido todos los formatos de salida para las páginas web, reportes, etcétera?
- ¿Se han especificado todas las interfaces de software y el hardware externo?
- ¿Todas las interfaces de comunicación externas se han especificado, incluyendo _"hand-shake"_, _"error-checking"_, y protocolos de comunicación?
- ¿Todas las tareas que el usuario quiere realizar se han especificado?
- ¿Se han definido los datos a usarse en cada tarea y los datos resultantes de cada una de ellas?

**Requerimientos No Funcionales (Calidad)**
- ¿El tiempo de respuesta esperado, desde el punto de vista de un usuario, se ha definido para todas las operaciones necesarias?
- ¿Existen otras tiempos a considerar, como tiempo de procesamiento, tiempo de transferencia de datos, y tiempos de rendimiento del sistema?
- ¿Se ha especificado el nivel de seguridad?
- ¿Se ha especificado la confiabilidad, incluyendo las consecuencias de fallo del software, la información vital que debe de ser protegida en caso de falla, y la estrategia a seguir en casos de deteccion de errores y recuperación?
- ¿Se ha indicado un mínimo de memoria en el equipo y de capacidad de disco duro?
- ¿La mantenibilidad del sistema, asi com tambien su habilidad para adaptarse a cambios de funcionalidades específicas, cambios en el ambiente operativo, y cambios de las interfaces con otros software se encuentran definidas?
- ¿Existen pautas definidas para indicar el exito del proyecto (o su fracaso)?

**Requerimientos de Calidad**
- ¿Los requerimientos se han escrito en el lenguaje del usuario, que opinión tienen los usuarios al respecto?
- ¿Cada requerimiento evita el conflicto con otros requerimientos?
- ¿Todas las concesiones de atributos en conflicto se han especificado, por ejemplo, entre robustez y corrección?
- ¿Los requerimientos evitan especificaciones de diseño?
- ¿Los requerimientos tiene un nivel detalle suficiente a su contexto? ¿Debería de especificarse con mayor detalle algún requerimiento? ¿Algún requerimiento debería de incluir menos detalles?
- ¿Los requerimientos son lo suficientemente claros para que puedan ser entendidos por un grupo independiente? ¿Que opinan los desarrolladores?
- ¿Cada item es relevante al problema y a su solución? ¿Cada item puede ser rastreado a sus origenes en el ambiente del problema?
- ¿Cada requerimiento es comprobable? ¿Será posible realizar pruebas independiente para determinar cuando cada requerimiento ha sido satisfecho?
- ¿Todos los posibles cambios de los requerimientos se han definido, incluyendo la probabilidad de cambio en ellos?

**Integridad de los Requerimientos**
- ¿Que información no se encuentra disponible antes de que el desarrollo inicie, existen definiciones de areas incompletas?
- ¿Todos los requerimientoss se encuentran completos en el sentido de que si el producto satisface cada requerimiento, será este aceptable?
- _**¿Te encuentras cómodo con todos los requerimientos?**_ ¿Haz eliminado requerimientos que son imposibles de implementar y se han incluido solamente para satisfacer o calmar al cliente o a tu jefe?

En la tercera y última parte de esta serie hablaremos sobre los prerequisitos para la arquitectura de software y la importancia que tiene en la construcción de sistemas.

Extracto/resumen del libro _**Code Complete**_ 2nd Edition de **Steve McConnell**, Chapter 3: _Measure Twice, Cut Once: Upstream Prerequisites_.

Estimado visitante, si haz llegado al final de esta entrada te lo agradezco y te invito a que _**aprendamos algo nuevo juntos...**_