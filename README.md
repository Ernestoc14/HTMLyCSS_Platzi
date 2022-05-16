# HTMLyCSS_Platzi
Curso Definitivode HTML y CSS en Platzi
https://platzi.com/cursos/html-css/

Para comentarios usamos ctrl+/
Etiquetas para manejo de:

Imagenes: Mostrar imagenes, src para la root, direccion o url
-Debemos comprimir la Img para que el peso sea menor y renderize mas rapido en el website
<Img> nos permite colocar solo una imagen
        1-Art src: Root, url de donde esta la img
<Figure> nos permite colocar varias imagener 
        Podemos agregarle descripcion a la img
        con una etiqueta extra (<figcaption>)
        -Atributo alt para una pequena descripcion
        en caso no se pueda mostrar la img
        -figcaption: desc similar a la de alt pero
          que pueda ayudar a dar explicacion de que es la imagen
Tipos de Imagenes: 
        -Lossy:(Con perdida)Formato con un poco de perdida de calidad, 
        mejorando la carga mas rapida en el navegador
           -jpg jpeg gama de colores ilimitadas 
        -Lossless:(Sin perdida)Formatos sin perdida, misma calidad, imagenes pesadas
           -gif png  (fondo transparente) 256 colores
           -SVG vector ligero usado para logotipos 
        -Retirar metadatos de tus imagenes
        Metadatos son(fechas de toma de foto, location...)
        -Verexif 

Videos: Muestra videos, atrributo src para url, direc o root 
        1-atriburo controls, sin valor, para el manejo del
        video, play pause etc
        2-atributo preload = "auto", para que el navegador carge el video 
        antes de entrar a la pagina
        3-#t= seg inicio, seg final: funciona para 
        que el video empieze y termine en estos segundos respectivamente
Etiqueta <Source>: para poner videos de diferentes 
        formatos y se pone el src del video.

Formularios: --------
        Etiqueta <Forms>:Le dice al navegador que 
        viene un formulario y que el user dejara informacion que tendriamos que enviar al server
        Etiqueta <label>: Atributo for, es como un identificador de lo que se introduce en el form
        Etiqueta <input>: Atributo type para el manejo de informacion, recoleccion de info de distintos tipos
               1-Atributo id para identificarlo, debe ser igual al for de etiq label.
               2-Atributo name sirve para mandar la info,debe ser el mismo que for y e id
               3-Atributo type submit para enviar info
               4-Atrb autocomplete: el navegador nos ayuda con la respuesta que el usuario siempre pone, para ahorrar tiempo la autocompleta 
               5-Atrb required: Se utiliza para que el user llene los campos que son necesarios (Requeridos)
        Etiqueta <span>: Para agregar texto como descripcion, al lado de la box del form
        Atributo placeholder: Texto de ejemplo que le dice a la persona que info debe ir alli.
Existen dos maneras de crear una lista con distintas opciones.
        La primera es con Etiq <select> permite crear la lista con etiq de <option>
        (Usada para lista con pocas opciones)
        Etiqueta <select>: Sirve para hacer una lista de las opciones de input en un form.
        -Name: es el contenido en relacion a las options
        -Id:
        Etiq <Option> dentro de <select>: Opcion de cada input en la lista a seleccionar

        La segunda es con etiq <input list="  ">
        (Usada para muchas opciones)
        Etiq <datalist>: Permite al user escribir en el input y filtrar su resultado. 
        -Id sera igual al valor que tiene list.
        Etiq <Option> dentro de <datalist>: Opcion de cada input en la lista a seleccionar

Existen dos tipos de botones
        1-Etiq Input type="submit": Por defecto, muestra enviar o submit pero podemos cambiarlo
        con el atrb value="texto a mostrar" 
        (Utilizado en forms para enviar informacion)

        2-Etiq Button: Usado en acciones que no correspondan a "enviar" en un forms
        Muestra el texto entre etiqueta, le podemos poner el 
        atributo type="submit" para usarla en los formularios para que funcione como input 
        (Utilizado en cualquier caso que necesitemos un boton)


CSS  Cascading Style Sheets 
Para agregar CSS a un HTML usamos:
Primero creamos un archivo .css
Etiq <link rel="  " href=" root de css">
        Atrb href: Nos ayuda a referenciar donde esta el .css file 
        (Crear y Ligar el archivo css aqui)=> href="./style.css"
Etiq <style> para agregar pocos estilos de Css

Selectores: (el selector universal es el * )
1-Por elemento de HTML:Parrafo ejm=>p{ css } en el CSS
2-Por Clase: Atriburo class=" nombre" en HTML dentro de etiq
        Llamamos como .nombre{ css} en el CSS
3-Por Id:Art id="nombre" en HTML dentro de etiq
        Llamamos como #nombre{ css } en el CSS

Pseudo clases y pseudo elementos
Esto es a lo que le vamos a agregar estilos una vez tengamos la etiq
-Pseudo Clases: definen el estilo de un estado especial de un elemento
                :class
-Pseudo Elemento: definen el estilo de una parte especifica de un elemento
                ::element

Anatomia o Syntaxis de una regla en CSS
        -Selector/PseudoClase o PsElemento: El elemento que quieres modificar
        -Declaracion del Estilo: -Propiedad -Valor de Propiedad
        Ejm: p (selector){
                color(propiedad): red(valor de propiedad);
                -----------declaracion de estilo-------------
             }

MODELO DE CAJA

        -Margin: Espacio Externo de la caja hacia afuera
        -Border: Linea que define a cada elemento 
        -Padding: Espacio Interno de la caja hacia adentro 
        -Contenido: Elemento(img video texto)
    Width y Height para posicionar la box (top-right-bottom-left)

Box-sizing: Border-box; Hace que se calcule automaticamente el 
tamano del elemento con el padding y border para eliminar scroll horizontal.
        -Suma el padding con el width del elemento 
Tambien podemos hacerlo utilizando el metodo calc(% - px); del Width
        -Ejm: Imagina que quieres colocar 2 cajas dentro de una caja padre y quieres que cada una tome el 50% de ancho, pero que cada una tenga un margen a la izquierda de 10px. Si colocas width de 50% a cada caja y además le colocas margen, esto hará que las cajas queden una arriba de la otra, porque al agregarle 20px de espacio en márgenes, vas a hacer que ya no ajuste el 50% a cada caja.
        (Debes restarle al width, el margin(20px))
        Para hacer que ambas cajas sigan tomando el 50% contando los márgenes, puedes hacer lo siguiente:
                .caja-hijo
                {  width: calc(50% - 20px); 
                }

