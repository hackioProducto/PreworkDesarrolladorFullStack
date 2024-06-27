<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Etiquetas multimedia

Cuando hablamos de etiquetas que representan contenido audiovisual, nos referimos a imágenes, vídeos, audios e iframes que permiten incrustar aplicaciones e interactuar con ellas.

## Etiqueta `<img>`

---

Para incluir una imagen, usamos la etiqueta `<img>`. Los atributos obligatorios son `src` y `alt`.

```html
<img src="ruta" alt="texto alternativo"/>
```

- **`src`**: Especifica la ruta de la imagen.
- **`alt`**: Proporciona texto alternativo si la imagen no se carga.

Otros atributos útiles son `width` y `height`, que especifican las dimensiones de la imagen.

```html
<img src="ruta" alt="texto alternativo" width="200" height="200"/>

```

Formatos de Imagen

| Formato | Descripción | Se recomienda |
| --- | --- | --- |
| PNG | Soporta transparencia. Compresión sin pérdidas. Ideal para imágenes con áreas de color plano. | Sí |
| JPG | Compresión con pérdidas. Ideal para imágenes con texturas y fotos. | Sí |
| SVG | Formato vectorial. Ideal para imágenes escalables y logotipos. | Sí |
| GIF | Formato para imágenes pequeñas y animadas. | Intentar evitar |
| WEBP | Alternativa de Google al JPEG. Soporta transparencias y compresión tanto con pérdidas como sin pérdidas. | Sí, con precaución |
| JPEG2000 | Evolución del JPEG. | No, solo Safari |
| JPEG-XR | Alternativa de Microsoft al JPEG. | No, solo IE |
| APNG | Alternativa libre a GIF. Compatible con PNG. Soporta animaciones. | Sí, con precaución |
| AVIF | Formato de imagen basado en AV1. | Poco soporte |
| JPEG-XL | Alternativa competidora a AVIF. | Poco soporte |

## Ejemplo de uso de la etiqueta `<img>`

---

Imagen básica

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Imagen Básica</title>
  </head>
  <body>
    <h1>Ejemplo de Imagen Básica</h1>
    <img src="imagen.jpg" alt="Descripción de la imagen" />
  </body>
</html>
```

Imagen con dimensiones específicas

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Imagen con Dimensiones</title>
</head>
<body>
    <h1>Ejemplo de Imagen con Dimensiones</h1>
    <img src="imagen.jpg" alt="Descripción de la imagen" width="200" height="200">
</body>
</html>
```

Ejemplos de formatos de imagen

```html
<img src="imagen.png" alt="Imagen en formato PNG">
```

```html
<img src="imagen.jpg" alt="Imagen en formato JPG">
```

```html
<img src="imagen.svg" alt="Imagen en formato SVG">
```

```html
<img src="imagen.gif" alt="Imagen en formato GIF">
```

```html
<img src="imagen.webp" alt="Imagen en formato WEBP">
```

Ejemplo de imágenes con diferentes formatos

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Formatos de Imagen</title>
  </head>
  <body>
    <h1>Ejemplo de Formatos de Imagen</h1>
    <p>Imagen PNG:</p>
    <img
      src="imagen.png"
      alt="Imagen en formato PNG"
      width="100"
      height="100"
    />

    <p>Imagen JPG:</p>
    <img
      src="imagen.jpg"
      alt="Imagen en formato JPG"
      width="100"
      height="100"
    />

    <p>Imagen SVG:</p>
    <img
      src="imagen.svg"
      alt="Imagen en formato SVG"
      width="100"
      height="100"
    />

    <p>Imagen GIF:</p>
    <img
      src="imagen.gif"
      alt="Imagen en formato GIF"
      width="100"
      height="100"
    />

    <p>Imagen WEBP:</p>
    <img
      src="imagen.webp"
      alt="Imagen en formato WEBP"
      width="100"
      height="100"
    />
  </body>
