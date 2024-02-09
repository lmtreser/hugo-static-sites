---
title: "Introducción al Diseño Electrónico por Computadora"
date: 2024-02-09T10:49:31-03:00
draft: false
weight: 2
---

## Algunas definiciones

La automatización de los procesos industriales a lo largo de los años ha dado lugar a un avance espectacular de la industria. Todo ello ha sido posible gracias a una serie de factores entre los que cabe destacar las nuevas tecnologías, la generalización del uso de las computadoras y, sobre todo, el control y la regulación de sistemas.

La incorporación de las computadoras en la producción es, sin lugar a dudas, el elemento puente que ha permitido lograr la automatización integral de los procesos industriales. La aparición de los microprocesadores/microcontroladores ha facilitado el desarrollo de técnicas de control complejas, la robotización, la implementación de sistemas de gobierno y la planificación. Todos estos elementos llevan consigo la reducción de costos, el aumento de productividad y la mejora de calidad del producto.

La primera época de la automatización estuvo marcada por la aplicación de dispositivos capaces de controlar una secuencia de operaciones y el comienzo del estudio sobre la regulación automática. La segunda época, desde la década de los cuarenta hasta nuestros días, se ha caracterizado por la aparición de la microelectrónica y de las computadoras y, a su vez, por el gran avance de la teoría de control. También en esta época, la introducción de los robots industriales en la fabricación de series pequeñas y medianas ha incrementado sustancialmente la flexibilidad y autonomía de la producción. A finales de los 80, las tecnologías de integración RISC y CISC y las nuevas generaciones de microprocesadores ponen a disposición del fabricante de software máquinas sin limitaciones tecnológicas, capaces de desarrollar aplicaciones cada vez más complejas, de modo que los actuales PCs se solapan tanto en prestaciones como en precio con las workstations, término indisolublemente ligado cada vez que se habla de CAD/CAE/CAM.

Podemos definir el CAD o Diseño Asistido por Computadora como la técnica que, basándose en el uso de la computadora y con los programas adecuados, se encarga de facilitar el diseño de un producto. El CAD se utiliza en mecánica, arquitectura, química, cartografía y, en lo que a nosotros se refiere, en electricidad y electrónica.

Como consecuencia del progresivo aumento de prestaciones de las computadoras personales, así como de la reducción de su precio, los conjuntos de programas integrados o paquetes de CAD/CAM se han popularizado y su empleo proporciona una importante disminución del tiempo dedicado al desarrollo, del coste y, por tanto, un notable incremento de la competitividad. Poco a poco, la computadora se ha convertido en una herramienta imprescindible para cada una de las etapas del proceso productivo, convirtiéndose en una auténtica estación de trabajo.

Se introduce el concepto CAE (Ingeniería Asistida por Computadora) conformando el grupo de ayudas centradas en la simulación eléctrica y funcional de los circuitos y sistemas.

Surge así, para la automatización del diseño electrónico, el entorno EDA que abarca la técnica CAD/CAE/CAM: el CAD como el conjunto de herramientas informáticas destinadas a capturar el esquema electrónico del circuito y a diseñar la tarjeta de circuito impreso correspondiente que se desea construir; el CAE se reserva a las herramientas informáticas encargadas de comprobar el correcto funcionamiento del circuito cuyo esquema se ha obtenido con el CAD; finalmente, el CAM proporciona los recursos precisos para la construcción del circuito probado.

Es en este tipo de técnicas donde el entorno EDA ha puesto de relieve la importancia de automatizar informáticamente el proceso, desde el diseño hasta la fabricación, ofreciendo las siguientes ventajas:

- Seguridad de un correcto funcionamiento, ya que se ha simulado el prototipo sin necesidad de montarlo físicamente.
- Fácil integración, sin problemas adicionales, en una cadena de fabricación.
- Obtención de un producto más económico, de mejor calidad y en el menor tiempo posible.

Una de los mayores aportes del CAD/CAE/CAM es la compartición de recursos, librerías y desarrollos, por parte de varios usuarios que realizan diversas labores relacionadas con el proyecto.

