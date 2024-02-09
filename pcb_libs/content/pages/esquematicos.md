---
title: "Circuitos Esquemáticos"
date: 2024-02-09T10:49:32-03:00
draft: false
weight: 3
---

## Introducción
Cuando se acomete un proyecto, en función del tamaño de los planos a dibujar o de la estructura y complejidad del mismo, podemos definir tres tipos de diseños: simple, plano y jerárquico.

*Diseño simple.* Consta de una sola página de esquema o lámina, donde se dibujará el circuito, eligiendo el tamaño de lámina normalizado más adecuado (A÷E según la norma americana ANSI ó A4÷A0 según la europea DIN) o bien estableciendo uno personalizado.

![](../img/15af23ba.png#center)

*Diseño plano.* Consta de varias páginas de esquema contenidas en una única carpeta, con conexión horizontal, todas con el mismo nivel de importancia y relacionadas entre sí a través de unos conectores especiales llamados de fuera de página. Se aconseja usar esta estructura para diseños con 10 páginas como máximo.

![](../img/b5531402.png#center)

*Diseño jerárquico.* Consta de varias páginas de esquema, con distinto nivel de importancia según una conexión vertical. La página principal o raíz, cuyo icono se identifica con una barra (/), contiene en su interior otra u otras páginas representadas mediante los llamados bloques jerárquicos, los cuales, a su vez, pueden alojar nuevas páginas, conformando una estructura de árbol. Tiene la ventaja de dar una visión modular, tipo diagrama en bloques, que facilita mucho el trabajo.

![](../img/9cb8aa65.png#center)

Las jerarquías pueden ser SIMPLES o COMPLEJAS, siendo su diferencia el que estas últimas contienen varios bloques jerárquicos que corresponden a una misma página de esquema, de modo que la circuitería repetida sólo hay que dibujarla una vez, mientras que en una jerarquía simple una misma página de esquema no se utiliza varias veces.

- Diseño jerárquico simple: el esquema raíz (o padre) tiene varios bloques jerárquicos (o hijos) todos diferentes. A su vez, cada hijo puede tener otros hijos, que serán los nietos del padre y así sucesivamente, conformando una estructura de árbol genealógico.

- Diseño jerárquico complejo: El esquema padre también tiene varios hijos, con la particularidad de que al menos dos de ellos tienen que ser iguales, es decir, gemelos. En el ejemplo, ambas jerarquías tienen en realidad el mismo número de planos (tres), pero en la compleja de la derecha, solo hay que dibujar dos.

![](../img/613d9dd6.png#center)

## Cajetines (Title Block)

Todo plano lleva en su borde inferior derecho un cajetín, casillero o rótulo destinado a incluir información relacionada con lo dibujado, como por ejemplo:

- Título del esquema
- Localización
- Escala
- Características de materiales, componentes, normas, etc.
- Empresa, escuela o laboratorio
- Departamento, grupo, etc.
- Autor(es), fecha y revisión
- Número total de planos

Según la norma UNE 1026, el cajetín se colocará a una distancia de 5 mm de los bordes de la hoja de papel, la cual dispondrá además de un margen izquierdo de 20 mm para el cosido y archivado del plano.

![](../img/2ac71127.png#center)

## Plegado de planos

En la figura vemos cómo deben doblarse los distintos formatos de planos, hasta quedar todos reducidos al tamaño A4, y así poder archivarlos junto con el resto de la documentación del proyecto.

![](../img/929a43ab.png#center)

## Elementos de un esquemático

![](../img/a861c43.png#center)

## Etiquetas (label)

Las etiquetas permiten conectar eléctricamente distintos puntos de la página del esquema sin necesidad de trazar los hilos, sin más que asignarles el mismo nombre o Alias. Es decir, se da un nombre a la conexión (net) y todos los hilos que compartan esa misma etiqueta, automáticamente, quedan incluidos en ella.

![](../img/148f7cad.png#center)

Dada la gran complejidad de algunos diseños electrónicos, este recurso posibilita el no tener que dibujar todos los cables entre componentes, evitando así aglomeraciones o esquemas con aspecto de tela de araña que resultan ilegibles. Este sistema es especialmente apropiado cuando las partes a unir estén muy alejadas entre sí. Por ejemplo, se ha empleado en la siguiente figura, donde los dos puntos marcados con el alias IN estarán eléctricamente unidos.

## Uniones

Se deberá colocar puntos de unión en las intersecciones de los hilos donde deba existir contacto eléctrico.

![](../img/fdfff71f.png#center)

## Capacitores de bypass en circuitos digitales

Al trabajar en conmutación los circuitos digitales no tienen un consumo constante de corriente de la fuente de alimentación, lo que puede provocar caídas de tensión perjudiciales para su correcto funcionamiento. Es necesario, por tanto, desacoplar la fuente de alimentación colocando un capacitor llamado de “bypass” en las proximidades de cada circuito integrado.

Al capturar un esquema con este tipo de circuito integrado, los condensadores de bypass o desacoplo se suelen dibujar aparte para no complicarlo en exceso, todos en paralelo entre el positivo y masa de la alimentación. En la figura observamos que también hemos colocado texto indicando el chip y los pines asociados a cada capacitor.

![](../img/623b075e.png#center)

En el diseño de la PCB, posicionemos los componentes en la placa y colocaremos los condensadores citados cerca de cada integrado. Luego trazaremos las pistas de conexión con los pads de alimentación, tal y como se ve en la figura.

![](../img/22a06d1c.png#center)

Después del trazado final de pistas veremos si es necesario modificar la posición o el cableado de alguno de ellos, para el caso de suponer un obstáculo insalvable en el trazado de otras conexiones. Cuando el montaje lo permita, se puede colocar un condensador SMD de bypass debajo del circuito integrado, o bien, adquirir un zócalo que lo lleve incorporado, lo cual simplifica el trazado.

![](../img/b230ec6c.png#center)

En otras ocasiones, en particular cuando predominan en la placa circuitos integrados digitales dispuestos matricialmente, tal es el caso de los bancos de memoria, es interesante la disposición de pistas de alimentación mostrada en la figura.

![](../img/82b9db0e.png#center)

## Pines de los componentes

Los pines de los circuitos integrados digitales generalmente se representan en el editor, según sean activos por flanco o por nivel, de la siguiente manera:

- Clock. Activo al flanco de subida.
- Dot. Activo a nivel bajo.
- Dot-clock. Activo al flanco de bajada.
- Zero length. Con cero unidades de rejilla.
- Line. Activo a nivel alto. Con una longitud de tres unidades de rejilla.
- Short. Activo a nivel alto. Con una longitud de una unidad de rejilla

![](../img/3d45e8d5.png#center)

Símbolos IEEE:

![](../img/e14659e3.png#center)

Respecto al tipo o carácter eléctrico, los pines pueden ser:

- 3-State. El triestado posee tres estados lógicos posibles: bajo (cero lógico), alto (uno lógico) y alta impedancia (circuito abierto).
- Bidirectional. Actúa como entrada y como salida.
- Input. Entrada o receptor de señal.
- Open collector. Colector abierto, que omite el pull-up del colector.
- Open emitter. Emisor abierto, que omite el pull-down del emisor.
- Output. Salida o emisor de señal.
- Passive. Pasivo, no tiene fuente de energía.
- Power. De alimentación, que recibirá el positivo o masa.

Los pines de alimentación no visibles se conectan por medio de etiquetas (alias) que llevan su nombre.

## Ejemplo de circuito esquemático terminado

![](../img/ba59638b.png#center)