</html>
```

**Conclusión**

Las etiquetas de contenido audiovisual en HTML, como `<img>`, permiten a los desarrolladores incluir y gestionar imágenes de manera eficiente. Con el conocimiento de los formatos de imagen y sus usos recomendados, puedes seleccionar el formato adecuado para cada situación y mejorar la experiencia del usuario y el rendimiento del sitio web. Utiliza los atributos `src` y `alt` correctamente para asegurar que las imágenes se carguen correctamente y que haya texto alternativo disponible si las imágenes no se cargan.

## Etiqueta `<picture>`

---

La etiqueta `<picture>` se utiliza para definir diferentes versiones de una imagen según el tamaño de la pantalla. Esto permite a los desarrolladores proporcionar imágenes optimizadas para diferentes dispositivos y resoluciones, mejorando el rendimiento y la experiencia del usuario.

La etiqueta `<picture>` contiene una serie de etiquetas `<source>` y una etiqueta `<img>`. Las etiquetas `<source>` especifican diferentes versiones de la imagen basadas en consultas de medios (media queries), mientras que la etiqueta `<img>` proporciona una imagen de respaldo si ninguna de las consultas de medios coincide.

## Ejemplos de uso de la etiqueta `<picture>`

---

1. **`<picture>`**: Contenedor para las versiones de la imagen.
2. **`<source>`**: Define una versión de la imagen y las condiciones bajo las cuales debe mostrarse.
    - **`media`**: Especifica las condiciones (media queries) en las que se utilizará esta versión de la imagen.
    - **`srcset`**: Especifica la ruta de la imagen que debe usarse cuando se cumplen las condiciones del atributo `media`.
3. **`<img>`**: Imagen de respaldo que se muestra si ninguna de las condiciones de las etiquetas `<source>` se cumple.
    - **`src`**: Ruta de la imagen de respaldo.
    - **`alt`**: Texto alternativo para la imagen.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Picture</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
    </style>
</head>
<body>
    <h1>Ejemplo de Uso de la Etiqueta `<picture>`</h1>
    <picture>
        <source media="(min-width: 600px)" srcset="imagen-xl.png" />
        <source media="(min-width: 300px) and (max-width: 600px)" srcset="imagen-large.png" />
        <source media="(max-width: 300px)" srcset="imagen-small.png" />
        <img src="imagen-medium.png" alt="Ejemplo de imagen" />
    </picture>
    <p>Esta imagen cambia según el tamaño de la pantalla.</p>
</body>
</html>
```

Imagen adaptativa para diferentes resoluciones

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Imagen Adaptativa</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          margin: 20px;
      }
    </style>
  </head>
  <body>
    <h1>Imagen Adaptativa</h1>
    <picture>
      <source media="(min-width: 1200px)" srcset="imagen-4k.png" />
      <source media="(min-width: 800px)" srcset="imagen-hd.png" />
      <source media="(min-width: 400px)" srcset="imagen-sd.png" />
      <img src="imagen-default.png" alt="Imagen adaptativa según resolución" />
    </picture>
    <p>La imagen cambia según la resolución de la pantalla.</p>
  </body>
</html>
```

Imagen adaptativa para diferentes dispositivos

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Imagen para Diferentes Dispositivos</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          margin: 20px;
      }
    </style>
  </head>
  <body>
    <h1>Imagen para Diferentes Dispositivos</h1>
    <picture>
      <source media="(orientation: landscape)" srcset="imagen-landscape.png" />
      <source media="(orientation: portrait)" srcset="imagen-portrait.png" />
      <img src="imagen-default.png" alt="Imagen adaptativa según dispositivo" />
    </picture>
    <p>La imagen cambia según la orientación del dispositivo.</p>
  </body>
</html>
```

Imagen con diferentes formatos

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Imagen con Diferentes Formatos</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          margin: 20px;
      }
    </style>
  </head>
  <body>
    <h1>Imagen con Diferentes Formatos</h1>
    <picture>
      <source type="image/webp" srcset="imagen.webp" />
      <source type="image/jpeg" srcset="imagen.jpg" />
      <img src="imagen.png" alt="Imagen en diferentes formatos" />
    </picture>
    <p>La imagen cambia según el formato soportado por el navegador.</p>
  </body>
