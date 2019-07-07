---
layout: post
author: Kenar716
title: "Measure Twice, Cut One - Part 1"
date: 2019-07-06 12:00:00 +0545
categories: blog
summary:
---
**Prerequisitos para la construcción de software**

La frase "Mide dos veces, corta una vez" es muy relevante en el proceso de desarrollo de software, ya que una mala definición de requisitos elevaran el costo, gran parte del éxito o fracaso de un proyecto ha sido determinado antes de que la construcción inicie. Si las bases no han sido bien cimentadas o si la planeación es inadecuada, lo mejor que se puede realizar durante la construcción es mantener el daño al mínimo. 

Cada tipo de proyecto de software tiene un balance diferente entre las preparaciones y la construcción, cada proyecto es único, pero los proyectos tienden a caer dentro de estilos de desarrollo generales. 

<table class="table table-sm table-striped table-bordered table-responsive align-items-center text-center small">
    <colgroup >
        <col width="25%" />
        <col width="25%" />
        <col width="25%" />
        <col width="25%" />
    </colgroup>
    <thead>
        <tr>
            <th colspan="4" class="table-active text-center">Buenas prácticas para los tres tipos de Software mas comunes</th>
        </tr>
        <tr>
            <th></th>
            <th class="text-center">De Negocio</th>
            <th class="text-center">De Misión Crítica</th>
            <th class="text-center">Embebidos</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td markdown="span" rowspan="6" class="table-inverse">Aplicaciones Típicas</td>
            <td markdown="span">Sitios de Internet</td>
            <td markdown="span">Software Embebido</td>
            <td markdown="span">Software de Aereonaútica</td>
        </tr>
        <tr>
            <td markdown="span">Sitios de Intranet</td>
            <td markdown="span">Juegos</td>
            <td markdown="span">Software Embebido</td>
        </tr>
        <tr>
            <td markdown="span">Sistemas de Inventario</td>
            <td markdown="span">Sitios de Internet</td>
            <td markdown="span">Dispositivos Médicos</td>
        </tr>
        <tr>
            <td markdown="span">Juegos</td>
            <td markdown="span">Paquetes de Software</td>
            <td markdown="span">Sistemas Operativos</td>
        </tr>
        <tr>
            <td markdown="span">Sistemas de Administración de Información</td>
            <td markdown="span">Herramientas de Software</td>
            <td markdown="span">Paquetes de Software</td>
        </tr>
        <tr>
            <td markdown="span">Sistemas de Pago</td>
            <td markdown="span">Servicios Web</td>
            <td markdown="span"></td>
        </tr>
        <tr>
            <td markdown="span" rowspan="3" class="table-inverse">Modelos de Ciclos de Vida</td>
            <td markdown="span">Desarrollo Agil (Programación Extrema, Scrum, etc.)</td>
            <td markdown="span">Entrega en etapas</td>
            <td markdown="span">Entrega en etapas</td>
        </tr>
        <tr>
            <td markdown="span">Prototipado evolutivo</td>
            <td markdown="span">Entrega evolutiva</td>
            <td markdown="span">Desarrollo en espiral</td>
        </tr>
        <tr>
            <td markdown="span"></td>
            <td markdown="span">Desarrollo en espiral</td>
            <td markdown="span">Entrega evolutiva</td>
        </tr>
        <tr>
            <td markdown="span" rowspan="4" class="table-inverse">Planificicación y Administración</td>
            <td markdown="span">Planeación de proyecto incremental</td>
            <td markdown="span">Planeación básica</td>
            <td markdown="span">Planeación exhaustiva</td>
        </tr>
        <tr>
            <td markdown="span">Planeación de pruebas y aseguramiento de calidad conforme se requiera</td>
            <td markdown="span">Planeación de pruebas básicas</td>
            <td markdown="span">Planeación de pruebas exhaustiva</td>
        </tr>
        <tr>
            <td markdown="span">Control de cambios informal</td>
            <td markdown="span">Planeación de aseguramiento de calidad conforme se requiera</td>
            <td markdown="span">Aseguramiento de calidad exhaustivo</td>
        </tr>
        <tr>
            <td markdown="span"></td>
            <td markdown="span">Control de cambios formal</td>
            <td markdown="span">Control de cambios riguroso</td>
        </tr>
        <tr>
            <td markdown="span" rowspan="2" class="table-inverse">Requerimientos</td>
            <td markdown="span">Especificación de requerimientos informal</td>
            <td markdown="span">Especificación de requerimientos semi-informal</td>
            <td markdown="span">Especificación de requerimientos formal</td>
        </tr>
        <tr>
            <td markdown="span"></td>
            <td markdown="span">Revisión de requerimientos conforme se requiera</td>
            <td markdown="span">Inspección de requerimientos formal</td>
        </tr>
        <tr>
            <td markdown="span" rowspan="4" class="table-inverse">Diseño</td>
            <td markdown="span">Diseño y codificación combinadas</td>
            <td markdown="span">Diseño arquitectónico</td>
            <td markdown="span">Diseño arquitectónico</td>
        </tr>
        <tr>
            <td markdown="span"></td>
            <td markdown="span">Detalles del diseño informales</td>
            <td markdown="span">Inspecciones formales de la arquitectura</td>
        </tr>
        <tr>
            <td markdown="span"></td>
            <td markdown="span">Revisión del diseño conforme se requiera</td>
            <td markdown="span">Diseñado detallado formal</td>
        </tr>
        <tr>
            <td markdown="span"></td>
            <td markdown="span"></td>
            <td markdown="span">Inspecciones formales del diseño detallado</td>
        </tr>
        <tr>
            <td markdown="span" rowspan="3" class="table-inverse">Construcción</td>
            <td markdown="span">Programación en partes o codificación individual</td>
            <td markdown="span">Programación en partes o codificación individual</td>
            <td markdown="span">Programación en partes o codificación individual</td>
        </tr>
        <tr>
            <td markdown="span">Procedimiento de "check-in" informal o sin procedimiento</td>
            <td markdown="span">Procedimiento de "check-in" informal</td>
            <td markdown="span">Procedimiento formal "check-in"</td>
        </tr>
        <tr>
            <td markdown="span"></td>
            <td markdown="span">Revisiones de código conforme se requieran</td>
            <td markdown="span">Inspecciones formales de código</td>
        </tr>
        <tr>
            <td markdown="span" rowspan="4" class="table-inverse">Pruebas y Aseguramiento de Calidad</td>
            <td markdown="span">Los desarrolladores prueban su propio código</td>
            <td markdown="span">Desarrollo guiado por pruebas</td>
            <td markdown="span">Pocas pruebas o sin pruebas de un grupo independiente</td>
        </tr>
        <tr>
            <td markdown="span">Los desarrolladores prueban su propio código</td>
            <td markdown="span">Desarrollo guiado por pruebas</td>
            <td markdown="span">Grupo independiente de pruebas</td>
        </tr>
        <tr>
            <td markdown="span">Los desarrolladores prueban su propio código</td>
            <td markdown="span">Desarrollo guiado por pruebas</td>
            <td markdown="span">Grupo independiente de pruebas</td>
        </tr>
        <tr>
            <td markdown="span"></td>
            <td markdown="span"></td>
            <td markdown="span">Grupo independiente de aseguramiento de calidad</td>
        </tr>
        <tr>
            <td markdown="span" class="table-inverse">Despliegue</td>
            <td markdown="span">Procedimiento de despliegue informal</td>
            <td markdown="span">Procedimiento de desgliegue formal</td>
            <td markdown="span">Procedimiento de desgliegue formal</td>
        </tr>

    </tbody>
