<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# MediaQueries

Una vez nos adentramos en el mundo del **Responsive Design**, nos damos cuenta en que hay situaciones en las que determinados aspectos o componentes visuales deben aparecer en un tipo de dispositivos, o deben existir ciertas diferencias.

Para ello, utilizaremos un concepto denominado **media queries**, con los que podemos hacer esas excepciones para que sólo se apliquen a un tipo de diseño concreto.

## **MediasQueries**

---

Las reglas **media queries** (*también denominadas **MQ** a veces*) son un tipo de reglas de CSS que permiten crear un bloque de código que sólo se procesará en los dispositivos que cumplan los criterios especificados como condición.

```css
@media screen and (*condición*) {
  /* reglas CSS */
  /* reglas CSS */
}

@media screen and not (*condición*) {
  /* reglas CSS */
  /* reglas CSS */
}
```

Con este método, especificamos qué queremos aplicar los estilos CSS para tipos de medios concretos (***screen**: sólo en pantallas, en este caso*) que cumplan las condiciones especificadas entre paréntesis.

## **Ejemplos Medias Queries**

---

Veamos un ejemplo clásico de **media queries** en el que definimos diferentes estilos dependiendo del dispositivo que estamos utilizando. Observese que en el código existen 3 bloques **@media** donde se definen estilos CSS para cada uno de esos tipos de dispositivos.

```css
@media screen and (max-width: 640px) {
  .menu {
    background: blue;
  }
}

@media screen and (min-width: 640px) and (max-width: 1280px) {
  .menu {
    background: red;
  }
}

@media screen and (min-width: 1280px) {
  .menu {
    background: green;
  }
}
```

El ejemplo anterior muestra un elemento (*con clase **menu***) con un color de fondo concreto, dependiendo del tipo de medio con el que se visualice la página:

- **Azul** para resoluciones menores a **640 píxeles** de ancho (*móviles*).
- **Rojo** para resoluciones entre **640 píxeles** y **1280 píxeles** de ancho (*tablets*).
- **Verde** para resoluciones mayores a **1280 píxeles** (*desktop*).

Las media queries son una herramienta fundamental en el diseño web responsivo, permitiendo que el diseño de la página se adapte a diferentes tamaños de pantalla y dispositivos. A continuación, os presentamos 10 ejemplos de uso de media queries en CSS con explicaciones detalladas sobre su aplicación.

**Cambiar el Fondo del Menú Basado en el Tamaño de Pantalla:** Este ejemplo cambia el color de fondo del menú en función del tamaño de la pantalla. Esto es útil para mejorar la visibilidad y la estética del menú en diferentes dispositivos.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo 1</title>
    <style>
      .menu {
        padding: 20px;
        color: white;
        text-align: center;
      }

      /* Móviles */
      @media screen and (max-width: 640px) {
        .menu {
          background: blue;
        }
      }

      /* Tablets */
      @media screen and (min-width: 641px) and (max-width: 1280px) {
        .menu {
          background: red;
        }
      }

      /* Desktop */
      @media screen and (min-width: 1281px) {
        .menu {
          background: green;
        }
      }
    </style>
  </head>
  <body>
    <div class="menu">Menú</div>
  </body>
</html>
```

**Ajustar el Tamaño del Texto para Mejorar la Lectura en Diferentes Dispositivos**: Este ejemplo ajusta el tamaño de la fuente para mejorar la legibilidad en diferentes dispositivos. El texto más pequeño en pantallas pequeñas y más grande en pantallas grandes asegura una mejor experiencia de lectura.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo 2</title>
    <style>
      /* Móviles */
      @media screen and (max-width: 480px) {
        body {
          font-size: 14px;
        }
      }

      /* Tablets */
      @media screen and (min-width: 481px) and (max-width: 768px) {
        body {
          font-size: 16px;
        }
      }

      /* Desktop */
      @media screen and (min-width: 769px) {
        body {
          font-size: 18px;
        }
      }
    </style>
  </head>
  <body>
    <p>
      Este es un párrafo de ejemplo para mostrar el cambio de tamaño de texto.
    </p>
  </body>
</html>
```