</html>
```

**Conclusión**
La etiqueta `<picture>` en HTML es una herramienta poderosa para proporcionar imágenes adaptativas, permitiendo cargar diferentes versiones de una imagen según el tamaño de la pantalla, la orientación del dispositivo o el formato soportado por el navegador. Esto mejora el rendimiento y la experiencia del usuario al asegurar que siempre se cargue la imagen más adecuada para cada situación.

## Etiqueta `<map>`

---

La etiqueta `<map>` se utiliza para crear mapas de imagen con áreas en las que se puede hacer clic. Esto permite que diferentes partes de una imagen actúen como enlaces, redirigiendo al usuario a distintas páginas o mostrando información específica cuando se hace clic en ellas.

La etiqueta `<map>` contiene una serie de etiquetas `<area>`, cada una de las cuales define un área interactiva de la imagen. La imagen a la que se aplica el mapa se referencia mediante el atributo `usemap`.

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Mapa de Imagen</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          margin: 20px;
      }
    </style>
  </head>
  <body>
    <h1>Ejemplo de Mapa de Imagen</h1>
    <img
      src="ruta-de-la-imagen/mapa.png"
      alt="MDN infographic"
      usemap="#infographic"
    />
    <map name="infographic">
      <area
        shape="rect"
        coords="34,44,270,350"
        href="https://developer.mozilla.org/docs/Web/HTML"
        target="_blank"
        alt="HTML"
      />
      <area
        shape="circle"
        coords="337,300,44"
        href="https://developer.mozilla.org/docs/Web/CSS"
        target="_blank"
        alt="CSS"
      />
      <area
        shape="poly"
        coords="130,147,200,107,254,219,130,228"
        href="https://developer.mozilla.org/docs/Web/JavaScript"
        target="_blank"
        alt="JavaScript"
      />
    </map>
    <p>
      Pasa el cursor sobre la imagen y haz clic en las diferentes áreas para
      aprender más sobre HTML, CSS y JavaScript en MDN.
    </p>
  </body>
</html>
```

1. **`<img usemap="#infographic" src="ruta-de-la-imagen/mapa.png" alt="MDN infographic" />`**:
    - **`usemap`**: Atributo que enlaza la imagen con el mapa de la imagen.
    - **`src`**: Ruta de la imagen.
    - **`alt`**: Texto alternativo para la imagen.
2. **`<map name="infographic">`**:
    - Define un mapa de imagen con el nombre "infographic".
3. **`<area>`**:
    - Define una área en la imagen donde se puede hacer clic.
    - **`shape`**: Forma del área (rectángulo `rect`, círculo `circle`, polígono `poly`).
    - **`coords`**: Coordenadas que definen el área.
    - **`href`**: URL a la que se redirige cuando se hace clic en el área.
    - **`target`**: Define dónde se abrirá el enlace (e.g., `_blank` para abrir en una nueva pestaña).
    - **`alt`**: Texto alternativo para el área.

## Atributos del área

---

- **`shape`**:
    - `rect`: Define un área rectangular. Las coordenadas `coords` son `x1,y1,x2,y2`.
    - `circle`: Define un área circular. Las coordenadas `coords` son `x,y,r` (centro y radio).
    - `poly`: Define un área poligonal. Las coordenadas `coords` son una lista de pares `x,y`.
- **`coords`**: Especifica las coordenadas de los puntos que definen la forma del área.

Área Rectangular : Coordenadas `(34,44)` y `(270,350)` definen los vértices opuestos del rectángulo.

```html
<area shape="rect" coords="34,44,270,350" href="https://developer.mozilla.org/docs/Web/HTML" target="_blank" alt="HTML"/>
```

Área Circular: Coordenadas `(337,300)` definen el centro del círculo y `44` define el radio.

```html
<area shape="circle" coords="337,300,44" href="https://developer.mozilla.org/docs/Web/CSS" target="_blank" alt="CSS"/>
```

Área Poligonal: Coordenadas `130,147`, `200,107`, `254,219`, `130,228` definen los vértices del polígono.

```html
<area shape="poly" coords="130,147,200,107,254,219,130,228" href="https://developer.mozilla.org/docs/Web/JavaScript" target="_blank" alt="JavaScript"/>
```

**Conclusión**
La etiqueta `<map>` junto con `<area>` permite crear mapas de imagen interactivos, donde diferentes áreas de la imagen pueden actuar como enlaces a diferentes recursos. Esto es útil para infografías y diagramas interactivos, proporcionando una forma visual e intuitiva de navegar por el contenido.

## Etiqueta `<iframe>`

---

Para insertar contenido como vídeos, audios y aplicaciones de servicios externos, usamos etiquetas como `<iframe>`, `<embed>` y `<object>`. Estas etiquetas permiten incrustar y mostrar contenido que no forma parte del documento HTML original.

