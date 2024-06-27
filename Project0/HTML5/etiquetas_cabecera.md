<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Etiquetas de cabecera

Las etiquetas de cabecera o `<head>` no tienen representación o visualización en el contenido que renderiza el navegador. Por ello, son meta-información adicional que ayuda a definir el comportamiento y la estructura del documento HTML.

## Etiquetas de relación

---

Bienvenidos a la sección de **cabeceras** de HTML. Cuando hablamos de la estructura de un documento de **HTML5**, una parte importante es la cabecera o `<head>`. Ahora vamos a ver las etiquetas más importantes que se suelen usar dentro de esta.

El `<head>` es un contenedor de metadatos (datos sobre datos). Los metadatos HTML son datos que no se muestran al usuario pero que describen el documento HTML. Además, contiene el título del documento y el enlace a las hojas de estilos que asociemos.

En resumen, el elemento HTML `<head>` se coloca entre la etiqueta `<html>` y la etiqueta `<body>` y es un contenedor para los siguientes elementos: `<title>`, `<style>`, `<meta>`, `<link>`, `<script>` y `<base>`.

## Etiquetas de relación: Título y Codificación

---

Dentro de `<head>` es aconsejable usar las etiquetas `<title>` y `<meta>`.

```html
<head>
  <title>Título</title>
  <meta charset="utf-8" />
</head>
```

- **`<title>`**: El `<title>` es el nombre que se muestra en la ventana de nuestro navegador. Este título aparece en la pestaña del navegador y es importante para el SEO (Search Engine Optimization).
- **`<meta charset="utf-8">`**: La etiqueta `<meta>` con el atributo charset indica al navegador que utilice la codificación UTF-8 para mostrar el texto. De este modo evitaremos problemas con vocales acentuadas, o caracteres como “ñ”.

## Etiquetas de relación: Favicon

---

El Favicon es un icono que hace referencia a nuestra aplicación. Es una pequeña imagen que se muestra junto al título de la página en la pestaña del navegador.

Para agregar un favicon a nuestra web, tenemos que crear una carpeta en la raíz de nuestro proyecto llamada `assets` y guardar la imagen de favicon en esta carpeta. Un nombre común para una imagen de favicon es "favicon.ico".

Para ello tenemos que hacer uso de la etiqueta `<link>` con dos atributos `rel="icon"` y `href="ruta-imagen"` como en el ejemplo.

```html
<head>
  <link rel="icon" href="./assets/favicon.ico" />
</head>
```

## Etiquetas de relación: Añadir hoja de estilos CSS y Script

---

También dentro de nuestra cabecera enlazamos tanto los ficheros de estilos como los de scripting. Para ello, vamos a crear un fichero CSS3 en la raíz del proyecto llamado `styles.css` y otro JS en la raíz del proyecto también llamado `main.js`. Y los vamos a enlazar.

```html
<head>
  <link rel="stylesheet" href="styles.css" type="text/css" />
  <script type="text/javascript" src="./main.js"></script>
</head>
```

Para comprobar que ya están enlazados, podemos usar el siguiente ejemplo:

```html
<!-- En el index.html -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script type="text/javascript" src="./main.js"></script>
    <link rel="stylesheet" href="./styles.css" />
    <title>My first document</title>
  </head>
  <body>
    <p>Esto es una prueba de que funciona la conexión entre archivos</p>
  </body>
</html>
```

```css
/* Styles.css */
p {
    color: blueviolet;
}
```

## Etiquetas de relación: Meta Viewport

---

El `name="viewport"` dentro de la etiqueta `<meta>` define el área visible del usuario de una página web. Varía según el dispositivo: será más pequeño en un teléfono móvil que en la pantalla de un portátil.

Cuando tenemos una aplicación web optimizada para dispositivos móviles, deberemos añadir la siguiente etiqueta.

```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

Esto le da al navegador instrucciones sobre cómo controlar las dimensiones y la escala de la página.

- `width=device-width` establece el ancho de la página (que variará según el dispositivo).
- `initial-scale=1.0` establece el nivel de zoom inicial cuando el navegador carga la página por primera vez.

## Etiquetas de relación: Compatibilidad con Navegadores

---

**X-UA-compatible** en HTML es otro meta-tag útil en la página HTML y este meta-tag se relaciona mayormente con el navegador. **El modo Edge** le dice a Internet Explorer que muestre el contenido en el modo más alto disponible.

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

## Etiquetas de Metadatos

---

La etiqueta de metadatos es `<meta>` y ofrece una gran cantidad de opciones dentro de la cabecera de un documento HTML. Puede contener los atributos `name` y `content` y servirán para indicar metadatos al documento.

Son usados por los buscadores para definir la información principal de nuestra web (temática, descripción), por lo que será muy importante que lo tengamos correctamente configurados.

```html
<head>
  <meta name="theme-color" content="#4285f4" />
  <meta name="description" content="Esta es la descripción en metadatos" />
  <meta name="keywords" content="web, programar, site, metadatos" />
  <meta name="author" content="Alberto Rivera" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
</head>

