<html>
      <head>
        <!-- Required meta tags -->
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    
        <!-- Bootstrap CSS -->
        <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.3.1/dist/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    
        <title>Practica #3 Lab. Programacion Web</title>
      </head>
      <body>
        <nav class="navbar-expand-lg bg-light">
            <div class="container-fluid">
                <center> <b><h1>Laboratorio de Programacion Web</h1></b></center>
              </div>
            <div class="right">
              <div align="right">
                <a href="https://alejandrohg90210.github.io/index.github.io/">
                <input type="button" value="Click INDEX"/>
              </a>
            <h2><p align=left>Practica #3</p></h2> 
              </div>
     </div>
        </nav>
     <H3>ACTIVIDAD 3: LECCION 3  Introducción a la presentación en pantalla con CSS </H3>
     <b><p>Objetivos</p></b>
     <p>En esta siguiente lección aprenderemos los conceptos fundamentales de diseño Web basados en CSS y la preparación de una estructura visual de página web con dos columnas y anchura fija. Además, también veremos el empleo de un archivo de “reset” de CSS y cómo se añade a las páginas. Se aborda también el uso del elemento &lt;div&gt; y las propiedades “float” y “clear” para crear columnas en la página.</p>
     <b> <p>El papel del archivo de reset CSS:</p></b>
     <p>Antes de empezar a crear un diseño visual de página Web vamos a ver cómo se utiliza un archivo de reset de CSS. Todos los elementos HTML se muestran en pantalla utilizando los estilos por defecto que aplica cada navegador. Ya hemos visto en el capítulo precedente cómo CSS nos permite definir estilos para tipos de letra, modificando el tamaño y la fuente, pero hay otros estilos no tan obvios. Por ejemplo: el estilo por defecto para un elemento heading 1 (&lt;h1&gt;) incluye unos márgenes de 10 pixeles por encima y por debajo del texto. Si queremos modificar el estilo de h1 para que no lleve márgenes, tendremos que indicar de manera explícita unas reglas que conviertan dichos valores a cero.
      Una regla CSS para anular los márgenes superior e inferior de los elementos heading 1 es así: </p>
    <p>h1{
         margin-top:0px;
         margin-bottom:0px;
      }</p>
      <p> Los elementos HTML incluyen márgenes por defecto. Aunque los navegadores web actuales tienen una calidad muy superior a los antiguos, conviene saber que cada motor de restitución empleado por los navegadores aplica sus propias reglas para mostrar los elementos en pantalla. En teoría esto quiere decir que el margen por defecto de 10 pixeles en un navegador X puede transformarse en 15 pixeles en el navegador y estas diferencias generan resultados no homogéneos a la hora de ver las páginas en distintos sistemas 
      Una técnica para homogeneizar las presentaciones en pantalla consiste en utilizar un archivo CSS de reset que elimine los estilos por defecto aplicados a los elementos HTML utilizados con más frecuencia. Con este reinicio de valores podemos conseguir una base fiable y coherente sobre la cual construir nuestros nuevos estilos. Para hacernos idea de cómo funcionan los estilos, vamos a abrir una página que ya tiene varios estilos y le asociaremos una hoja de estilos CSS de reset.
      </p>
      <ol>
        <li> En el editor de textos, en Archivo selecciona Abrir. Abre en la carpeta HTML5_03lessons el archivo 03_reset.html.
        Este archivo contiene una serie de elementos HTML genéricos, como títulos, párrafos, listas y formularios. No incluye estilos CSS.</li>
      <li>Muestra en el navegador la página y mira el  espacio de separación que hay entre los títulos, y fíjate también en el aspecto de las listas de datos y el formulario. Lo que haremos ahora es asociar una hoja de estilo CSS de reset para ver cómo afecta a la presentación en pantalla de estos elementos. Cierra el navegador y vuelve al editor.</ol>
      <li>Añade la siguiente línea de código (destacada en color rojo) debajo de la etiqueta de título para asociar la hoja de estilos reset.css que se encuentra también en la carpeta HTML5_03lessons:
        <p>&lt;head&gt;
           &lt;meta charset="utf-8" /&gt;
           &lt;title&gt; CSS Reset&lt;/title&gt;
           &lt;link href="reset.css" rel="stylesheet" type="text/css"&gt;
        &lt;/head&gt;</p>
        Guarda el archivo y visualízalo en el navegador
        Una página con elementos HTML habituales con reset de estilos CSS.
        Muchos de los elementos en esta página tenían los márgenes y distancias al borde prefijadas a cero. En consecuencia, el espacio entre ellos se ha eliminado. Se han reseteado también otros muchos estilos, como por ejemplo las listas de datos, que se han dejado en valor “none”, lo que elimina los puntos de las líneas en las listas no ordenadas, así como los números de orden en las listas ordenadas. Cierra el navegador y vuelve al editor de textos.
        </li>
      <li>Selecciona Archivo-Abrir. En la ventana, selecciona el archivo reset.css y pulsa Abrir. Revisa un momento el contenido.
        Esta serie de reglas elimina los valores por defecto de márgenes, márgenes interiores (“padding”), y los bordes de casi todos los elementos HTML.
      </li>
      <li>Ahora vamos a modificar la hoja de estilos, pero tenemos que asociarla a las páginas web. Recuerda que las hojas de estilos de reset son opcionales. Nos ayudan a normalizar la presentación en los distintos navegadores, y algunos diseñadores también incluyen en ellas sus propios estilos de uso frecuente para reiniciar los valores iniciales de los elementos.</li>
      </ol>
     <p><b>Breve historia de las técnicas de presentación en pantalla para la Web </b></p>
     <p>Cuando se empezó con el diseño web a mediados de los 90, el único método que se podía emplear para crear estructuras visuales complejas, como por ejemplo la presentación en varias columnas, consistía en emplear el elemento tabla (<table>). La tabla HTML estaba pensada inicialmente para mostrar datos de manera estructurada, en filas, columnas y celdas. Sin embargo los diseñadores empezaron a utilizar este elemento como base para las estructuras visuales de las páginas. En aquel momento esa técnica estaba plenamente justificada: las tablas era lo único que tenían para generar el tipo de diseños que se necesitaban y, además, eran un recurso extremadamente flexible.
      Empezaron a utilizarse técnicas como el anidamiento de tablas, es decir, crear tablas dentro de celdas de otras tablas de mayor tamaño. Por ejemplo, el código para una página normal de dos columnas podía empezar creando una tabla de tres filas y dos columnas:
      Puesto que la primera fila se iba a convertir en la sección de cabedera, no interesaría que quedase dividida en dos columnas. La etiqueta HTML &lt;colspan&gt; permite fusionar las dos celdas:
      En esta primera fila el diseñador, por ejemplo, podía intentar insertar una sección independiente de tres columnas, para mostrar un logo y otros elementos, como una barra de navegación o un campo para pedir credenciales de usuario. Para añadir esta sección, el diseñador tenía que crear una nueva tabla (esta vez con una fila de tres columnas) dentro de la primera fila de la tabla inicial:
      Para generar esta estructura de tabla, el diseñador tenía que configurar la tabla inicial con una anchura y altura fijas. Supongamos que el diseñador también quisiera un borde negro fino para todos los elementos. La propiedad “border” de las tablas HTML es muy básica no nos permite añadir colores. Una solución frecuente consistía en insertar la tabla actual dentro de otra, que consistía simplemente en una única celda con el fondo en color negro. Al modificar el margen interior y el color de fondo, y fusionar otras celdas más, el diseñador podía así crear una estructura visual basada en tablas con un cierto estilo.
      CSS ha sustituido ya el empleo de tablas para organizar las páginas, por lo que los elementos de tabla de HTML van regresando, poco a poco, a su función original, que es la de mostrar datos estructurados, y abandonan su papel como armazón visual de las páginas. 
      </p>
     <p><b>Introducción a las distintas opciones de presentación de páginas </b></p>
     <p></p>
     <p><b>El elemento &lt;div&gt;: creación de una estructura CSS de dos columnas con anchura fija </b></p>
     <p>Podemos considerar al elemento &lt;div&gt; como un contenedor genérico en el que podemos poner elementos relacionados entre sí de forma lógica. La apertura y cierre de etiquetas &lt;div&gt; suele hacerse rodeando a otros elementos de la página, de forma que dichos elementos quedan anidados dentro del contenedor. Puedes tener en la misma página todos los elementos &lt;div&gt; que consideres necesarios y con frecuencia se utilizan para crear el armazón visual. Un elemento &lt;div&gt; suele llevar un atributo ID (con lo que adquiere un “nombre” explícito dentro de la página) o bien pertenecer a una clase CSS, utilizándose ambos como medio para aplicar al contenedor uno o más estilos CSS. El empleo de elementos &lt;div&gt; facilita a otras personas la identificación de las diversas secciones en que se subdivide la página y también nos ayuda a controlar y aplicar estilos en cada una de ellas.</p>
     <p><b>La propiedad float CSS </b></p>
     <p>La propiedad float en CSS hace posible que un texto pueda escribirse alrededor de una imagen. Este estilo ha sido tomado del diseño de imprenta, donde a este efecto se le llama “justificación” del texto. CSS consigue el mismo efecto haciendo que los elementos que siguen a un elemento “flotante” puedan rodearlo, cambiando su posición relativa con respecto a él. Este comportamiento también nos sirve para crear columnas en una página.
      El valor float se puede también declarar como “left”.
      Los únicos valores posibles para float son “left”, “right” y “none”. No se puede centrar un objeto utilizando esta propiedad.
      Si queremos tener múltiples elementos flotantes dentro del mismo contenedor, el resultado es que se alinean entre sí. Este comportamiento se suele utilizar en ciertas funciones habituales de las páginas web, como por ejemplo los menús horizontales o las galerías de imágenes.
      Es fundamental conocer cómo interactúan múltiples elementos flotantes unos con otros a fin de utilizarlos correctamente.
      </p>
     <p>Creación de columnas con la propiedad float</p>
     <p>Vamos a aplicar la propiedad float a los divs de contenidos sidebar y main para ver cómo les afecta.</p>
      <ol>Añade el siguiente selector y las reglas de estilo debajo de la regla #mainnav:
        #sidebar {
        float:right;
        width:300px;
        background-color:#CCC;
       }
       Guarda la página y muéstrala en el navegador. La página aparece “rota”. Ahora vas a ver qué es lo que causa que la página salga “rota” como en este caso, ya que este efecto enseña cómo funciona la propiedad float.
       Aunque la página parece rota, los divs están realmente funcionando tal y como debe ser: cuando convertimos en flotante un elemento (en este caso el div sidebar), queda eliminado del flujo normal del HTML. Es por eso que la barra lateral se extiende por todo el contenedor.
       La barra lateral queda flotando, pero se superpone sobre los límites de otros elementos de la página.
       Ahora vamos a declarar como flotante al otro div, hacia el lado izquierdo, y vamos a ver cómo afecta eso a nuestra página. Vuelve al editor.
      </ol>
      <ol>Añade este selector y las reglas de estilo debajo de la regla #sidebar:
      #main {
      width:600px;
      float:left;
      background-color:#ADA446;
     }
     </ol>
     <ol>Guarda el archivo y vuelve a mostrar la página en el navegador.
      El div “main” flota hacia la izquierda, pero el “footer” sube a la parte superior siguiendo el curso o “flujo” de restitución de  la página.
      Al hacer flotar este div hacia la izquierda hemos resuelto el problema de que parte de su contenido apareciera debajo de sidebar; a pesar de que por la cantidad de contenido que tiene el div main parte de él se sale del propio contenedor. También vemos que tenemos otro problema con el elemento footer: debería aparecer en la parte inferior de la página pero no es así.
      Para obligar al div footer a ponerse en la parte inferior de la página le vamos a asignar una nueva propiedad llamada clear.
      </ol>
     <p><b>La propiedad clear </b></p>
     <p>Cuando añadimos la propiedad CSS clear a un objeto, le estamos indicando una regla que dice “no admito elementos flotantes a mi lado”. Podemos especificar si queremos que no haya elementos flotantes a la izquierda, a la derecha o en ambos lados. En el caso del pie de página, queremos eliminarlos de ambos lados.</p>
      <ol>Añade este nuevo selector y sus reglas debajo de las reglas de #main:
        #footer {
        clear:left;
        background-color:#BA2B22;
       }
      </ol>
      <ol>Guarda el archivo y visualízalo en el navegador. Ahora el pie de página queda en la parte inferior del div main. Lo que hace la regla clear:left es impedir la presencia de elementos flotantes a su izquierda. El div main es flotante, por lo que el pie se mueve a la siguiente posición disponible. Cierra el navegador y vuelve al editor.
        El problema es que el div “sidebar” siguen superpuesto al pie y aunque podemos cambiar la regla a clear:right y con ello lo evitaríamos, una forma más segura de resolver esta situación es asegurarnos de que no se van a colocar objetos flotantes ni a su derecha ni a su izquierda.
        </ol>
      <ol>Cambia el valor de la propiedad clear así:
        clear:both;
        De esta forma nos aseguramos de que no habrá elementos flotantes en ambos lados del pie de página.
        </ol>
      <ol>Guarda el archivo y vuelve a mostrarlo en el navegador. Verás que no cambia con respecto al paso 3 pero el pie de página ahora está mejor preparado para cambios futuros en el contenido.</ol>
     <p><b>Creación de un menú de navegación basado en listas con “float” </b></p>
     <p>Ahora que has aprendido los conceptos básicos de “float” y “clear”, volvamos a la sección de la barra de navegación y vamos a añadir un menú sencillo basado en una lista no ordenada Los elementos de la lista dentro de este menú tendrán que ser flotantes para modificar la presentación vertical por defecto de las listas. Los menús de navegación CSS se utilizan mucho en el diseño basado en estándares porque se pueden actualizar y modificar de manera muy sencilla, y porque se basan en textos, lo que mejora la accesibilidad en dispositivos como los lectores de pantalla, e incluso ayudan a mejorar el posicionamiento de nuestras páginas en los buscadores.</p>
     <ol>Desde el editor de textos, busca el div mainnav y añádele la siguiente lista no ordenada y estas líneas:
      &lt;div id="mainnav"&gt;
       &lt;ul&gt;
           &lt;li&gt;&lt;a href="index.html">Home&lt;/a&gt;&lt;/li&gt;
           &lt;li&gt;&lt;a href="ourcompany.html"&gt;Our Company&lt;/a&gt;&lt;/li&gt;
           &lt;li&gt;&lt;a href="policies.html">Policies and Procedures&lt;/a&gt; &lt;/li&gt;
           &lt;li&gt;&lt;a href="doc_repository.html">Document Repository&lt;/a&gt;&lt;/li&gt;
           &lt;li&gt;&lt;a href="news.html">News & Events&lt;/a&gt;&lt;/li&gt;
         &lt;/ul&gt;
      &lt;/div&gt;
      Los elementos de la lista son enlaces a páginas que todavía no existen. Pero necesitamos crear estos enlaces para que se apliquen correctamente los estilos que vamos a declarar ahora.
      </ol>
     <ol>Guarda el archivo y visualízalo en el navegador.
      Fíjate que la página aparece otra vez como “rota”. Esto se debe a que la lista se está superponiendo a la barra lateral flotante. Además la lista no tiene los puntos indicadores. Recuerda que nuestra página está asociada a una hoja de estilo CSS de reset y una de sus reglas declara la propiedad list-style:none, que elimina los puntos indicadores en las listas.
      </ol>
     <ol>Vuelve al editor y localiza la regla #mainnav. Añade una nueva regla entre ésta y la regla de la barra lateral pulsando Intro unas cuantas veces e insertando el código siguiente:
      #mainnav li {
      float:left;
     }
     Fíjate que en este paso estamos creando una nueva regla justo después de #mainnav. Aunque podríamos haber insertado la regla al final de la hoja de estilos, las buenas prácticas recomiendan que se pongan juntas las reglas que tienen relación entre sí para que el código esté más organizado y sea más fácil de mantener.
     </ol>
     <ol>Guarda la página y visualízala en el navegador. Todos los elementos aparecen ahora colocados en horizontal. Los enlaces casi no se ven porque hay muy poco contraste entre el enlace que se escribe en color azul oscuro y el gris oscuro del fondo de la sección “mainnav”, pero lo vamos a resolver añadiendo unas cuantas reglas de estilo más.
     </ol>
     <ol>Vuelve al editor y añade este código a la regla #mainnav li:
      #mainnav li {
         float:left;
        width:170px;
         height:40px;   background-color:#CCC;
             text-align:center;
         border-left:1px black solid;
         border-right:1px black solid;
      }
      En este código hemos hecho estos cambios: hemos definido el recuadro alrededor de cada elemento de la lista con una anchura de 170 pixels  y una altura de 40 pixels. Hemos añadido un color de fondo, hemos alineado cada elemento al centro del recuadro y además, se dibujarán en pantalla los bordes verticales de cada recuadro con un trazo negro de 1 pixel. Guarda el archivo y visualízalo en el navegador. 
      </ol>
     <ol>Debajo de la declaración de border-right, añade esta línea de código:
      line-height:40px;
     </ol>
     <ol>Guarda el archivo y muéstralo en el navegador, El texto aparece ahora centrado dentro del recuadro. Conviene notar que podemos tener problemas si en un futuro cambiásemos el texto de los elementos de la navegación, ya que tanto el valor de “line-height” como el tamaño del propio contenedor se basan en el tamaño de la fuente. Si cambiásemos el tamaño de la fuente o la altura de la sección “nav”, habría que volver a ajustarlo todo para compensar los desplazamientos.</ol>
     <p><b>Añadir estilos para el texto </b></p>
     <p>Hasta aquí hemos añadido los estilos dentro de una hoja de estilos interna en vez de hacerlo sobre una externa. Cuando estamos diseñando la estructura de las páginas, el empleo de hojas de estilo internas es una cuestión de comodidad: resulta más sencillo para crear y modificar reglas si las tenemos dentro de la página y podemos llegar a ellas desplazando la ventana que si las tenemos en un archivo externo. De momento vamos a asociar una hoja de estilos externa que añade reglas de base para elementos como títulos, listas y párrafos.</p>
      <ol>En la parte inicial del archivo HTML busca la etiqueta &lt;link&gt; de la hoja de estilos reset.css. Para añadir otra hoja de estilos externa, selecciona esta línea y pulsa Ctrl + C para copiarla. En la línea siguiente pulsa Ctrl + V para pegarla. Ahora cambia el nombre de archivo “reset.css” por el siguiente “base.css”:
        &lt;link href="reset.css" rel="stylesheet" type="text/css" /&gt;
        &lt;link href="base.css" rel="stylesheet" type="text/css" /&gt;
        </ol>
      <ol>Guarda el archivo y visualízalo en el navegador para ver cómo afectan estos nuevos valores a nuestra página. Ahora los titulares y el texto del cuerpo se escriben utilizando el tipo de letra MS Trebuchet y también se han aplicado algunos otros estilos.
        La página utiliza ahora una hoja de estilos externa para los elementos de texto.
        </ol>
      <ol>Regresa al editor y selecciona el menú Archivo - Abrir. En la ventana que aparece, ve a la carpeta  HTML5_03lessons, selecciona el archivo base.css y pulsa Abrir. Revisa los estilos que incluye este archivo CSS. Mantén abierto el archivo, porque lo vamos a modificar dentro de un momento.
        Existen algunas propiedades CSS adicionales aplicables a las fuentes, como “font-weight”, “text-transform” o “letter-spacing”. 
        </ol>
     <p><b>Efecto de los márgenes internos y externos en una estructura de anchura fija </b></p>
     <p>Las secciones de texto de nuestra página (que en este momento tienen márgenes de cero pixels, por efecto de la hoja de estilos de reset). Vamos a ver ahora algunas estrategias para controlar la estructura visual de la página. El objetivo de esta práctica no consiste en mostrar un método único de organización con CSS, sino en conocer las diferentes opciones posibles, lo que te ayudará en futuros proyectos a la hora de decidir qué método es el más adecuado en cada caso.</p>
     <p><b>Repaso al uso de márgenes internos y externos </b></p>
     <p>Hay dos métodos para separar los elementos dentro de una página. 
      El primero consiste en añadir margen interno (padding) al elemento div contenedor. En este caso la ventaja es que todos los elementos dentro de este div se ven afectados al mismo tiempo, es una solución rápida y eficiente. Su desventaja es que aumenta la anchura total del propio contenedor. Para compensar esta expansión, tenemos que dejar algo de espacio adicional a los lados. Este comportamiento puede generar cierta confusión y provocar que las páginas se restituyan incorrectamente si no tenemos cuidado.
      El segundo método consiste en añadir márgenes externos a los elementos que están dentro del propio div. Su desventaja es que necesitamos más código y hay que prestar atención a los detalles, tenemos que ir viendo cómo se posicionan los elementos individualmente. Su ventaja es que el posicionamiento de la columna es más predecible, puesto que solo tenemos que tener en cuenta una anchura total.
      Finalmente, conviene destacar que lo habitual es aplicar una combinación de ambos métodos en cualquier estructura de presentación. Por tanto, debes conocer bien el comportamiento y los efectos de cada uno de ellos.
      </p>
     <p><b>Aplicar una imagen de fondo al pie de página </b></p>
     <ol>Localiza el div #footer y sustituye todo el contenido de texto que hay dentro por este que aparece aquí
      &lt;div id="footer"&gt;
      &lt;p&gt;Copyright Worldwide Apparel 2011 &lt;/p&gt;
      &lt;p&gt;All content on this site is confidential and should not be shared with anyone outside of Worldwide Apparel. &lt;p&gt;
      &lt;/div&gt;</ol> 
      <ol>Guarda la página y ábrela en el navegador.</ol> 
      <ol>En la hoja de estilos interna, encuentra la regla para el pie de página (“#footer”). Añade una nueva regla para aplicar una imagen de fondo indicando un archivo de la carpeta de imágenes de tu equipo:
        #footer {
        clear:both;
        background-color:#BA2B22;
        background-image:url(images/footer_background.jpg);
        background-repeat:no-repeat;
        }
        La imagen de fondo ahora aparece detrás de los textos.</ol>  
      <ol>Modifica la regla para el pie de página añadiendo las líneas en rojo:
        #footer {
        clear:both;
        background-color:#BA2B22;
        background-image:url(images/footer_background.jpg);
        background-repeat:no-repeat;
        width:960px;
          height:128px;
        }</ol> 
      <ol>En el editor de texto, encuentra la regla #footer y justo debajo añade esta otra regla para párrafos, que se aplicará únicamente a los párrafos del footer:
        #footer p {
          margin:10px 0px 0px 20px;
          width:280px;
          font-family:Verdana, Geneva, sans-serif;
          font-size:0.689em;
        }
        Esta regla añade un margen superior de 10 pixels y margen izquierdo de 20 pixels a ambos párrafos del pie.
      </ol> 
      <ol>Añade la declaración que aparece en rojo a la regla #footer:
        #footer {
          clear:both;
          background-color:#BA2B22;
          background-image:url(images/footer_background.jpg);
          background-repeat:no-repeat;
          width:960px;
          height:128px;
          padding-top:10px;
        }</ol>
      </p>
     <p><b>Ajuste fino de la estructura visual de la página </b></p>
     <p>Ahora vamos a eliminar los colores de fondo de los divs del centro de la página, añadiremos algunas imágenes de fondo y mejoraremos algo el estilo de nuestra barra de navegación.</p>
      <ul>
     <li>1. Elimina toda la propiedad background-color en las siguientes 4 reglas de estilo:  #wrap, #sidebar, #main y #footer. Guarda el archivo y visualízalo en el navegador.</li>
      <li>2. Vamos a empezar por poner un fondo de gradiente de color a la barra lateral. Vuelve al editor y añade estas declaraciones a la regla #sidebar:
       <p>#sidebar { </p>
       <p>float:right;</p>
       <p>width:300px;</p>
       <p>background-image:url(images/sidebar_bg.png);</p>
       <p>background-repeat:repeat-x;</p>
       <p>}</p></li>
      <li>3. Añade también esta otra declaración para aplicarla al borde Izquierdo de la barra.
        #sidebar {
          float:right;
          width:300px;
        background-image:url(images/sidebar_bg.png);
        background-repeat:repeat-x;
        border-left: thin solid gray;
        }</li>
      <li>4. Otro problema de nuestra estructura es el logo dentro de la cabecera. En este momento está anidado y se presenta en pantalla pegado al borde del contenedor:
        #masthead img {
          margin-left: 20px;
        }
        Se trata de un selector contextual igual que otros que hemos ido añadiendo a los títulos y párrafos dentro de las columnas “main” y “sidebar”. En este caso, se trata de una declaración para añadirle margen por la izquierda a todas las imágenes que puedan aparecer en el div “masthead”.</li>
      <li>5. Para mejorar la presencia visual de los enlaces dentro de la sección “mainnav” vamos a añadir una regla explícita para los enlaces. Encuentra la regla #mainnav li y añade la siguiente regla justo debajo de ella:
        #mainnav ul li a {
        color:#ffffff;
        text-decoration: none;
        display:block;
        }</li>
      <li>6. Cuando el usuario pasa el cursor por encima de los enlaces, sería interesante que cambiasen su apariencia, así sabe que se trata de vínculos y no de texto normal. Para ello podemos aprovechar una particularidad de los estilos que solo tienen los vínculos. Justo debajo de la regla #mainnav ul li a , añade esta otra:
        #mainnav ul li a:hover {
        background-color:#666666;
        color:#D2CD2F;
        }</li>
      </ul>
     <p><b>Autoestudio</b></p>
     <p>Para seguir practicando con márgenes internos y externos, añade otros contenidos a la sección “main”. Por ejemplo, puedes añadir un título de nivel 3 y una lista no ordenada entre los dos párrafos:</p>
      <p>&lt;h3&gt;Quick Links&lt;/h3&gt;</p>
      <p>&lt;ul&gt;</p>
      <p><br> &lt;li&gt;New Employee Forms&lt;/li&gt;</p>
      <p><br> &lt;li&gt;Flexible Spending Plans&lt;/li&gt;</p>
      <p><br> &lt;li&gt;401K paperwork&lt;/li&gt;</p>
      <p><br> &lt;li&gt;Employee Discounts&lt;/li&gt;</p>
      <p>&lt;/ul&gt;</p>
     <p><b>Repaso</b></p>
     <p><b>1.	¿En qué consiste un diseño de anchura fija y un diseño de ancho variable?. ¿Qué ventajas y desventajas presentan cada uno de ellos?</b></p>
     <p>En un diseño de anchura fija, el contenedor primario tiene una anchura absoluta. Una de las ventajas principales de este tipo de diseños es que es más fiable a la hora de colocar los demás elementos. Su desventaja más importante es que no altera su tamaño al cambiar las dimensiones de la ventana del navegador.</p>
     <p><b>2.	¿Qué hace la propiedad  float de CSS y cuándo conviene utilizarla?</b></p>
     <p>La propiedad CSS float permite eliminar cualquier elemento dentro del flujo HTML  y moverlo a la derecha o a la izquierda del contenedor. Podemos utilizar la propiedad float cuando queremos que el texto se organice alrededor de imágenes, para crear menús de navegación horizontales o utilizar diseños de página en columnas.</p>
     <p><b>3.	Tu compañero ha añadido un párrafo al div sidebar que ha creado. El párrafo está pegado al borde mismo de la barra lateral. Indícale dos técnicas que puede emplear para separar un poco el párrafo con respecto a los bordes del contenedor</b></p>
     <p>Mi compañero puede añadir un valor de margen interno  a la barra lateral, lo que hará que todos los contenidos se separen automáticamente del borde. También puede añadir una regla para los párrafos dentro del div y aplicar en ella unos valores de margen que separen los textos con respecto al borde</p>
      <br>
     <p><b>Preguntas de la Actividad 3</b></p>
     <p><b>1.- ¿Que es un CSS?</b></p>
     <p></p>
     <p><b>2.- ¿Para que sirve un CSS?</b></p>
     <p></p>
     <p><b>3.- ¿Cual es la diferencia que seria mas difícil de realizar en un sitio web si se optara por no usar un CSS?</b></p>
     <p></p>
        <br>
        <br>
        <h4> Conclusiones </h4>
        <br>
        <b><p>Diego Alberto Oliva Gonzalez </p></b>
        <p></p>
        <b><p>Edrik Alejandro Hernandez Garcia </p></b>
        <p></p>
        <b><p>Carlos Alberto Salazar Beltran </p></b>
        <p>Como conclusión sobre este resumen sobre el curso de HTML de MSDN. El Lenguaje de Marcado de Hipertexto de HTML es el código que se utiliza para estructurar y desplegar una página web y sus contenidos HTML consiste en una serie de elementos que usarás para encerrar diferentes partes del contenido para que se vean o se comporten de una manera determinada. Ya que, los navegadores suelen disponer de un menú con la opción Ver desde la que se puede visualizar el código fuente de la página HTML.</p>
        <b><p>Jesus Ruben Balleza Rojas </p></b>
        <p>En conclusion, esta practica nos fue de mucha ayuda, ya que nos empezamos a meter un poco con CSS que es una parte fundamental para el momento de hacer paginas web con un buen diseño y llamativas. Vimos el elemento div, que nos ayuda para personalizar a nuestro gusto pequeñas partes de la pagina, independientemente de el contenido de esta. Tambien un elemento de CSS que me pareció muy interesante y que no conocía, es el elemento float que lo que hace es que ubica un elemento hacia el lado derecho o el lado izquierdo del contenedor , haciendo que el texto que lo acompañe se situe al lado de la imagen</p>
        <b><p>Diana Nahomi Santos Ortega  </p></b>
        <p>Esta practica fue realmente interesante porque comprendí los diferentes conceptos fundamentales que se involucran en el diseño Web basados en CSS, como también la preparación de una estructura visual de página web con dos columnas y por supuesto su anchura fija. Además, también entendí con mayor facilidad el cómo es el empleo de un archivo de “reset” de CSS y cómo se debe de añadir a las páginas. En esta práctica se aborda el uso del elemento &lt;div&gt; y así mismo las propiedades “float” y “clear” para crear columnas en la página.
        Son temas muy importantes que debemos comprender mucho sobre ellos ya que básicamente comprendiendo esta información es posible ponerla en practica en determinado tiempo con mas facilidad y mejorando cada día para un buen desempeño.</p>
        <br>
        <br>
            <h4>Elaborado por:</h4>
            <table class="default">
              <div class="container-fluid">
                  <tr>
                    <b>
                    <th><h5>Nombre:</h5></th>
                    <th><h5><center>Hora</center></h5></th>
                  </b>
                  </tr>
                  <tr> 
                    <td>Edrik Alejandro Hernandez Garcia</td>
                    <td><center>M5</center></td>
                  </tr>
                  <tr>
                    <td>Diego Alberto Oliva Gonzalez</td>
                    <td><center>M5</center></td> 
                  </tr>
                  <tr>
                      <td>Diana Nahomi Santos Ortega</td>
                      <td><center>M5</center></td>
                  </tr>
                  <tr>
                    <td>Carlos Alberto Salazar Beltran</td>
                    <td><center>M5</center></td>
                  </tr>
                  <tr>
                    <td>Jesús Rubén Balleza Rojas</td>
                    <td><center>M5</center></td>
                  </tr>
              </div>
                </table>
            <!-- Optional JavaScript -->
        <!-- jQuery first, then Popper.js, then Bootstrap JS -->
        <script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
        <script src="https://cdn.jsdelivr.net/npm/popper.js@1.14.7/dist/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.3.1/dist/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
   </body>
</html>