La etiqueta `<iframe>` se utiliza para incrustar aplicaciones o contenido externo, como vídeos de YouTube, páginas web, mapas de Google, entre otros.

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Iframe</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          margin: 20px;
      }
      iframe {
          border: none;
      }
    </style>
  </head>
  <body>
    <h1>Ejemplo de Uso de Iframe</h1>
    <iframe
      width="560"
      height="315"
      src="https://www.youtube.com/embed/VIDEO_ID"
      title="YouTube video player"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    ></iframe>
  </body>
</html>
```

Atributos comunes de `<iframe>`

- **`width`**: Define el ancho del iframe.
- **`height`**: Define la altura del iframe.
- **`src`**: Especifica la URL de la página que se va a incrustar.
- **`title`**: Proporciona un título accesible para el iframe.
- **`frameborder`**: Define el grosor del borde del iframe (usualmente `0` o `1`).
- **`allow`**: Especifica permisos para el contenido del iframe (por ejemplo, `autoplay` para reproducir automáticamente un vídeo).
- **`allowfullscreen`**: Permite que el iframe se muestre en pantalla completa.

## Etiquetas `<embed>` y `<object>`

---

Antiguamente se usaba `<embed>` para incrustar contenido como animaciones Flash, pero actualmente se recomienda usar `<object>` para un mayor control y compatibilidad.

### `<embed>`

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Embed</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          margin: 20px;
      }
    </style>
  </head>
  <body>
    <h1>Ejemplo de Uso de Embed</h1>
    <embed
      src="path-to-your-file.swf"
      width="400"
      height="300"
      type="application/x-shockwave-flash"
    />
  </body>
</html>
```

### `<object>`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Object</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
    </style>
</head>
<body>
    <h1>Ejemplo de Uso de Object</h1>
    <object data="path-to-your-file.swf" width="400" height="300">
        <param name="quality" value="high">
        <embed src="path-to-your-file.swf" width="400" height="300" quality="high" type="application/x-shockwave-flash"></embed>
    </object>
</body>
</html>

```

Atributos comunes de `<object>`

- **`data`**: Especifica la URL del recurso a incrustar.
- **`type`**: Define el tipo MIME del recurso.
- **`width`**: Define el ancho del objeto.
- **`height`**: Define la altura del objeto.

**Conclusión**
Las etiquetas `<iframe>`, `<embed>` y `<object>` son herramientas poderosas en HTML para incrustar contenido externo en una página web. Mientras `<iframe>` es ampliamente usado para incrustar contenido dinámico como vídeos y mapas, `<object>` ofrece un mayor control y compatibilidad para otros tipos de contenido, incluyendo archivos multimedia interactivos. Conociendo cómo y cuándo usar cada una de estas etiquetas, puedes mejorar significativamente la funcionalidad y la interactividad de tus páginas web.

## Vídeo en HTML5

---

Con HTML5, podemos mostrar vídeos directamente en nuestra web usando la etiqueta `<video>`. Esto permite reproducir contenido multimedia sin necesidad de plugins adicionales, ofreciendo una mejor integración y soporte para diferentes formatos de vídeo.

La etiqueta `<video>` permite incrustar vídeos en una página web. Se pueden especificar varios atributos para controlar la reproducción y apariencia del vídeo.

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Video</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          margin: 20px;
      }
    </style>
  </head>
  <body>
    <h1>Ejemplo de Uso de la Etiqueta Video</h1>
    <video src="./assets/thepower.mp4" autoplay controls width="600">
      Tu navegador no admite el elemento <code>video</code>.
    </video>
  </body>
</html>
```

Atributos comunes de `<video>`

- **`src`**: Especifica la URL del archivo de vídeo.
- **`autoplay`**: Reproduce el vídeo automáticamente cuando la página se carga.
- **`controls`**: Muestra los controles de reproducción (play, pause, volumen, etc.).
- **`width`**: Define el ancho del vídeo en píxeles.
- **`height`**: Define la altura del vídeo en píxeles.
- **`loop`**: Reproduce el vídeo en bucle.
- **`muted`**: Inicia el vídeo en silencio.

Diferentes formatos de vídeo son soportados por la etiqueta `<video>`, cada uno con sus ventajas y desventajas.

