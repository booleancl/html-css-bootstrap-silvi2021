# HTML CSS BOOTSTRAP

Html css y javascript son los pilares de toda aplicación o sitio web.
cualquier cosa que funcione dentro de un navegador web(chrome,mozilla 
o safari) utiliza estos pilares. Y no solo eso, hoy tambien  se pueden
hacer aplicaciones "nativas" con estas tecnologías.

## HTML 

Significa **Hiper Text Markup Language*, que en castellano sería algo
como Lenguaje de marcada de hiper texto.Lenguaje de marcado es por la
*Etiquetas*. Dependiendo de su etiqueta al navegador lo procesa de 
diferente forma.Y el hipeer texto se refiere a que estos documentos
están enlazados por *links*.

Con HTML crearemos *documentos estructurados* mediante etiquetas que el 
navegador puede interpretar.

El documento principal de un sitio o aplicación se debe llamar
**index.html*. Todo junto y en minúsculas.

### Un poquito de historia

HTML inicialmente estaba pensado para transmitir
documentación cientifica. Y se necesitaba una forma de indicar que secciones del documento eran párrafos,imágenes,títulos y encabezados. Con este motivo nació  HTML.

### Doctype

Esta primera etiqueta indica al navegador la versión de HTML.En 
este caso indica que es la versión 5.

```html
   <!DOCTYPE html>
```

### Html

Luego de eso viene la etiqueta que es parte
del documento. La famosa etiqueta **html**:

```html
<html lang="es">
    ...
</html>
```

Del ejemplo anterior vemos que esta etiqueta se compone
de 2 partes principales.La etiqueta de apertura `<html>`
y la de cierre `</html>`

Entremedio de las etiquetas de apertura y cierre irá el contenido.

Además vemos que la etiqueta de apertura tiene el 
**atributo** `lang="es`, lo que le indica la navegador
en qué idioma está el documento.


**ATENCIÓN**: Solo las etiquetas de apertura pueden 
tener atributos, las etiquetas de cierre no.


### Head

A continuación viene la etiqueta `head`. Esta etiqueta
entrega información al **navegador** sobre como visualizar
el contenido que vendrá en las siguientes secciones. Por
ejemplo se indica mediante etiquetas `meta` el set de carateres
que utilizará la paginá.
Ejemplo:

```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible"
    content="IE=edge">
    <meta name="viewport" 
    content="width=device-width, 
    initial-scale=1.0">
    <title>Hola Microsystem</title>
</head>
```

La tercera etiqueta `meta` que tiene el atributo 'name="viewport'
permite que el contenido se cargue inicialmemnte considerando el 
tamaño de pantalla disponoble,
desde grandes a muy pequeños.

Además dentro del head se encuentra la etiqueta `title`, que es la
encargada de mostrar el nombre del sitio en la pestaña del navegador

Por otra parte dentro del `head` podemos cargar otros recursos que
utilizará el docuemnto como por ejemplo hojas de estilo CSS o archivos
de Javascript

### Estructuras Jerárquicas

Algo que es muy muy importante notar  y que no es tan evidente,
es que los documentos HTML forman una estructura jerarquica bien
definida del tipo árbol. Donde la etiqueta raíz es la etiqueta 
`html`. Lo podemos visualizar de la siguiente forma

```html
  <html>
    <head></head>
    <body></body>
  </html>
```

Esto es muy importante de comprender ya que luego
manejaremos las etiquetas pensando en su ubicación relativa dentro
del árbol. Y pensaremos que las etiquetas son **nodos** que tiene 
**nodos padres**, **hermanos** y **nodos hijos**.


## Etiquetas principales

Podemos separar las etiquetas en 2 tipos:
semánticos y no semánticos.

### Títulos

Las etiquetas para hacer títulos son  las etiquetas **h**
con números del 1 al 6. Ejemplos

```html
    <h1>Súper título</h1>
    <h2>Súper subtitulo</h2>
    <h3>super sub sub titulo</h3>
    <h4>...</h4>
    <h5>...</h5>
    <h6>...</h6>
```    

## Links

Los links son el corazon de internet y los crearemos frecuentemente. 
Se componen de el atributo `href` que significa el destino del link
y su contenido,que es lo que se muestra al usuario

```html
 <a href="headings.html">Títulos</a>
 ```

### Imagenes

Las imágenes son una de las etiquetas que no requiere de cierre ya que
la imagen que se despliega se indica mediante el atributo `src` y en 
caso que la imagen no este disponible se despliega el texto indicado 
en el atributo `alt` conocido como texto alternativo.

### Listas

#### Ordenadas

```html
    <ol>Días de la semana
        <li>Lunes</li>
        <li>Martes</li>
        <li>Miercoles</li>
        <li>Jueves</li>
        <li>viernes</li>
    </ol>

#### No ordenadas

```html

<ul>  pilares de la web  
    <li>HTML</li>    
    <li>CSS</li>    
    <li>Javascript</li>    
</ul>
```

### Tablas

<table>
        <tr>
            <th>Italiano</th>
            <th>Chacarero</th>
        </tr>
        <tr>
            <td>Tomate</td>
            <td>Lechuga</td>
        </tr>
        <tr>
            <td>Palta</td> 
            <td>Porotos</td>    
        </tr>
        <tr>
            <td>Mayo</td>
            <td>Aji</td>
        </tr>
    </table>

### Etiquetas no semánticas

    Estas etiquetas no tienen un significado propio y sirven como contenedor para agrupar otras etiquetas

## div 

    ```html
    <div>
        <p>Hola mundo</p>
    </div>
    ```

## spam

    La etiqueta span se puede usar dentro de un texto.

    ```html
    <div>
        <p>Hola <span>mundo</span></p>
    </div>
    ```

La idea detrás de los elementos no semánticos es utilizar CSS para darles estilo.

Más adelante,en este módulo veremos lo frecuente de su uso con el marco de trabajo o framework Booststrap.

## Formularios
Contiene controles interactivos para ingresar información 

```html
<form action="/search" method="get">
...
</from>
```

Cuando enviamos el formulario mediante el método `get`,los parámetros ingresados quedan reflejados en la url después del signo `?` y separados por `&`

## CSS

hojas de estilo en cascada(Cascade style Sheets)
CSS nos permite entregar al sitio el aspecto que queremos.Lo hace
aplicando reglas de estilo soobre los diferentes elementos del HTML.

Los navegadores tienen estilos predefinidos para mostrar las diferentes
etiquetas.

Cuando el código CSS está definido dentro del mismo archivo html,
se denomina css-inline,pero no es la mejor forma de definir los estilos
que se van a utilizar en varias páginas.Para eso es mejor utilizar un
archivo externo y vincularlo al html.

### Sintaxis CSS

Las reglas CSS parten con un selector,luego dentro de las llaves se ingresan
las propiedades junto con su valor.
ejemplos

```css
h2{
    color: blue;
    font-size: 24px;
}

selector{
    propiedad:valor;
    propiedad:valor;
}

p{
   color:red;
   text-align: center;
}

```

## Selectores

En el ejemplo anterior el selector era la misma etiqueta,es decir, la regla 
de estilo aplica a **todas** las etiquetas de ese tipo. Tenemos otros 2 selectores
muy frecuentes.El selector por `id` y por `clase`.

El `id` es un atributo de las etiquetas HTML.Toda etiqueta HTML puede tener el atributo
`id` para diferenciarlo del resto. Y podemos usar ese atributo como selector css usando
la notación `#`

```css
#fname{
    border-radius: 6px;
}
```



