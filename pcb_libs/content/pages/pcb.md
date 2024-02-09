---
title: "Placas de Circuito Impreso (PCB)"
date: 2024-02-09T10:49:33-03:00
draft: false
weight: 4
---

## Introducción

Sabemos que una placa de circuito impreso o PCB es un soporte físico para componentes electrónicos que permite, además, su interconexión eléctrica. Dicho soporte está realizado a partir de una plancha de material aislante que lleva adherida, en una o en sus dos caras, una fina película de cobre.

Podemos así clasificar las PCB atendiendo a distintos criterios:

- El sustrato o material: baquelita, fibra de vidrio, teflón, etc.
- El número de caras: de simple o doble cara, aunque también las hay multicapa o flexibles.

![](../img/ea9fb22b.png#center)

Las PCB más comunes tienen 1,6 mm de espesor y una fina película de cobre de 35 micras. En cualquier caso, nuestro objetivo será realizar el diseño de las pistas ayudados por un editor. Obtendremos el resultado en dos formatos diferentes según sea el método de fabricación que vayamos a emplear:

- Los fotolitos en papel vegetal o transparencias, si elegimos el método químico sobre placas fotosensibilizadas.
- Los archivos Gerber, en caso de disponer de una máquina microfresadora CNC sobre placas vírgenes.

En ambos casos supondremos que la fabricación del circuito impreso corre de nuestra cuenta, así como las fases posteriores de ensamblaje de componentes y soldadura manual. Esto implica que es conveniente trabajar con encapsulados cuyos pads sean ligeramente mayores que los de las librerías originales, pensados para fabricación automatizada con equipos profesionales. Por otra parte, estableceremos parámetros “generosos” de anchura de pistas y separaciones entre ellas.

Llamaremos cara de componentes (top) aquélla donde van situados la mayoría de ellos, normalmente los de inserción y algunos de montaje superficial, y cara de soldadura (bottom) a la opuesta exterior. Quede claro que en caso de tarjetas con muchos componentes, habrá pistas y componentes en las dos caras.

![](../img/407c71e6.png#center)

En la figura se detalla el sistema para realizar la conexión eléctrica entre pistas de capas opuestas mediante las llamadas vías. Éstas son colocadas automáticamente durante el proceso de autoruteado.

![](../img/78e1286.png#center)

## Unidades de medida

Hay que tener cierta atención a la hora de trabajar con los software de diseño ya que por defecto, generalmente las unidades de medida están definidas en pulgadas (Sistema Anglosajón) y no en milímetros (Sistema Internacional).  Por ejemplo es muy común ver el mil como unidad. El mil es una unidad de longitud igual a 1⁄1000 de una pulgada (una milésima de pulgada).

```
1 pulgada   2,54 centímetros
1 mil       0,0254 milímetros
```

## Identificación y correspondencia de pines

Sucede a menudo que es incorrecta la identificación original de terminales de algún componente discreto, es decir, que los números de los pines del mismo en el esquema no coinciden con los nombres de los pads en el layout. Este conflicto, que no sucede con los circuitos integrados, debemos solucionarlo en el esquemático.

![](../img/42d25621.png#center)

Es recomendable comprobar la correcta asignación y nombrado de pines de los componentes discretos. Por tanto, sugerimos que al crear o al modificar cualquier componente, por ejemplo, llamaremos:

- P a los terminales positivos y N a los negativos de condensadores electrolíticos, buzzers, pilas, etc.
- A al ánodo y K al cátodo de todo tipo de diodos.
- E, B y C para los transistores bipolares.
- A1, A2 y G para los TRIACs, etc.
- En los componentes sin polaridad también deberá haber correspondencia exacta entre los números de los pines, sobre todo si tienen más de dos.

## Taladros de fijación

Una operación de mecanizado usual en las tarjetas consiste en situar, normalmente en la periferia, unos taladros de unos 3 mm de diámetro destinados a colocar los separadores de fijación de la misma. El número de ellos lo define el usuario y dependerá del tamaño y la forma de la tarjeta.

![](../img/99117987.png#center)

## Definir valores globales de espaciado

![](../img/610e4d20.png#center)

## Preparar la placa para el posicionado

Esta operación es crítica porque de ella dependerá que se realice un buen acabado en el posterior trazado de pistas (pocas vías y pistas cortas) y una distribución uniforme y racional de componentes, con previsión de futuro que facilite el acceso a los puntos de prueba en posibles reparaciones e inspecciones. Esto se puede traducir en los siguientes criterios funcionales:

- Facilitar las conexiones a regletas y bases conectoras situándolas próximas al borde de la PCB.
- Permitir con facilidad la realización de ajustes en trimmers y demás componentes variables.
- Aislar convenientemente los componentes emisores de radiaciones electromagnéticas.
- Alejar los componentes de potencia de aquellos que son más sensibles al calor.
- Separar las zonas de alta tensión respecto al resto.
- Respetar la separación mínima entre componentes.
- Dejar espacio apropiado para los tornillos de fijación de la placa y de componentes grandes.
- Prever el espacio necesario para los radiadores de los componentes de potencia.
- Alinear los componentes paralelos a los ejes X e Y.
- Agrupar los componentes en función del tipo: analógicos, digitales, etc.
- Orientar de una determinada forma los componentes polarizados, por ejemplo el cátodo de los diodos, la tolerancia de las resistencias y el positivo de los electrolíticos, mirando hacia la derecha en montaje axial y abajo en montaje radial.
- Montar los componentes del mismo tipo a ser posible en el mismo sentido.
- En ningún caso se introducirá en un taladro de pad más de un terminal de componente.
- No dejar componentes aislados del resto, evitando también aglomeraciones.
- Cuidar que se pueda leer correctamente el valor, nomenclatura y el código de marcado de cada componente.
- Utilizar una rejilla uniforme en milésimas de pulgada.
- Cuidar la presentación y el aspecto final de la tarjeta.

## Crear zonas de relleno de cobre (blindaje y escudos EMI)

Hay tres tipos de obstáculos que se disponen en layout cuando se trabaja con cobre:

- Copper pour. Es un relleno de cobre que obedece a las reglas de aislamiento asignadas a pistas, las cuales pueden pasar a través de él. Puede utilizarse para la supresión de ruidos, como pantalla o para aislar señales.

- Copper area. Es una zona o área de cobre en la que no pueden trazarse pistas y que no respeta las normas de aislamiento. Permite crear formas de nodos personalizados, suprimir ruidos, evitar el calentamiento de componentes o actuar como barrera de trazado.

- Anti-copper. Son zonas sin cobre dentro de rellenos de cobre. Los rellenos y áreas de Cu pueden ser sólidos o enrejillados.

![](../img/e6b7146e.png#center)

## Tipos de vías

Sabemos que las vías son taladros metalizados cuya misión es unir pistas situadas en distintas capas. Se emplean en las tarjetas de dos o más caras y nunca deben ser utilizadas para la inserción de los terminales de componentes. En las PCB multicapa las vías tienen una importancia fundamental porque realizan todas las interconexiones.

Dependiendo de la complejidad del diseño, estas tarjetas incorporan los siguientes tipos de vías:

- Vía pasante (Through-hole via). Conecta las dos capas externas entre sí y, a veces, con algunas internas.
- Vía enterrada (Buried via). Conecta capas internas.
- Vía ciega (Blind via). Conecta una capa externa –top o bottom– con alguna(s) interna(s).
- Microvía (Micro via). Es un caso particular de vía ciega con dimensiones reducidas. Se caracteriza por no realizarse de forma mecánica, sino mediante tecnología láser. Puede llegar a conectar varias capas y facilita altísimos niveles de integración.

![](../img/29068d18.png#center)

## Nodos térmicos

Los nodos térmicos (Thermal reliefs) se emplean en las PCB multicapa para establecer el contacto entre las conexiones de positivo y negativo de cualquier capa con los planos de alimentación y masa respectivamente. También se emplean en las zonas de relleno de cobre. Son pads especiales que, al tener forma anular con discontinuidades, evitan la dispersión sobre una zona amplia de cobre y facilitan la transmisión del calor durante la soldadura.

![](../img/e777ec4e.png#center)

## Capas

Las capas pueden ser de los siguientes tipos:

- Apta para el trazado (Routing Layer).
- No usada (Unused Routing).
- De taladros (Drill Layer).
- Plano (Plane Layer).
- De documentación (Documentation).
- De puentes (Jumper Layer).

*Las capas para el trazado de pistas* pueden hacerse invisibles separadamente y tener distintos colores identificativos.

*Los planos de alimentación y masa* pueden ser conectados a cualquier conexión o terminal de componentes.

*Las capas de serigrafía* nos facilitarán el marcado del contorno de los componentes y su referencia, así como texto libre sobre la placa.

*Las capas de ensamblaje* proporcionan detalles válidos para la fabricación, como dimensiones globales, cotas de posición, marcas fiduciales, etc.

*Las capas de taladrado* contienen una codificación de la posición y diámetro de todos los taladros a realizar sobre la tarjeta.

*Las capas de máscara de soldadura* se presentan en negativo, es decir, vemos los pads que definen, precisamente, las zonas donde no se aplicará el barniz de la máscara usada para soldar por ola.

*Las capas de pasta de soldadura*, también en negativo, son aptas para componentes SMD.

## Cálculo de ancho de pistas

La determinación de la anchura de pistas de la PCB se facilita si admitimos que:

- Para corrientes menores de 300 mA dependerá del procedimiento de fabricación: en el caso de la química el ancho mínimo será de 0,5 mm y para microfresado de 0,3 mm.

- Para corrientes mayores de 300 mA y considerando una tarjeta con espesor de cobre de 35 micras, calculamos el ancho de cada pista mediante el gráfico de la figura, donde también se tiene cuenta el incremento de temperatura previsible en la placa. Como norma práctica digamos que basta con 0,5 mm de ancho por cada Ampere.

![](../img/c394aad.png#center)

## Postprocesos

Antes de dar por terminado el diseño de la PCB, debemos crear los archivos, informes y documentos de salida, en el formato adecuado a las máquinas y técnicas de fabricación que se usarán. Las tareas disponibles de postprocesado son las siguientes:

- Renombrar los componentes sobre la placa en la dirección que se desee y después reanotar estos cambios al esquema para mantener la coherencia del diseño.
- Documentar las dimensiones de la placa.
- Obtener la vista preliminar de las capas para comprobar los resultados y a continuación imprimir los fotolitos.
- Crear los archivos Gerber de las caras y taladros.
- Generación de informes.