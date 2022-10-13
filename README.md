# Profesional-de-CSS-Grid-Layout
 Layout para maquetar sitios web complejos sin complicaciones. Analiza tus diseños, divide tu aplicación en cuadrículas y conviértelas en estilos CSS. Integra CSS Grid con Flexbox y el modelo de caja para alinear tus elementos exactamente donde deben estar. Descifra todos los misterios de CSS Grid Layout para convertirte en frontend developer profesional.

1991 Tim Berners-Lee sus hojas de estilo
1993 Viola intenta 
1994 Mosaic
Hakon CHSS
1994 CSS
Bert Bos 1995 WWW1996 w3c
- ie3
- netscape
- opera
Ethan Diseño Responsivo
pre prefijos
atomic dising diseño de componentes
frameworks facilitan la elaboración de componentes
performance peso
accesibilidad todos pueden acceder
CSS Grid diseño basado en cuadriculas
Rachel Andrew CSS3 Grid layout
Jen Simmons CSS3 Grid layout
2017 se unen todos los navegadores
CSS es un sistema de diseño
Técnicas de alineamiento antiguas
- Margin: 
    top
    right
    bottom 
    left
    margin top rights bottom left

- Line height
    text-align
    vertical-align
    line-height
- Tabel cell
    display
    text-align
    vertical-align
block-start se refiere al top
block-end se refiere al bottom
inline-start se refiere al left
inline-end se refiere al ringth

Propiedades físicas
MARGIN: margin-top | Margin-left | Margin-right | Margin-bottom

PADDING: padding-top | paddding-left | padding-right | padding-bottom

BORDER (-size-style-color): border-top | border-left | border-right | border-bottom

POSITIONS top | left | right | bottom.

Propiedades Lógicas
MARGIN: Margin-block-start | Margin-inline-start | Margin-inline-end | Margin-block-end

PADDING padding-block-start | paddding-inline-start | padding-inline-end | padding-block-end

BORDER(-size-style-color): border-block-start | border-inline-start | border-inline-end | border-block-end.

POSITIONS: inset-block-start | inset-inline-start | inset-inline-end | inset-block-end

TOP = Block-Start
RIGHT = Inline-End
BOTTOM = Block-End
LEFT = Inline-Start

Las propiedades que tenemos que tener en cuenta para el alineamiento son estas 3:

Display: Flex
Justify-content: Es para los elementos en su alineación horizontal
align-items: Es para alinear los elementos de forma vertical.

CSS Grid se puede utilizar para lograr muchos diseños diferentes. También se destaca por permitir dividir una página en áreas o regiones principales, por definir la relación en términos de tamaño, posición y capas entre partes de un control construido a partir de primitivas HTML.

<h4>Apuntes</h4>
Grid nos permite crear rejillas que tenga filas y columnas

En este momento se tiene una mayor complejidad en el diseño web

Siempre se tendrá un Contenedor (padre)

Los items (elementos hijos) serán los que estarán dentro de este contenedor
Los hijos también pueden ser padres
Todos los padres tienen que tener:
display: grid;

Display: Mostrar y presentar

Outer: Grid se comporta como bloque por fuera pero no por dentro

Los elemenos **inline **no se les puede poner width ni height ni margin-top o bottom, el tamaño del contenedor será determinado por el tamaño del contenido

Los elementos inline-block, tienen muchas similitudes con los elementos inline, hacen todo lo que los **inline **hacen, sin embargo a estos se les puede poner width, height y margin vertical, lo que quiere decir que es lo mejor de ambos mundos.

Los elementos block, siempre van a iniciar en una linea nueva,y tomaran todo el ancho de su contenedor, no podemos posicionar otros elementos de html al lado de un elemento block, a estos elementos **block **se les puede poner width, height, y margin vertical.

Block-level Elements
A block-level element always starts on a new line.
A block-level element always takes up the full width available (stretches out to the left and right as far as it can).
A block level element has a top and a bottom margin, whereas an inline element does not.

Inline Elements
An inline element does not start on a new line.
An inline element only takes up as much width as necessary.
This is a <span> element inside a paragraph.

Alineamiento ⇒ en donde quiero que estén los elementos de mi grid
Podemos alinear todos los contenedores a una dirección
Tenemos dos Grupos para ordenar por parte del contenedor
    Items
        justify-items
        align-items
        place-items
    Content
        justify-content
        align-content
        place-content
Propiedades en común:
    Justify ⇒ Alineación por dentro de la grid
        Inline axis (row axis)
        De izquierda a derecha
        start
        end
    Align ⇒ Alinear la Grid en su contenedor
        block axis (column axis)
        De arriba hacia abajo
        start
        end
Content
    Cuando el contenedor del grid es más grande que la grid, podemos alinear la utilizando las propiedades justify-content y align-content

items
    justify-items y align-items nos permiten alinear los elementos que están dentro de la grid.
<h4>Ideas/conceptos claves</h4>
    Track ⇒ Union de dos o más celdas dentro de una grid    

<h4>Apuntes</h4>
    No todas las grillas tendrán items exactamente contados
        No contaras con filas y columnas exactas por que los datos pueden ser dinámicos
    Para ello está la grid implícita
        Te crea filas o columnas si las necesitas con anchos sin tamaño
    Para que se valla ordenando según lleguen nuevos elementos se debe usar esta propiedad
        Don especificaremos el tamaño donde agregarlo

/* Agrega automaticamente columnas */
grid-auto-flow: column;

/* Agrega automaticamente filas */
grid-auto-flow: row;

/* Define el tamaño a las columnas que se agreguen automaticamente */
grid-auto-columns: 100px;

/* Define el tamaño a las filas que se agreguen automaticamente */
grid-auto-rows: 100px;

La función CSS repeat() representa un fragmento repetido de la lista de la pista, permitiendo un gran número de columnas o renglones que exhiben un patrón recurrente para ser escrito de una forma más compacta.
|
En función Css minmax() el min representa el tamaño mínimo que va a tener cada uno de los elementos de la grid y el max nos indica el valor máximo de los elementos de la grid. Esto nos sirve para que el contenido se vea bien en determinados tamaños.
|
Con la función de auto-fit() ADAPTA las columnas DISPONIBLES ACTUALMENTE en el espacio expandiéndolas para que ocupen cualquier espacio disponible. El navegador hace eso después de LLENAR ese espacio adicional con columnas adicionales (como con el autocompletar) y luego colapsar las vacías.
|
Con la función de auto-fill() LLENA la fila con tantas columnas como pueda caber. Por lo tanto, crea columnas implícitas cada vez que cabe una nueva columna, porque está tratando de LLENAR la fila con tantas columnas como sea posible. Las columnas recién agregadas pueden estar vacías, pero seguirán ocupando un espacio designado en la fila.
/************ Estas funciones con perfectas para el responsive design.*********/
|
La función fit-content() organiza un contenido en especifico el cual lo reserva y el resto seria auto.