

**Introducción**

A partir del año 1998, a través de un proyecto denominado Congreso visible, el departamento de ciencia política de la Universidad de los Andes realiza un análisis y un seguimiento al congreso de la república estudiando sus actividades legislativas, con el fin de fortalecer y promover la participación ciudadana en los procesos de rendición de cuentas.

Congreso Visible es un proyecto que busca generar un canal de comunicación entre la ciudadanía y sus representantes, de esta manera, este proyecto busca fortalecer el conocimiento en las personas con relación al comportamiento del congreso de la república y en general, de todo el sistema democrático, proporcionando un análisis e información de manera periódica, organizada y de fácil acceso para todo el mundo.

 Parte de la misión del proyecto congreso visible de la Universidad de los Andes, se enfoca en fomentar la participación ciudadana en actividades del sistema democrático monitoreando y provisionando la información sobre el desempeño de los representantes electos (congresistas, entre otros), con el fin de mejorar las prácticas políticas y de culturizar a los ciudadanos sobre el comportamiento del sistema democrática, teniendo en cuenta que ellos valoran la transparencia de aquellos que son elegidos.

 Teniendo en cuenta lo anterior, se presenta una serie de visualizaciones que permiten estudiar el comportamiento del congreso en términos de los proyectos que se radican, inicialmente se presenta una visualización basada en árboles que permite estudiar el estado de los proyectos que se radican  desde las distintas comisiones (de cámara y de senado) y en un periodo de interés, seguidamente, se presentan una serie de gráficos barchart que permiten comparar el número de proyectos (sancionados y archivados) que se radican teniendo en cuenta distintos atributos (por temas, iniciativas, tipo de proyectos y alcance), así mismo, se presentan una serie de gráficos barchart que permiten comparar el tiempo (medido en días) que tarda un proyecto en alcanzar un estado (sancionado ó archivado) teniendo en cuenta distintos atributos (por temas, iniciativas, tipo de proyectos y alcance), finalmente se presenta una visualización basada en redes que permite ver cómo se relacionan los Congresistas entre sí para trabajar las diferentes propuestas en un período específico y filtrando por el estado de los proyectos: sancionados como ley, archivados y otros.

**Metodología**

**Recolección de los datos:** Los datos fueron generados por el cliente (congreso visible) y estos fueron entregados en un archivo de Excel, estos datos contienen la información de los proyectos que se han presentado en los últimos cuatro cuatrienios.

**Entendimiento del problema:** A partir de una serie de reuniones con el cliente, se estableció el problema que se busca solucionar por medio de una visualización.

**Procesamiento de los datos:  ** Los datos fueron procesados en Python con el fin de obtener la información necesaria para la construcción de las visualizaciones.

**Visualizaciones:** Las visualizaciones se construyeron utilizando javascript d3 v.4 y v.5.

**Despliegue:** El despliegue de todas las visualizaciones se realizó utilizando github.

**Visualización 1 basada en árboles**