![](../img/92c9345a.png#center)

## CAD electrónico

Las estaciones de diseño CAD necesitan una base de datos de la que extraer la información necesaria para las distintas fases del proceso. La forma de iniciarla es mediante la captura de esquemas en la que el diseñador dibuja los circuitos del proyecto, valiéndose de un editor gráfico que le permite posicionar componentes y figuras, trazar líneas y buses de interconexión, mover, copiar, borrar objetos, etc.

Para realizar la entrada del esquemático es necesario, además del editor gráfico, que el sistema lleve incorporada información de los componentes incluidos en el esquema. Es pues esencial disponer de una completa biblioteca de componentes electrónicos (analógicos, digitales, discretos, integrados, conectores, elementos complementarios, etc.) debidamente caracterizados, tanto desde el punto de vista geométrico como de comportamiento eléctrico, de forma que el usuario pueda invocarlos, posicionarlos y realizar conexiones entre ellos.

El editor gráfico permitirá la estructuración del proyecto de forma jerárquica, es decir, a base de bloques interconectados entre sí al nivel más alto de la jerarquía, correspondiendo al diseñador asignar a cada uno de los bloques su contenido, de forma que el sistema, cuando analiza ese esquema jerárquico, sabe encontrar el contenido de cada bloque.

Una vez dibujado el esquema eléctrico en la computadora, mediante el editor gráfico y las librerías de componentes, se realiza un proceso de compilación que establece la base de datos global, única para todas las tareas, de modo que las modificaciones introducidas en cualquier etapa del desarrollo se reflejen en ella inmediatamente, minimizando así la posibilidad de introducir errores por falta de actualización o por incorrecta transmisión de información de una etapa a otra. Esta compilación detecta, a su vez, los posibles errores de conexionado cometidos, con lo que el usuario tiene control sobre la calidad del producto desde las primeras etapas del proceso.

Como complemento al editor gráfico existe un editor de componentes destinado a la creación de nueva simbología, no incluida en las librerías originales del programa, o a la modificación de la ya existente.

Una etapa intermedia entre la captura de un esquema y su posterior simulación o diseño del circuito impreso, consiste en someterle a una serie de procesos que posibiliten la comunicación con otras herramientas informáticas.

Finaliza esta fase con la preparación de la PCB, posicionado de componentes, definición de zonas de relleno de cobre, trazado de pistas, verificación de las reglas del diseño y obtención de archivos para trazado y taladrado de la placa.

## CAE electrónico

El CAE se encarga de efectuar una completa simulación del circuito cuyo esquema se ha capturado en la fase anterior, tanto en condiciones nominales como en otras, incluidas las situaciones límite que, de ser realizadas sobre un prototipo real, podrían producir su destrucción. En la actualidad son comunes los paquetes integrados que incluyen simulación mixta dirigida a circuitos constituidos por componentes analógicos y digitales.

Se cuenta con librerías especiales que contienen los componentes modelizados matemáticamente para responder a su comportamiento físico.

Se puede someter al circuito a multitud de análisis: barrido DC, punto de trabajo, función de transferencia, sensibilidad, respuesta en frecuencia, ruido, transitorio, Fourier, paramétrico, de temperatura, estadísticos (Montecarlo y peor caso), etc.

Así, con frecuencia no será necesario montar físicamente el prototipo y, de hacerlo, se conseguirá que cumpla las especificaciones de funcionamiento en un corto intervalo de tiempo, logrando una puesta a punto rápida y definitiva.

También se pueden obtener copias duras de los gráficos y de las señales del circuito mediante impresoras a color y plotters, que documenten con todo detalle el proyecto.

## CAM electrónico

El CAM facilita la implementación física de los esquemas electrónicos diseñados y simulados en las fases previas de CAD/CAE. Está dirigido a dos áreas principales:

- Fabricación de ICs. Existen estaciones que ofrecen la información necesaria para la construcción de circuitos integrados a medida, los cuales contienen los esquemas electrónicos diseñados.

- Fabricación de circuitos impresos. Se importan los archivos Gerber y se preparan los datos de producción para prototipos, calculando los canales de aislamiento en caso de usar máquinas CNC para taladrado y fresado de la PCB, cuyos parámetros de herramientas y funciones de control habrá que conocer para un correcto manejo.

Los buenos sistemas CAM disponen de salidas directas a fotoplotter, máquinas de inserción automática de componentes, taladradoras con control numérico, etc. Finalmente, hay estaciones de trabajo que transfieren automáticamente datos sobre el diseño físico al sistema de prueba de tarjetas acabadas, mejorando la productividad y la fiabilidad, y proporcionando un producto final listo para fabricación de series.

## Detalle del proceso para obtención del prototipo

Las herramientas de las que se vale el diseñador, tanto en el diseño a nivel de placa de circuito impreso como a nivel de circuito integrado, constituyen el Software de Diseño Electrónico.

Una vez hechos los cálculos precisos para iniciar el proyecto de acuerdo con las especificaciones dadas, procederemos a la captura de dicho diseño en la computadora, para posteriormente utilizarlo en la simulación, fabricación y documentación. Es por tanto necesario disponer de:

- *Un editor gráfico para la captura esquemática.* Este programa utiliza símbolos de componentes y otros elementos auxiliares para representar circuitos.

- *Una base de datos jerarquizada.* Aunque forma parte del editor de gráficos, por su importancia, se puede tratar aparte. En ella están los elementos a emplear y debe ser única.

- *El netlist.* Programa destinado a generar la lista de conexionado entre los elementos de un diseño. Puede efectuarse manualmente mediante un editor de texto o, como es habitual, a partir del esquema. Se utiliza como entrada de datos para el simulador y para la PCB.

- *Simuladores.* Programas que permiten determinar el comportamiento de un diseño antes de su realización física, mediante simulaciones, análisis y ensayos.

- *Programas para el diseño lógico programable.* Destinados a obtener los ficheros con la información lógica a implementar en un dispositivo programable, en el formato adecuado, para su posterior grabación.

- *Un editor gráfico para el trazado del circuito impreso.* Este programa utiliza el netlist adecuado, que incluirá la información de los encapsulados, para realizar el emplazamiento y conexionado de los componentes.

- *Fabricación CNC.* Programas de control numérico para el microfresado y taladrado automático de la placa virgen.

![](../img/f8119736.png#center)