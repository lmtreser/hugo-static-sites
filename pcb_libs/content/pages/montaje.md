---
title: "Montaje Final de las Placas"
date: 2024-02-09T10:49:34-03:00
draft: false
weight: 5
---

## Inserción de componentes

Las tareas de insertar los componentes y soldarlos se llevarán a cabo más fácilmente si se dispone de un bastidor de trabajo para sujetar PCBs durante el montaje, pues lleva una tapa articulada forrada de gomaespuma para inmovilizar los componentes. En su defecto vale un tornillo de banco abatible o un pequeño robot.

![](../img/b30d9b17.jpg#center)

Antes de realizar la inserción de componentes en los orificios de la tarjeta procederemos al preformado de sus terminales. Se trata de doblarlos a la medida adecuada o de cortarlos. Lo podemos hacer manualmente con herramientas diseñadas al efecto y automáticamente, para grandes volúmenes de producción, con máquinas preformadoras cuyos ratios de trabajo son de miles de componentes/hora.

![](../img/348b594c.png#center)

En el montaje de prototipos o placas de muestra, bastarán unas pinzas y unos alicates para insertar los componentes en su posición correcta e ir cortando los terminales y doblando los extremos salientes con el fin de conseguir cierta sujeción mecánica que permita soldarlos manualmente sin que caigan de la placa al invertirla.

![](../img/722000e2.png#center)

Los componentes que tengan una gran disipación térmica necesitan ser montados algo elevados sobre la placa. Los demás pueden ser colocados en contacto con ella, doblando sus terminales en ángulo recto si son axiales o directamente si son radiales.

![](../img/c3819c11.png#center)

Para ajustar patitas de circuitos integrados DIL, con distancia entre filas de 7,62 mm y 15,24 mm, existen herramientas que consiguen el espaciado correcto entre ellas.

![](../img/b6c335b0.png#center)

Al insertar los componentes tendremos en cuenta las siguientes recomendaciones:

- Si el mecanizado de la placa se ha hecho bien no habrá ninguna dificultad en insertar los componentes con sus terminales preformados. Con un poco de práctica esto se hace muy rápido y con un poco más de práctica se aprende a darles una forma tal a los terminales que al dar la vuelta a la placa para soldar el componente no se salga de su sitio.
- Comenzar por los de menor altura, para que al soldar se puedan apoyar sobre el soporte mullido sin salirse. Primero las vías y los puentes, después resistencias, diodos, condensadores, etc.
- Permitir que se lean sus valores: códigos de marcado en las resistencias, polaridad y valor de los electrolíticos, denominación de semiconductores, etc.
- Los componentes del mismo tipo seguirán el mismo criterio de colocación, por ejemplo en las resistencias horizontales la banda de tolerancia siempre a la derecha o en la parte inferior si están en posición vertical.
- Respetar las polaridades de LEDs, electrolíticos, puentes rectificadores, etc.
- Colocar los circuitos integrados y los semiconductores en posición correcta teniendo en cuenta el pin número 1 o el chaflán o muesca que indica un determinado terminal.
- Prestar atención a la posición de conectores y regletas que llevan cables al exterior.
- Los componentes que van sobre zócalo no se montan hasta que el circuito esté totalmente acabado.
- En general, los componentes deben entrar a fondo hasta estar en contacto con la placa, pero hay excepciones: componentes que se calientan mucho (para facilitar su refrigeración se deja un espacio entre ellos y la placa), la mayoría de transistores, reguladores, puentes rectificadores, etc.

## Proceso de soldadura

El proceso de soldadura puede automatizarse, aunque en prototipos de laboratorio se suele hacer de forma manual.

Pretendemos lograr una buena conducción eléctrica del componente a la placa y una buena resistencia mecánica, para lo cual seguiremos los siguientes pasos:

![](../img/cbcd8de1.png#center)

1. Introducir la patita del componente en el orificio del pad y sujetarle evitando que pueda moverse durante el proceso.
2. La punta del soldador caliente debe hacer contacto con la patita del componente y con el pad de cobre de la placa.
3. Una vez estén suficientemente calientes ambos elementos, pin y pad, se aplica el estaño justo para que se forme una especie de cono o volcán en la zona de soldadura.
4. Se mantiene unos instantes la punta del soldador con el fin de que el estaño se distribuya uniformemente. Después retirar el soldador.
5. Mantener el componente inmóvil unos segundos hasta que se enfríe y solidifique el estaño. No se debe forzar el enfriamiento del estaño soplando porque se reduce la resistencia mecánica del conjunto.
6. Con la herramienta adecuada se corta el trozo de patita que sobresale de la soldadura.

La soldadura de estaño debe ser lo más perfecta posible, para ello observaremos lo siguiente:

- Las piezas a soldar deben estar totalmente limpias y, a ser posible, preestañadas. Si hay suciedad en la zona de soldadura puede interferir en la conductividad y en la resistencia mecánica de la misma, por lo que es necesario limpiar bien los restos de óxido, grasa, etc. de todos los elementos a soldar, incluida la punta del soldador.
- Una soldadura “fría” se produce cuando no se aplica suficiente calor. El estaño queda adherido de forma defectuosa con lo cual se desprenderá con facilidad y además no asegura una buena conducción eléctrica. Comprobar que el soldador ha adquirido la temperatura adecuada acercando el hilo de estaño a la punta: si se funde con facilidad, el soldador está dispuesto para su utilización.
- Si se aplica poco estaño puede parecer en principio que la soldadura es buena porque existe conducción eléctrica, pero tiene poca resistencia mecánica y acabará por desprenderse.
- Si se aplica estaño en exceso, dado que el espacio entre las pistas de cobre de un circuito impreso suele ser de unos pocos milímetros, se sobrepasará la zona de soldadura pudiendo llegar a unirse una pista con otra y provocar averías en el circuito.

![](../img/860e9e12.png#center)

- Es aconsejable disponer de una estación soldadora termorregulada. En su defecto, utilizaremos un equipo formado por un soldador tipo lápiz de punta fina de 25 ó 30W (12 ó 15W si se trata de componentes SMD) y un soporte provisto de esponja limpiadora.
- Es conveniente el uso de algún flux para facilitar el proceso de soldadura y, así mismo, limpiar a menudo la punta caliente del soldador frotándola suavemente con la esponja humedecida del soporte portasoldador.
- En los componentes con muchos terminales esperar a que se enfríe una soldadura antes de comenzar con la siguiente con el objeto de no acumular en él una temperatura excesiva.
- Al soldar los terminales de dispositivos activos (diodos, transistores, etc.) sujetarlos con unos alicates metálicos que hagan la función de radiador, para evitar que llegue un calor excesivo al cuerpo del componente.

![](../img/fefced6b.png#center)

- Una soldadura correcta debe tener forma de carpa de circo en cuya cúspide sobresalga (A) la patita del componente. Nunca debe dejarse una soldadura con forma abombada o esferoide (B), pues puede ser una soldadura falsa en la que no haya contacto eléctrico entre la pata y el estaño por quedar una película de resina que recubre y aísla eléctricamente ambos elementos. Este error se produce porque la patita no se ha calentado lo suficiente y la resina no se ha volatilizado, o porque se ha puesto demasiado estaño o un estaño de baja calidad.
- Filtrar el humo que se produce al fundirse el núcleo de resina que acompaña al hilo de estaño.

![](../img/9a3f5caf.png#center)