```

## Otros Metadatos incluidos por Google

---

Usando el atributo `google`, podemos establecer valores como `nositelinkssearchbox`, que indica a Google que no muestre el buscador en [sitelinks](https://developers.google.com/search/docs/appearance/sitelinks?hl=es), y el valor `notranslate` para indicar que no se debe traducir la página.

Por último, el atributo `robots` recibe parámetros y se le indica al robot de Google si debe indexar la página o no.

```html
<head>
  <meta name="google" content="nositelinkssearchbox" />
  <meta name="google" content="notranslate" />
  <meta name="robots" content="index, nofollow" />
  <meta name="googlebot-news" content="nosnippet">
</head>
```

Existe además un último atributo `http-equiv` usado para que los robots del buscador sepan que se deben cambiar las cabeceras HTTP al realizar ciertas acciones.

```html
<head>
  <!-- refresh redirige a la URL pasados los segundos indicados -->
  <meta http-equiv="refresh" content="300;url=http://www.google.com/" />
  <!-- Expires es la fecha a partir de la que consideramos la página expirada -->
  <meta http-equiv="expires" content="Fri, 29 Apr 2016 12:56:00 GMT" />
  <!-- Pragma indica si queremos que se guarde o no la caché -->
  <meta http-equiv="pragma" content="no-cache" />
  <!-- Este es el especial que indica a Internet si debe o no guardar la caché -->
  <meta http-equiv="cache-control" content="no-cache" />
</head>
```

## Etiquetas Metadatos: Redes Sociales (RRSS)

---

Para añadir título y descripción a una página web lo hacemos con etiquetas de metadatos, existen un tipo de etiquetas de metadatos especiales orientadas a redes sociales. Así, se pueden añadir títulos y descripciones especiales para estos sitios.

Open Graph (Facebook)

```html
<head>
  <title>The Rock (1996)</title>
  <meta property="og:title" content="The Rock" />
  <meta property="og:type" content="video.movie" />
  <meta property="og:url" content="https://www.imdb.com/title/tt0117500/" />
  <meta
    property="og:image"
    content="https://ia.media-imdb.com/images/rock.jpg"
  />
</head>
```

Twitter Cards

```html
<head>
  <meta property="twitter:card" content="summary_large_image" />
  <meta property="twitter:creator" content="@Alberto" />
  <meta property="twitter:title" content="Título" />
  <meta property="twitter:description" content="Descripción" />
  <meta property="twitter:image:src" content="mi_imagen.jpg" />
</head>
```

Para usar [Twitter Cards](https://developer.twitter.com/en/docs/twitter-for-websites/cards/guides/getting-started) debemos registrarnos previamente en [Twitter Developers](https://developer.twitter.com/en) y deberán analizar si nuestra web cumple o no los requisitos.

**Conclusión**
Entender y utilizar adecuadamente las etiquetas de cabecera y los metadatos en HTML es crucial para asegurar que nuestras páginas web sean accesibles, optimizadas y bien indexadas por los motores de búsqueda.

## Reto Coding

---

Crear un documento HTML que utilice etiquetas de metadatos y de cabecera para optimizar la página web y mejorar su interacción con redes sociales.

### Instrucciones:

1. **Crea un documento HTML** que incluya:
    - Título del documento.
    - Metadatos para la codificación de caracteres y viewport.
    - Favicon.
    - Enlace a una hoja de estilos CSS.
    - Inclusión de un archivo JavaScript.
    - Metadatos de descripción, autor y palabras clave.
    - Metadatos para mejorar la interacción con redes sociales usando Open Graph y Twitter Cards.
2. **Contenido del archivo**:
    - El archivo debe incluir una estructura básica de HTML5.
    - Debe contener un encabezado `<head>` con todas las etiquetas mencionadas anteriormente.
    - Debe contener un cuerpo `<body>` con algún contenido mínimo, como un párrafo.

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta
      name="description"
      content="Esta es una página de ejemplo para aprender sobre metadatos y cabeceras en HTML."
    />
    <meta name="keywords" content="HTML, metadatos, cabeceras, tutorial" />
    <meta name="author" content="Alberto Rivera" />
    <meta name="theme-color" content="#4285f4" />
    <meta name="robots" content="index, follow" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />

    <link rel="icon" href="./assets/favicon.ico" />
    <link rel="stylesheet" href="styles.css" type="text/css" />
    <script type="text/javascript" src="main.js"></script>

    <meta property="og:title" content="Página de Ejemplo" />
    <meta property="og:type" content="website" />
    <meta property="og:url" content="https://www.ejemplo.com" />
    <meta property="og:image" content="https://www.ejemplo.com/imagen.jpg" />

    <meta property="twitter:card" content="summary_large_image" />
    <meta property="twitter:creator" content="@Alberto" />
    <meta property="twitter:title" content="Página de Ejemplo" />
    <meta
      property="twitter:description"
      content="Esta es una página de ejemplo para aprender sobre metadatos y cabeceras en HTML."
    />
    <meta
      property="twitter:image:src"
      content="https://www.ejemplo.com/imagen.jpg"
    />

    <title>Página de Ejemplo</title>
  </head>
  <body>
    <p>
      Bienvenidos a nuestra página de ejemplo sobre metadatos y cabeceras en
      HTML.
    </p>
  </body>
</html>
```
## Contenido asociado
---
- [Video: Etiquetas de cabecera](https://vimeo.com/846222882/057c8d8840)