| FORMATO | CODEC | DESCRIPCIÓN | ¿RECOMENDADO? |
| --- | --- | --- | --- |
| MP4 | x264, DivX H264 | Alta calidad. Codec x264 libre. | Sí, buen soporte |
| WebM | VP8, VP9 | Alternativa libre a MP4 de Google. | Sí, soporte medio |
| AV1 | Basado en VP10, Daala y Thor | Compite con HEVC/H.265 | No, soporte bajo |
| HEVC | x265, DivX HEVC | Futura evolución de MP4. | No, poco soporte |
| OGV | Theora | Alternativa libre a MP4. | Con precaución |
| MKV | Matroska | Buena compresión. Potente. | No, alto consumo CPU |
| AVI | XviD, DivX 3/5 | Menor compresión que MP4. | No, anticuado |

## Ejemplos detallados de vídeo

---

Vídeo con múltiples formatos: Para asegurar la compatibilidad en diferentes navegadores, puedes proporcionar múltiples fuentes de vídeo usando la etiqueta `<source>` dentro de la etiqueta `<video>`.

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vídeo con Múltiples Formatos</title>
  </head>
  <body>
    <h1>Ejemplo de Vídeo con Múltiples Formatos</h1>
    <video controls width="600">
      <source src="./assets/video.mp4" type="video/mp4" />
      <source src="./assets/video.webm" type="video/webm" />
      <source src="./assets/video.ogv" type="video/ogg" />
      Tu navegador no soporta el elemento <code>video</code>.
    </video>
  </body>
</html>
```

Vídeo en bucle y silenciado

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vídeo en Bucle y Silenciado</title>
  </head>
  <body>
    <h1>Ejemplo de Vídeo en Bucle y Silenciado</h1>
    <video src="./assets/video.mp4" loop muted controls width="600">
      Tu navegador no soporta el elemento <code>video</code>.
    </video>
  </body>
</html>
```

**Conclusión**
La etiqueta `<video>` en HTML5 proporciona una manera efectiva de incrustar y reproducir contenido de vídeo en páginas web, soportando varios formatos y ofreciendo controles integrados para mejorar la experiencia del usuario. Conociendo los formatos de vídeo recomendados y cómo utilizarlos, puedes asegurarte de que tu contenido multimedia sea accesible y eficiente en todos los navegadores modernos.

## Audio en HTML5

---

Para insertar archivos de audio en nuestras webs, usamos la etiqueta `<audio>`. Esta etiqueta permite reproducir audio directamente en la página, ofreciendo controles integrados para la reproducción.

La etiqueta `<audio>` se utiliza para incrustar archivos de audio en una página web. Se pueden especificar varios atributos para controlar la reproducción del audio.

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Audio</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          margin: 20px;
      }
    </style>
  </head>
  <body>
    <h1>Ejemplo de Uso de la Etiqueta Audio</h1>
    <audio src="audio.mp3" preload="none" controls>
      Tu navegador no admite el elemento <code>audio</code>.
    </audio>
  </body>
</html>
```

Atributos comunes de `<audio>`

- **`src`**: Especifica la URL del archivo de audio.
- **`preload`**: Indica al navegador si debe descargar el archivo de audio cuando la página se carga (valores posibles: `none`, `metadata`, `auto`).
- **`controls`**: Muestra los controles de reproducción (play, pause, volumen, etc.).
- **`autoplay`**: Reproduce el audio automáticamente cuando la página se carga.
- **`loop`**: Reproduce el audio en bucle.
- **`muted`**: Inicia el audio en silencio.

Diferentes formatos de audio son soportados por la etiqueta `<audio>`, cada uno con sus ventajas y desventajas.

| FORMATO | CODEC | DESCRIPCIÓN | ¿RECOMENDADO? |
| --- | --- | --- | --- |
| MP3 | MPEG Layer-3 | Buena calidad. | Sí, buen soporte |
| AAC | Advanced Audio Coding | Mejora el MP3. Usado como audio en MP4. | Sí, buen soporte |
| OGG | Ogg Vorbis | Buena calidad. Alternativa libre a MP3. | Sí, soporte medio |
| Opus | Opus | Buena calidad. Alternativa libre a MP3. | Sí, soporte medio |
| FLAC | FLAC Audio Lossless | Compresión sin pérdidas. Alto tamaño. | Sí, buen soporte |
| WAV | Wave sound | Formato de Microsoft. Está soportado. | No, muy pesado |

## Ejemplos detallados audio en HTML5

---

Audio con múltiples formatos: Para asegurar la compatibilidad en diferentes navegadores, puedes proporcionar múltiples fuentes de audio usando la etiqueta `<source>` dentro de la etiqueta `<audio>`.

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Audio con Múltiples Formatos</title>
  </head>
  <body>
    <h1>Ejemplo de Audio con Múltiples Formatos</h1>
    <audio controls>
      <source src="audio.mp3" type="audio/mpeg" />
      <source src="audio.ogg" type="audio/ogg" />
      <source src="audio.flac" type="audio/flac" />
      Tu navegador no soporta el elemento <code>audio</code>.
    </audio>
  </body>
</html>
```