La siguiente visualización busca presentar los proyectos que se presentan desde las distintas comisiones observando múltiples características a través de un gráfico basado en árboles.

 ![alt text](https://i.ibb.co/mtjVZnx/tree.jpg)

A continuación, se describe esta visualización en términos del Framework de Tamara

**What**

**Tipo de conjunto de datos:** Redes

**Atributos**

- **Comisión entrante:** Corresponde a la comisión que presenta el proyecto, esta variable es categórica.
- **Iniciativa:** Corresponde a las iniciativas del proyecto, esta variable es categórica.
- **Estado:** Esta variable permite identificar si un proyecto es sancionado o archivado, esta variable es categórica.
- **Id del proyecto:** Esta variable permite identifica el proyecto, esta variable es categórica.
- **Fecha de radicación:** Esta variable permite identificar la fecha en la cual se radicó el proyecto, esta variable es cuantitativa secuencial.

**Why**

A continuación, se describe las tareas principales que se busca realizar a partir de esta visualización.

**Tareas principales**

1. Identificar el estado de un proyecto radicado a través de las distintas comisiones (Tamara: Identify, feature).
2. Identificar la cantidad de proyectos archivados o sancionados, presentados por las diferentes comisiones (Tamar: Identify, feature)
3. Encontrar la ruta de un proyecto determinado desde su radicación (Tamara: Identify path)

**How**

A continuación, se describe la visualización

**Marcas:** Los puntos representan los nodos (y en estos se ubican las comisiones entrantes, la iniciativa del proyecto, el estado y el id) del árbol y las líneas representan los enlaces.

**Canales:** Cada nodo tiene un tamaño determinado, aquellos que no tienen asociado ningún proyecto, son más pequeños, por otra parte, la posición espacial horizontal permite evidenciar una jerarquía en el árbol, aunque esta no representa ningún atributo.

**Manipulación:** Esta visualización contiene un browser el cual permite seleccionar el rango de tiempo de interés, por otra parte, al seleccionar un nodo de interés, se despliegan los nodos hijos.

**Insights obtenidos de esta visualización**

- Gran cantidad de proyectos son archivados por tránsito de legislatura, por iniciativa legislativa y por las comisiones de las cámaras de representantes.



**Visualización 2 basada en barcharts**

A continuación, se presenta una visualización que permite comparar el número de proyectos presentados por distintas categorías de un atributo de interés (por tema, iniciativa, alcance, tipo de proyecto y por comisión entrante) y en un periodo de tiempo determinado, de la misma manera se busca estudiar el tiempo que toma un proyecto en alcanzar un estado por distintas categorías de un atributo (por tema, iniciativa, alcance, tipo de proyecto y comisión entrante) y en un periodo de tiempo determinado.

 ![alt text](https://i.ibb.co/cvtGs8r/bar1.jpg)
 
A continuación, se realiza una descripción de esta visualización en términos del Framework de Tamara

**What**

**Tipo de conjunto de datos:** Temporales

**Atributos**

- **Tiempo promedio:** Corresponde al tiempo promedio que demora un proyecto en alcanzar un estado (archivado o sancionado), esta variable en cuantitativa y secuencial.
- ** Alcance:** Corresponde al alcance del proyecto, esta variable es categórica.
- **Tipo de proyecto:** Corresponde al tipo de proyecto, esta variable es categórica.
**Comisión entrante:** Corresponde a la comisión que presenta el proyecto, esta variable es categórica.
- **Iniciativa:** Corresponde a la iniciativa del proyecto, esta variable es categórica.
**Tema:** Corresponde al tema del proyecto, esta variable es categórica.


**Why**

A continuación, se describen las tareas principales y secundarias que se quieren realizar a través de esta visualización

**Tareas principales:**

1. Comparar el número de proyectos archivados presentados en un período dado (cuatrienio específico) por tema, por comisión entrante (cámara o senado), alcance, tipo de proyecto e iniciativa ( **Tamara: Compare, Features** ).
2. Comparar el número de proyectos sancionados presentados en un período dado (cuatrienio específico) por tema, por comisión entrante (cámara o senado), alcance, tipo de proyecto e iniciativa ( **Tamara: Compare, Features** ).
3. Comparar el tiempo que tarda un proyecto en ser sancionado en un periodo dado (cuatrienio específico), por tema, por comisión entrante (cámara o senado), alcance, tipo de proyecto e iniciativa ( **Tamara: Compare, Features** ).
4. Comparar el tiempo que tarda un proyecto en ser archivado en un periodo dado (cuatrienio específico), por congresista, por partido político, por tema, por comisión de cámara y por comisión de senado ( **Tamara: Identify, Features** )

**Tareas secundarias**

1. Derivar el número de proyectos presentados por comisión entrante, alcance, tipo de proyecto e iniciativa (Tamara: Derive, Features).
2. Derivar el tiempo promedio que toma un proyecto en ser archivado por comisión entrante, alcance, tipo de proyecto e iniciativa (Tamara: Derive, Features).
3. Derivar el tiempo promedio que toma un proyecto en ser sancionado por comisión entrante, alcance, tipo de proyecto e iniciativa (Tamara: Derive, Features).

**How**

A continuación, se describe los elementos que conforman la visualización.

Para las tareas 1, como se desea comparar el número de proyectos presentados en un periodo determinado (cuatrienio específico), por tema, por comisión entrante (cámara o senado), alcance, tipo de proyecto e iniciativa, se propone construir un conjunto de gráficos de barras, a continuación, se presenta la descripción de las marcas y canales asociadas a estas visualizaciones.

**Marcas:** Líneas

**Canales:  **

- La variable número de proyectos presentados tendrá una posición vertical (express value attribute with aligned vertical position).
- La variable tema/congresista/comisión entrante/ iniciativa/ alcance tendrá una posición horizontal (separate key attribute with horizontal position.).

Así mismo, esta visualización contiene un filtro que permitirá comparar el número de proyectos presentados a través de un atributo de interés.

A manera de observación, para las tareas 2,3 y 4 se utiliza el mismo modismo.

**Insights obtenidos de esta visualización**

- En el periodo 2002-2006, el mayor número de proyectos archivados fueron de celebración, honores y monumentos, por otra parte, el menor número de proyectos archivados en este periodo fueron de juegos de azar.
-  En el periodo 2006-2010, el mayor número de proyectos archivados fueron de celebración, honores y monumentos, por otra parte, el menor número de proyectos radicados en este periodo fueron de PND (plan nacional de desarrollo)
-  En el periodo 2014-2010, el mayor número de proyectos archivados fueron de seguridad social y salud, por otra parte, el menor número de proyectos archivados en este periodo fueron de corrupción.
-  En el periodo 2014-2018, el mayor número de proyectos archivados fueron de justicia, por otra parte, el menor número de proyectos archivados en este periodo fueron de desastres y calamidades.
-  En el periodo 2002-2006, el mayor número de proyectos sancionados son de celebración, honores y monumentos, por otra parte, el menor número de proyectos sancionados son de vivienda.
-  En el periodo 2006-2010, el mayor número de proyectos sancionados son de política internacional, por otra parte, el menor número de proyectos sancionados son de vivienda.
-  En el periodo 2010-2014, el mayor número de proyectos sancionados son de celebración, honores y monumentos, por otra parte, el menor número de proyectos sancionados son de rama legislativa.
-   En el periodo 2014-2018, el mayor número de proyectos sancionados son de celebración, honores y monumentos, por otra parte, el menor número de proyectos sancionados son de rama judicial.
- En el periodo 2002-2006, los proyectos de desastre y calamidades son los que más se demoran en ser archivados, por otra parte, los proyectos de derechos humanos son los que menos se demoran en ser archivados.
- En el periodo 2006-2010, los proyectos de mujer son los que más se demoran en ser archivados, por otra parte, los proyectos de partidos y movimientos son los que menos se demoran en ser archivados.
- En el periodo 2010-2014, los proyectos de notariado y registro son los que más se demoran en ser archivados, por otra parte, los proyectos de derechos de autor son los que menos se demoran en ser archivados.
- En el periodo 2014-2018, los proyectos de seguridad social y salud son los que más se demoran en ser archivados, por otra parte, los proyectos de rama ejecutiva son los que menos se demoran en ser archivados.
- En el periodo 2002-2006, los proyectos de derechos fundamental son los que más tiempo tomaron en ser sancionados, por otra parte, los proyectos de presupuestos son los que menos tiempo tomaron en ser sancionados.
-  En el periodo 2006-2010, los proyectos de familia son los que más tiempo tomaron en ser sancionados, por otra parte, los proyectos de presupuesto son los que menos tiempo tomaron en ser sancionados
- En el periodo 2010-2014, los proyectos de bienestar y pobreza son los que más tiempo tomaron en ser sancionados, por otra parte, los proyectos de presupuesto son los que menos tiempo tomaron en ser sancionados
-  En el periodo 2014-2018, los proyectos de familia son los que más tiempo tomaron en ser sancionados, por otra parte, los proyectos de rama judicial son los que menos tiempo se tomaron en ser sancionados.

**Visualización 3 basada en redes**

Esta visualización permite ver cómo los autores (representados por los círculos o nodos) trabajan en conjunto una propuesta en un período legislativo.

![alt text](https://i.ibb.co/HHXjVPm/red1.jpg)

A continuación, se realiza una descripción de esta visualización en términos del Framework de Tamara:

**What**

Tipo de dataset: Redes

Tipos de datos: Items (nodos: Congresistas), links (conexiones entre Congresistas que trabajan en conjunto proyectos) y atributos como:

|
- id\_congresista: Identificador único del congresista. Variable cuantitativa - secuencial
 |
| --- |
|
- Congresista: Nombre del Senador o Representante a la Cámara. Variable Cuantitativa
 |
|
- Cuatrienio: Periodo legislativo. Variable categórica
 |
|
- Partido: Partido político del cual hace parte un Congresista. Variable categórica
 |
|
- Cámara: Indica si el Congresista pertenece a la Cámara o Senado. Variable categórica
 |
|
- id\_del\_proyecto: Identificador único del proyecto. Variable cuantitativa - secuencial
 |
|
- estado\_actual: Estado en el cual se encuentra un proyecto. Variable categórica
Atributos Derivados:  |

- Total proyectos presentados por cada Congresista. Variable cuantitativa
- Total proyectos sancionados como ley por Congresista.  Variable cuantitativa
- Total proyectos archivados por Congresista. Variable cuantitativa
- Total proyectos en otros estados por Congresista. Variable cuantitativa
- Total proyectos en conjunto entre Congresistas.Variable cuantitativa.

**Why**

A continuación, se describen las tareas principales y secundarias que se quieren realizar a través de esta visualización:

**Tarea principal:**

1. Navegar o explorar por diferentes comunidades que se pueden ver al relacionar los autores que trabajan juntos para presentar proyectos en el Congreso. **(Explore - Topologys)**

**Tareas secundarias:**

1. Identificar aquellos autores que más proyectos han logrado Sancionar como Ley (Identify – Features)
2. Buscar aquellas comunidades o agrupaciones en un  período específico de tiempo para mirar cuáles características presentan. (Browse – Features).
3. Identificar aquellos autores que no muestran relaciones comunes con los demás Congresistas (Identify – Outliers).

**How**

A continuación, se describen los elementos que conforman la visualización.

**Marcas:**

- Líneas que representan la Conexión entre los Congresistas que trabajan en conjunto una propuesta.
- Puntos que representan los nodos Congresistas.

      **Canales:  **

- Posición espacial: para la distribución de los nodos y enlaces en el svg.
- Color hue: Para representar los partidos políticos. Separate, order.
- Ancho de la línea que representa la cantidad de proyectos trabajados en conjunto entre dos personas. Express
- El tamaño del nodo representa el número de proyectos radicados, sancionados, archivados por un Congresista. Express

**Manipulación:** Esta visualización permite seleccionar nodos o congresistas específicos y navegar por la red.

**Reducción:** Se utilizan filtros por período y estado del proyecto.

**Insights obtenidos de esta visualización**

- En el cuatrienio 2002-2006, se observa que en cuanto a los proyectos sancionados como Ley existía la participación de Congresistas que pertenecían a diferentes partidos, si ya miramos el año 2014-2018, se ve que éstos proyectos Sancionados ya tienden a ser aquellos propuestos por Congresistas que pertenecen a un único partido.
- El congresista que más proyectos presenta no es al que más proyectos le sancionaron como ley, por ejemplo, para el período 2014-2018 el congresista que más proyectos radicó fue Carlos Eduardo Guevara Villabón con 109 proyectos del partido MIRA y aprobados 6, mientras que fue la Congresista María del Rosario Guerra de la Espriella del partido Centro Democrático quien logró que se sancionaran el mayor número de proyectos en dicho período, 11 en total de 83 proyectos radicados.
- Vemos el caso del Senador Jaime Alejandro Amin Hernandez (periodo 2014-2018) siendo del partido de la U trabajó más en conjunto con Congresistas del partido Centro Democrático los proyectos que fueron sancionados.
- Existen Congresistas como Álvaro Uribe Vélez, Alfredo Ramos Maya y María del Rosario Guerra de la Espriella, que para el período 2014-2018 trabajaron el mayor número de proyectos en conjunto, en total 9.



**COMO EJECUTARLO**

Para ejecutar esta visualización se requiere de los siguientes aspectos:

- Un conjunto de datos correspondientes a las &quot;Autorías&quot; del congreso de la república de Colombia, suministrado por Congreso Visible de la Universidad de los Andes Colombia.

- Para las visualizaciones de Árbol y de Barras se debe el set de Datos debe ser csv, entre tanto para la visualización tipo Red se requiere la trasformación a formato Json.

- Para navegar por las diferentes visualizaciones hacer uso del Menú:
  - Flujo Proyectos:

Despliegue la Jerarquía de un proyecto por las características seleccionadas en un árbol desplegable, con opción de búsqueda por contenido o por ID de proyecto.

-
  - Proyectos por Estado:

Despliegue el comportamiento global de los proyectos sancionados y archivados por periodos y temas.

-
  - Proyectos por Tiempo:

Despliegue de los tiempos en la gestión de los proyectos seleccionable por categorías.

Comportamiento Congreso:

Despliegue del grado de cohesión de congreso en forma de Red, utilizando la simulación de fuerzas entre partidos, proyectos y autores.

- El proyecto se encuentra disponible en GitHub, ver links.

**LINKS**

- Link página:

[https://ricarsant.github.io/CongresoCol/](https://ricarsant.github.io/CongresoCol/)

- Link repositorio:

[https://github.com/ricarsant/CongresoCol](https://github.com/ricarsant/CongresoCol)

- Link diapositivas:
-  [https://docs.google.com/presentation/d/e/2PACX-1vRY50nShH64cEAkNOOYUghIRsbgxkytuoESdoWJKhe2zO4hKeLQnvNDRzCULHkFU\_Rem8TyuFvH0KEr/pub?start=false&amp;loop=false&amp;delayms=3000](https://docs.google.com/presentation/d/e/2PACX-1vRY50nShH64cEAkNOOYUghIRsbgxkytuoESdoWJKhe2zO4hKeLQnvNDRzCULHkFU_Rem8TyuFvH0KEr/pub?start=false&amp;loop=false&amp;delayms=3000)

- Link Video insight: [https://www.youtube.com/watch?v=9tPimc7mCdQ&amp;feature=youtu.be](https://www.youtube.com/watch?v=9tPimc7mCdQ&amp;feature=youtu.be)

- Link video Demo: [https://www.youtube.com/watch?v=8IpKkZsaTVg&amp;feature=youtu.be](https://www.youtube.com/watch?v=8IpKkZsaTVg&amp;feature=youtu.be)

- Link Twitter:

[https://twitter.com/yagomezm/status/1069763601257369600](https://twitter.com/yagomezm/status/1069763601257369600)

**Autores**

- Yenny Astrid Gomez Moreno :    Universidad de los Andes
- Harry Cristhian Torres Moreno:   Universidad de los Andes
- Ricardo Jaime Santacruz Garzon: Universidad de los Andes