</table>

Un proyecto con el enfoque secuencial se basa solamente en las pruebas para descubrir sus defectos, la mayoría de los correcciones se realizan al final creando costos mayores, mientras que un enfoque iterativo los descubre conforme se progresa, por lo tanto se retrabaja conforme se descubren y lo cual genera un costo menor. 

Para determinar el mejor tipo de enfoque para el proyecto se recomiendan los siguientes lineamientos. 

<table class="table table-striped table-bordered table-responsive align-items-center small">
    <colgroup >
        <col width="50%" />
        <col width="50%" />
    </colgroup>
    <thead>
        <tr>
            <th>Secuencial</th>
            <th>Iterativo</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td markdown="span">Los requerimientos son lo bastante estables.</td>
            <td markdown="span">Los requisitos no se entienden bien o se espera que sean inestables por otras razones.</td>
        </tr>
        <tr>
            <td markdown="span">El diseño es sencillo y se ha entendido bastante bien.</td>
            <td markdown="span">The diseño es complejo, desafiante, o ambos.</td>
        </tr>
        <tr>
            <td markdown="span">El equipo de desarrollo esta esta familiarizado con el area de aplicación</td>
            <td markdown="span">The equipo de desarrollo no está familiarizado con el area de aplicación.</td>
        </tr>
        <tr>
            <td markdown="span">El proyecto tiene pocos riesgos.</td>
            <td markdown="span">The proyecto contiene grandes riesgos.</td>
        </tr>
        <tr>
            <td markdown="span">La previsibilidad a largo plazo es importante.</td>
            <td markdown="span">La previsibilidad a largo plazo no es importante.</td>
        </tr>
        <tr>
            <td markdown="span">El costo de cambiar los requerimientos, el diseño, y el código es alto.</td>
            <td markdown="span">El costo de cambiar los requerimientos, el diseño, y el código es probablemente bajo.</td>
        </tr>
    </tbody>