Audio en bucle y silenciado

```html
htmlCopiar código
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Audio en Bucle y Silenciado</title>
  </head>
  <body>
    <h1>Ejemplo de Audio en Bucle y Silenciado</h1>
    <audio src="audio.mp3" loop muted controls>
      Tu navegador no soporta el elemento <code>audio</code>.
    </audio>
  </body>
</html>
```

**Conclusión**
La etiqueta `<audio>` en HTML5 proporciona una manera efectiva de incrustar y reproducir contenido de audio en páginas web, soportando varios formatos y ofreciendo controles integrados para mejorar la experiencia del usuario. Conociendo los formatos de audio recomendados y cómo utilizarlos, puedes asegurarte de que tu contenido multimedia sea accesible y eficiente en todos los navegadores modernos.

## Subtítulos en vídeos HTML5

---

Los subtítulos son una característica importante para mejorar la accesibilidad y la comprensión de los vídeos en la web. La etiqueta `<track>` se utiliza para añadir subtítulos, descripciones, capítulos y metadatos a los vídeos.

La etiqueta `<track>` se usa dentro de la etiqueta `<video>` para proporcionar diferentes tipos de texto sincronizado con el vídeo.

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Subtítulos en Vídeo</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          margin: 20px;
      }
      video {
          max-width: 100%;
          height: auto;
      }
    </style>
  </head>
  <body>
    <h1>Ejemplo de Subtítulos en Vídeo</h1>
    <video controls src="thepower.mp4" autoplay width="600">
      <track default kind="captions" srclang="es" src="subtitulos.vtt" />
      Sorry, your browser doesn't support embedded videos.
    </video>
  </body>
</html>
```

Atributos comunes de `<track>`

- **`default`**: Especifica que esta pista debe ser la predeterminada.
- **`kind`**: Define el tipo de pista. Los valores posibles son:
    - `subtitles`: Subtítulos traducidos.
    - `captions`: Subtítulos en el mismo idioma del vídeo, usualmente para sordos y personas con problemas de audición.
    - `descriptions`: Descripciones auditivas del contenido del vídeo.
    - `chapters`: Marcadores de capítulos dentro del vídeo.
    - `metadata`: Información adicional sobre el contenido.
- **`srclang`**: Especifica el lenguaje de la pista de texto (ej. "es" para español).
- **`src`**: Especifica la URL del archivo de la pista.

## Formato WebVTT

---

WebVTT (Web Video Text Tracks) es un formato de archivo de texto usado para subtítulos, capítulos y metadatos. A continuación se muestra un ejemplo de un archivo WebVTT (`subtitulos.vtt`):

```lua
WEBVTT

00:03.000 --> 00:05.000
<v Alberto>
El fullstack development o desarrollo web es el arte de construir aplicaciones
```

Detalles del Formato WebVTT

1. **Encabezado**: `WEBVTT` para indicar el formato.
2. **Tiempos**: Indican el inicio y fin del texto que se mostrará, en el formato `HH:MM:SS.MMM`.
3. **Texto**: El texto del subtítulo, puede incluir nombres de hablantes.

## Ejemplos detallados subtítulos en vídeos HTML5

---

Subtítulos en Inglés y Español

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vídeo con Subtítulos en Inglés y Español</title>
  </head>
  <body>
    <h1>Vídeo con Subtítulos en Inglés y Español</h1>
    <video controls width="600">
      <source src="thepower.mp4" type="video/mp4" />
      <track
        kind="subtitles"
        srclang="es"
        src="subtitulos_es.vtt"
        label="Español"
        default
      />
      <track
        kind="subtitles"
        srclang="en"
        src="subtitulos_en.vtt"
        label="English"
      />
      Sorry, your browser doesn't support embedded videos.
    </video>
  </body>
</html>
```

Ejemplo de archivos WebVTT `subtitulos_es.vtt`