**Mostrar u Ocultar Elementos Basados en el Dispositivo**: Este ejemplo muestra cómo ocultar una barra lateral en dispositivos móviles para ahorrar espacio y mostrarla en tablets y desktop donde hay más espacio disponible.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo 3</title>
    <style>
      .sidebar {
        background: lightgray;
        padding: 20px;
        color: black;
      }

      /* Ocultar elementos en móviles */
      @media screen and (max-width: 480px) {
        .sidebar {
          display: none;
        }
      }

      /* Mostrar elementos en tablets y desktop */
      @media screen and (min-width: 481px) {
        .sidebar {
          display: block;
        }
      }
    </style>
  </head>
  <body>
    <div class="sidebar">Barra lateral</div>
  </body>
</html>
```

**Modificar la Disposición de la Barra de Navegación**: Este ejemplo ajusta la barra de navegación para que sea vertical en dispositivos móviles y horizontal en tablets y desktop, mejorando la navegación y el uso del espacio.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo 4</title>
    <style>
      .nav {
        background: lightblue;
        padding: 10px;
      }

      .nav a {
        color: white;
        text-decoration: none;
        margin: 5px;
      }

      /* Barra de navegación vertical en móviles */
      @media screen and (max-width: 640px) {
        .nav {
          display: block;
        }
        .nav a {
          display: block;
        }
      }

      /* Barra de navegación horizontal en tablets y desktop */
      @media screen and (min-width: 641px) {
        .nav {
          display: flex;
        }
        .nav a {
          display: inline-block;
        }
      }
    </style>
  </head>
  <body>
    <div class="nav">
      <a href="#">Inicio</a>
      <a href="#">Sobre</a>
      <a href="#">Contacto</a>
    </div>
  </body>
</html>
```

**Cambiar el Número de Columnas en un Grid**: Este ejemplo utiliza CSS Grid para cambiar el número de columnas en un diseño basado en el tamaño de la pantalla, proporcionando una mejor disposición del contenido.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo 5</title>
    <style>
      .grid-container {
        display: grid;
        gap: 10px;
      }

      .grid-item {
        background: lightcoral;
        padding: 20px;
        color: white;
        text-align: center;
      }

      /* Una columna en móviles */
      @media screen and (max-width: 480px) {
        .grid-container {
          grid-template-columns: 1fr;
        }
      }

      /* Dos columnas en tablets */
      @media screen and (min-width: 481px) and (max-width: 768px) {
        .grid-container {
          grid-template-columns: repeat(2, 1fr);
        }
      }

      /* Cuatro columnas en desktop */
      @media screen and (min-width: 769px) {
        .grid-container {
          grid-template-columns: repeat(4, 1fr);
        }
      }
    </style>
  </head>
  <body>
    <div class="grid-container">
      <div class="grid-item">1</div>
      <div class="grid-item">2</div>
      <div class="grid-item">3</div>
      <div class="grid-item">4</div>
    </div>
  </body>
</html>
```

**Ajustar el Tamaño de las Imágenes para Diferentes Dispositivos**: Este ejemplo ajusta el tamaño de las imágenes en función del dispositivo, asegurando que las imágenes se vean bien y se carguen rápidamente en cualquier dispositivo.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo 6</title>
    <style>
      .responsive-image {
        display: block;
        margin: 0 auto;
      }

      /* Imágenes pequeñas en móviles */
      @media screen and (max-width: 480px) {
        .responsive-image {
          width: 100px;
        }
      }

      /* Imágenes medianas en tablets */
      @media screen and (min-width: 481px) and (max-width: 768px) {
        .responsive-image {
          width: 200px;
        }
      }

      /* Imágenes grandes en desktop */
      @media screen and (min-width: 769px) {
        .responsive-image {
          width: 300px;
        }
      }
    </style>
  </head>
  <body>
    <img
      src="https://via.placeholder.com/400"
      alt="Responsive"
      class="responsive-image"
    />
  </body>
</html>
```