</table>

El primer prerequisito que se debe de cumplir antes de iniciar la construccion de software es definir de manera clara cual es el problema que el sistema se supone va a resolver. 

![code-complete-2](/assets/images/posts/2019-07-06-measuretwicecutoncepart1/PiramidaConstruccion.PNG){: .center-image }

La definición del problema nos indica que cual es el problema que enfrentamos sin ninguna referencia posible a una solución, es un enunciado simple y debe de sonar como un problema, la definición del problema debe de estar en el lenguaje del usuario, y los problemas deben de ser descritos desde el punto de vista de un usuario, usualmente no deben de contener terminos técnicos o computacionales, salvo el contexto lo requiera como tal. 

Establecer un conjunto de requerimientos explícitos es importante por varias razones, nos ayudan en asegurar que el usuario en lugar del desarrollador dirijan la funcionalidad del sistema. Si los requerimientos son explícitos, el usuario puede revisar y aceptar los cambios, si no son explícitos, el desarrollador usualmente termina tomando decisiones sobre los requerimientos durante la codificación. Los requerimientos explícitos evitan estar adivinando lo que el usuario realmente quiere, además tambien ayudan a evitar argumentos cuando el equipo de desarrollo tiene discrepancias sobre lo que el sistema se supone que hara ya que estos se puede resolver al verificar la lista de requerimientos. 

Algunas recomendaciones a seguir para el cambio de requerimientos durante la construcción del software son las siguientes: 
- Que los requimientos cumplan la calidad usando la lista de verificacion siguiente. 
- Asegurarse que todo el mundo entienda el costo de cambiar los requerimientos. 
- Establecer un procedimiento de control de cambios. 
- Usar estilos de desarrollo que se faciliten los cambios. 
- Abandonar el proyecto. 
- Mantener un ojo en las oportunidades de negocio del proyecto. 

Extracto del libro _**Code Complete**_ 2nd Edition de **Steve McConnell**, Chapter 3: _Measure Twice, Cut Once: Upstream Prerequisites_.

Estimado visitante, si haz llegado al final de esta entrada te lo agradezco y te invito a que _**aprendamos algo nuevo juntos...**_