```lua
WEBVTT

00:03.000 --> 00:05.000
<v Alberto>
El fullstack development o desarrollo web es el arte de construir aplicaciones
```

`subtitulos_en.vtt`

```csharp
WEBVTT

00:03.000 --> 00:05.000
<v Alberto>
Fullstack development is the art of building applications
```

**Conclusión**
La etiqueta `<track>` junto con el formato WebVTT proporciona una manera efectiva de añadir subtítulos y otros tipos de texto sincronizado a los vídeos en HTML5. Esto mejora la accesibilidad y permite a los usuarios disfrutar del contenido multimedia de manera más completa. Usando subtítulos en diferentes idiomas, puedes hacer que tu contenido sea accesible a una audiencia global.

## Reto Coding

---

Practicar la inserción de imágenes, vídeos, audios e iframes en un documento HTML.

### Instrucciones:

1. **Crea un documento HTML** que contenga:
    - Una imagen con texto alternativo y dimensiones definidas mediante CSS.
    - Un vídeo con controles, subtítulos y reproducido automáticamente.
    - Un audio con controles y reproducido automáticamente.
    - Un iframe que incruste un vídeo de YouTube.
2. **Aplica estilos** usando CSS para mejorar la presentación del contenido audiovisual.
    
    ```html
        <style>
            .imagen {
                width: 300px;
                height: auto;
                display: block;
                margin: 10px 0;
            }
            .video, .audio {
                display: block;
                margin: 20px 0;
                width: 100%;
                max-width: 600px;
            }
            iframe {
                width: 100%;
                height: 315px;
            }
        </style>
    ```
    

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Contenido Audiovisual</title>
    <style>
      .imagen {
          width: 300px;
          height: auto;
          display: block;
          margin: 10px 0;
      }
      .video, .audio {
          display: block;
          margin: 20px 0;
          width: 100%;
          max-width: 600px;
      }
      iframe {
          width: 100%;
          height: 315px;
      }
    </style>
  </head>
  <body>
    <h1>Ejemplos de Contenido Audiovisual</h1>

    <!-- Imagen -->
    <h2>Imagen</h2>
    <img
      src="https://via.placeholder.com/300"
      alt="Ejemplo de imagen"
      class="imagen"
    />

    <!-- Video -->
    <h2>Video</h2>
    <video
      src="https://www.w3schools.com/html/mov_bbb.mp4"
      autoplay
      controls
      width="600"
      class="video"
    >
      <track default kind="captions" srclang="es" src="subtitulos.vtt" />
      Tu navegador no admite el elemento <code>video</code>.
    </video>

    <!-- Audio -->
    <h2>Audio</h2>
    <audio
      src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3"
      autoplay
      controls
      class="audio"
    >
      Tu navegador no admite el elemento <code>audio</code>.
    </audio>

    <!-- Iframe -->
    <h2>Iframe (Video de YouTube)</h2>
    <iframe
      src="https://www.youtube.com/embed/dQw4w9WgXcQ"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    ></iframe>
  </body>
</html>
```

### Explicación del **Reto Coding**

**Imagen**: Se utiliza la etiqueta `<img>` con los atributos `src` y `alt`. El tamaño de la imagen se controla mediante CSS.

```html
<img src="https://via.placeholder.com/300" alt="Ejemplo de imagen" class="imagen">
```

**Video**: La etiqueta `<video>` se utiliza para insertar un vídeo, con los atributos `autoplay` y `controls`. Se añade una pista de subtítulos con `<track>`.

```html
<video src="https://www.w3schools.com/html/mov_bbb.mp4" autoplay controls width="600" class="video">
    <track default kind="captions" srclang="es" src="subtitulos.vtt" />
    Tu navegador no admite el elemento <code>video</code>.
</video>
```

**Audio**: La etiqueta `<audio>` se utiliza para insertar un archivo de audio con los atributos `autoplay` y `controls`.

```html
<audio src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" autoplay controls class="audio">
    Tu navegador no admite el elemento <code>audio</code>.
</audio>
```

**Iframe**: La etiqueta `<iframe>` se utiliza para incrustar un vídeo de YouTube.

```html
<iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```
## Contenido asociado
---
- [Video: Imagenes](https://vimeo.com/846212713/bb2cd5a236)
- [Video: Video, audio & iframe](https://vimeo.com/846215402/595b84ee9b)
