# Miligram CSS
### Un framewok ligero y minimalista.
**[Milligram CSS](https://milligram.io/)** es un framework para la estilización y maquetación de una aplicación o página web, que se enfoca en la simplicidad y el rendimiento, de ahí que sus características principales sean:

- **Tamaño y rendimiento;** Ocupa muy poco espacio lo que hace ligero y cómodo, y está diseñado para ofrecer un rendimiento óptimo gracias a su poco peso y mejorar la productividad.
- **Características;** Nos ofrece un conjunto completo de las herramientas básicas para el desarrollo web, a pesar de ser ligero y de poco tamaño. Su tipografía por defecto es `Roboto`, y define los tamaños y las fuentes con `rem`, e incluye estilos para elementos comunes, como botones, tablas formularios...
- **Diseño y estructura;** Trabaja con un sistema de grid tipo `flexbox` principalmente, pero es posible cambiarlo a un `grid` de entre 12 y 10 columnas ajustables.
- **Compatibilidad;** Compatible con los navegadores más usados y recientes como Chrome, Firefox, Edge...

### Instalación y uso en Aplicaciones y Webs
La instalación es bastante sencilla solo tenemos que instalar su paquete, con un gestor;

- **Bower:** `$ bower install milligram`
- **npm:** `$ npm install milligram`
- **Yarn:** `$ yarn add milligram`

Y se nos instalara la estructura de paquetes del framework;
````
milligram/
├── dist/
│   ├── milligram.css
│   └── milligram.min.css
├── example.html
├── license
└── readme.md
````
Tenemos que enlazar el archivo `css` a nuestro `html` y listo ya podemos comenzar a usarlo.
````html
<link rel="stylesheet" href="node_modules/milligram/dist/milligram.min.css">
````

Si queremos utilizarlo insertándolo directamente sin instalación de paquete directamente podemos usar:
````html
<!-- Google Fonts Roboto-->
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,300italic,700,700italic">

<!-- CSS Reset -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.css">

<!-- Milligram CSS -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/milligram/1.4.1/milligram.css">
````

### Sintaxis de uso con Ejemplos
Principalmente, la **sintaxis y estilización** de este Framework presenta elementos ya estilizados en `sass`, por lo que se 
aprecia en la instalación del módulo, cuyo cuál aplica una serie de estilos predeterminados a la mayoría de etiquetas
básicas de `html` presentando así una maquetación básica con una estilización minimalista, cuya nos permite un diseño 
rápido y optimizado, aparte podemos encontrar algunas clases predeterminadas y definidas con una serie de estilos listos
para ser aplicados, en ciertos elementos como los botones, y también para el uso del `grid` de la página.

Utilizando muy pocas líneas de código y muy sencillas.
### Tipografía y tamaños
Este utiliza `Roboto` como ya comentamos anteriormente y para medir los tamaños de los elementos se utiliza `rem`
````html
<!-- Tamaño base a utilizar -->
<p>La fuente base parte 1.6 rem (16px), la versión alta de (24px)</p>

<!-- Elementos de marcaje predeterminados -->
<a>Anchor</a>
<em>Emphasis</em>
<small>Small</small>
<strong>Strong</strong>
<u>Underline</u>

<!-- Títulos Predeterminados con tamaños -->
<h1>Heading</h1>
<h2>Heading</h2>
<h3>Heading</h3>
<h4>Heading</h4>
<h5>Heading</h5>
<h6>Heading</h6>
````
Como se puede observar en el ejemplo directamente podemos ver su tamaño principal de `1.6rem` y que 
las etiquetas predeterminadas del propio HTML ya tienen una serie de estilos aplicados que facilita el uso de las etiquetas.

### Blockquotes
La etiqueta `blockquote` también tiene un estilo predeterminado.
````html
<blockquote>
  <p><em>Yeah!! Milligram is amazing.</em></p>
</blockquote>
````

### Buttons
En los botones ya encontramos diferentes clases aplicadas sobre la clase `.button` con estilos predeterminados, para
obtener diferentes estilos.
````html
<!-- Default Button -->
<a class="button" href="#">Default Button</a>

<!-- Outlined Button -->
<button class="button button-outline">Outlined Button</button>

<!-- Clear Button -->
<input class="button button-clear" type="submit" value="Clear Button">
````
Como se aprecia en el código aplicamos directamente estilos con clases, una utilidad
interesante es que se le pueden dar propiedades a los inputs como a los botones y jugar así un poco con los `input`.

### Listas
En las listas encontramos 3 tipos las `ul, ol, dt` básicamente, desordenada, ordenada y descriptiva, estás ya tienen
estilos predeterminados simplemente es usarlas y ya.
````html
<!-- Unordered list -->
<ul>
  <li>Unordered list item 1</li>
  <li>Unordered list item 2</li>
</ul>

<!-- Ordered list -->
<ol>
  <li>Ordered list item 1</li>
  <li>Ordered list item 2</li>
</ol>

<!-- Description list -->
<dl>
  <dt>Description list item 1</dt>
  <dd>Description list item 1.1</dd>
</dl>
````

### Formularios
En los formularios utilizamos las etiquetas predeterminadas de los formularios, combinadas con algunas clases para darle 
un formato y posicionamiento concretos.
````html
<form>
  <fieldset>
    <label for="nameField">Name</label>
    <input type="text" placeholder="Adrii Ucha" id="nameField">
    <label for="ageRangeField">Age Range</label>
    <select id="ageRangeField">
      <option value="0-13">0-13</option>
      <option value="14-17">14-17</option>
      <option value="18-23">18-23</option>
      <option value="24+">24+</option>
    </select>
    <label for="commentField">Comment</label>
    <textarea placeholder="Hi Adrii …" id="commentField"></textarea>
    <div class="float-right">
      <input type="checkbox" id="confirmField">
      <label class="label-inline" for="confirmField">Send a copy to yourself</label>
    </div>
    <input class="button-primary" type="submit" value="Send">
  </fieldset>
</form>
````

Como podemos apreciar se utilizan las etiquetas normales con sus respectivos label asociativos, que le da ya un formato 
predeterminado, pero podemos encontrar algunos elementos con clases en concreto de posicionamiento, como `float-right` 
para alinear la caja a la derecha y el `label-inline` para que no ocupe espacio de bloque y esté al lado del checkbox.

Con esas simples clases podemos jugar y alinear elementos básicos a centro, derecha izquierda...

### Tablas 
Las tablas son como las listas utilizando `thead` y `tbody` ya tenemos unos estilos predeterminados solo hay que usarlos.
````html
<table>
  <thead>
    <tr>
      <th>Nombre</th>
      <th>Edad</th>
      <th>Altura</th>
      <th>Localización</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Stephen Curry</td>
      <td>27</td>
      <td>1,91</td>
      <td>Akron, OH</td>
    </tr>
    <tr>
      <td>Klay Thompson</td>
      <td>25</td>
      <td>2,01</td>
      <td>Los Angeles, CA</td>
    </tr>
  </tbody>
</table>
````

### Grids
Como comentamos antes utiliza un grid de tipo flex en el que simplemente tenemos que aplicar las clases y ajustar el flex
como queramos.

````html
<div class="container">
  <div class="row">
    <div class="column">.column</div>
    <div class="column">.column</div>
    <div class="column">.column</div>
    <div class="column">.column</div>
  </div>
  <div class="row">
    <div class="column">.column</div>
    <div class="column column-50 column-offset-25">.column column-50 column-offset-25</div>
  </div>
</div>
````

En base, a la propiedad que se le agrega al `column` ocupa un espacio normal o anterior junto con el tamaño, combinando
el uso en bloques de `row` y `column` para la alineación de los elementos.

**! Os dejé un [index.html](index.html) donde se aprecia el resultado de la aplicación de estas técnicas.**

### Conclusión 
Para mí, es un framework bastante básico que tiene muy poco contenido, ya que hay otros mucho más potentes, aunque si
buscas realizar un **crm de clientes** con formularios de datos y tablas de base de datos fácil, rápido y sencillo a la hora de estilizar
este es tu framework, porque te da unos estilos muy sencillos y rápidos, y además también brinda la opción de que lo combines con `css`
para darle tu toque en caso de que quieras.

---
_**Adrián Ucha Sousa - Diseño de Interfaces Web**_