**Cambiar la Altura de los Encabezados**: Este ejemplo ajusta la altura de los encabezados para adaptarse mejor a la pantalla del dispositivo, proporcionando un diseño más coherente y accesible.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo 7</title>
    <style>
      header {
        background: lightgreen;
        text-align: center;
        padding: 10px;
        color: white;
      }

      /* Altura de encabezados en móviles */
      @media screen and (max-width: 480px) {
        header {
          height: 50px;
        }
      }

      /* Altura de encabezados en tablets */
      @media screen and (min-width: 481px) and (max-width: 768px) {
        header {
          height: 100px;
        }
      }

      /* Altura de encabezados en desktop */
      @media screen and (min-width: 769px) {
        header {
          height: 150px;
        }
      }
    </style>
  </head>
  <body>
    <header>Encabezado</header>
  </body>
</html>
```

**Ajustar el Margen y el Padding**: Este ejemplo muestra cómo ajustar el margen y el padding en función del tamaño de la pantalla, asegurando que el contenido tenga suficiente espacio en diferentes dispositivos.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo 8</title>
    <style>
      .content {
        background: lightyellow;
        color: black;
      }

      /* Márgenes y padding en móviles */
      @media screen and (max-width: 480px) {
        .content {
          margin: 5px;
          padding: 10px;
        }
      }

      /* Márgenes y padding en tablets */
      @media screen and (min-width: 481px) and (max-width: 768px) {
        .content {
          margin: 10px;
          padding: 20px;
        }
      }

      /* Márgenes y padding en desktop */
      @media screen and (min-width: 769px) {
        .content {
          margin: 20px;
          padding: 30px;
        }
      }
    </style>
  </head>
  <body>
    <div class="content">
      <p>Este es un ejemplo de contenido con diferentes márgenes y padding.</p>
    </div>
  </body>
</html>
```

**Cambiar el Layout de Flexbox**: Este ejemplo utiliza Flexbox para cambiar la dirección de los elementos en función del dispositivo, asegurando una disposición flexible y adaptativa.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo 9</title>
    <style>
      .flex-container {
        display: flex;
        background: lightblue;
      }

      .flex-item {
        background: lightcoral;
        margin: 10px;
        padding: 20px;
        color: white;
        text-align: center;
        flex: 1;
      }

      /* Columnas en móviles */
      @media screen and (max-width: 480px) {
        .flex-container {
          flex-direction: column;
        }
      }

      /* Filas en tablets y desktop */
      @media screen and (min-width: 481px) {
        .flex-container {
          flex-direction: row;
        }
      }
    </style>
  </head>
  <body>
    <div class="flex-container">
      <div class="flex-item">1</div>
      <div class="flex-item">2</div>
      <div class="flex-item">3</div>
    </div>
  </body>
</html>
```

**Ajustar el Diseño de las Tablas**: Este ejemplo adapta el diseño de las tablas para dispositivos móviles, haciendo que las tablas sean más legibles y fáciles de usar en pantallas pequeñas.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo 10</title>
    <style>
      table {
        width: 100%;
        border-collapse: collapse;
      }

      th, td {
        padding: 8px;
        border: 1px solid #ddd;
        text-align: left;
      }

      th {
        background: lightgray;
      }

      /* Tablas adaptativas en móviles */
      @media screen and (max-width: 480px) {
        thead {
          display: none;
        }
        tbody, tr, td {
          display: block;
          width: 100%;
        }
        tr {
          margin-bottom: 10px;
        }
        td {
          text-align: right;
          padding-left: 50%;
          position: relative;
        }
        td::before {
          content: attr(data-label);
          position: absolute;
          left: 10px;
          width: 50%;
          padding-right: 10px;
          white-space: nowrap;
        }
      }
    </style>
  </head>
  <body>
    <table>
      <thead>
        <tr>
          <th>Nombre</th>
          <th>Edad</th>
          <th>País</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td data-label="Nombre">Juan</td>
          <td data-label="Edad">25</td>
          <td data-label="País">España</td>
        </tr>
        <tr>
          <td data-label="Nombre">Ana</td>
          <td data-label="Edad">28</td>
          <td data-label="País">México</td>
        </tr>
        <tr>
          <td data-label="Nombre">Luis</td>
          <td data-label="Edad">32</td>
          <td data-label="País">Argentina</td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
```
**Conclusión**

Las media queries permiten adaptar el diseño de una página web a diferentes dispositivos y tamaños de pantalla, mejorando así la experiencia del usuario. Estos ejemplos ilustran cómo utilizar media queries para hacer que los elementos cambien de estilo y disposición en función del ancho de la pantalla del dispositivo.
