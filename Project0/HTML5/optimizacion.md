<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Optimización del rendimiento de un documento HTML

Optimizar el rendimiento de un documento HTML es crucial para mejorar la experiencia del usuario y reducir los tiempos de carga. A continuación, se presentan algunas recomendaciones y técnicas que puedes aplicar para lograrlo.

## **Comprimir los archivos**

---

Comprimir los archivos HTML, CSS y JavaScript puede reducir significativamente su tamaño y mejorar los tiempos de carga.

- **Minificar archivos**: Utiliza herramientas en línea como [Minifier](https://www.minifier.org/) para eliminar espacios en blanco y comentarios innecesarios.
- **GZip**: Herramientas como [GZip](https://gzip.org/) comprimen los archivos en un formato más pequeño y eficiente.

## **Optimizar las imágenes**

---

Las imágenes a menudo representan la mayor parte del tamaño de una página web. Optimizarlas puede mejorar considerablemente el rendimiento.

- **Herramientas de compresión**: Utiliza herramientas como [TinyPNG](https://tinypng.com/) o [JPEG Optimizer](https://jpeg-optimizer.com/) para reducir el tamaño de las imágenes sin comprometer la calidad.
- **Formato adecuado**: Usa el formato de archivo correcto para cada tipo de imagen (por ejemplo, PNG para imágenes con transparencia y JPEG para fotografías).

## **Utilizar CDN (Content Delivery Network)**

---

Un CDN distribuye el contenido de tu sitio web en múltiples servidores alrededor del mundo, mejorando la velocidad de carga para los usuarios sin importar su ubicación.

- **Servicios populares**: Algunos servicios CDN populares incluyen [Cloudflare](https://www.cloudflare.com/) y [Amazon CloudFront](https://aws.amazon.com/cloudfront/).

Para integrar un CDN en tu sitio web, contrata un servicio de CDN y configura tu sitio web para usarlo.

## **Minimizar el uso de scripts externos**

---

Reducir el uso de scripts externos puede disminuir el tiempo de carga de tu página web.

- **Uso necesario**: Utiliza solo los scripts absolutamente necesarios.
- **Carga asíncrona**: Asegúrate de que los scripts se carguen de forma asíncrona para no bloquear la carga de la página.

## **Usar la caché del navegador**

---

Configurar la caché del navegador permite que los usuarios carguen la página más rápidamente en visitas posteriores.

- **Configuración de la caché**: Configura las cabeceras HTTP de tus archivos para indicar cuánto tiempo deben mantenerse en la caché. Aquí tienes un ejemplo de cómo agregar la cabecera `Cache-Control`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mi página web</title>
    <meta http-equiv="Cache-Control" content="max-age=604800">
</head>
<body>
    <h1>Bienvenido a mi página web</h1>
</body>
</html>
```

```css
/* archivo estilo.css */
body {
    background-color: #f1f1f1;
    color: #333;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

/* Se recomienda establecer un valor alto para la caché en producción */
```

```jsx
// archivo script.js
console.log("Hola, mundo!");

// Se recomienda establecer un valor alto para la caché en producción
```

## **Evitar redireccionamientos innecesarios**

---

Los redireccionamientos innecesarios pueden aumentar los tiempos de carga.

- **Estructura adecuada**: Planifica la estructura de tu sitio web para minimizar redireccionamientos.
- **Redireccionamientos permanentes**: Usa redireccionamientos 301 en lugar de 302, ya que los primeros son permanentes y más eficientes.

## **Reducir el número de solicitudes HTTP**

---

Reducir el número de solicitudes HTTP puede mejorar el rendimiento de la página.

- **Combinar archivos**: Combina varios archivos CSS y JavaScript en uno solo.
- **Carga diferida**: Utiliza técnicas como la carga diferida de imágenes y otros elementos no críticos.

## **Utilizar etiquetas de carga diferida**

---

Las etiquetas de carga diferida retrasan la carga de imágenes y otros elementos no críticos hasta que el usuario los necesite.

- **Imágenes y iframes**: Usa las etiquetas `<img loading="lazy">` y `<iframe loading="lazy">` para mejorar el rendimiento.

```html
<img src="imagen.jpg" loading="lazy" alt="Descripción de la imagen">
<iframe src="https://example.com" loading="lazy"></iframe>
```

## Reto Coding

---

El objetivo de este ejercicio es aplicar las técnicas de optimización aprendidas para mejorar el rendimiento de un documento HTML. A través de este ejercicio, aprenderás a comprimir archivos, optimizar imágenes, utilizar la caché del navegador, minimizar el uso de scripts externos y utilizar etiquetas de carga diferida.

### Instrucciones:

1. **Comprimir archivos HTML, CSS y JavaScript**
    - Utiliza [Minifier](https://www.minifier.org/) para comprimir los siguientes archivos:
        
        **index.html**
        
        ```html
        <!DOCTYPE html>
        <html>
        <head>
            <title>Mi Página Web</title>
            <link rel="stylesheet" type="text/css" href="styles.css">
            <script src="script.js" defer></script>
        </head>
        <body>
            <h1>Bienvenido a mi página web</h1>
            <img src="image.png" alt="Descripción de la imagen">
        </body>
        </html>
        ```
        
        **styles.css**
        
        ```css
        body {
            background-color: #f1f1f1;
            color: #333;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        ```
        
        **script.js**
        
        ```jsx
        console.log("Hola, mundo!");
        ```
        
    - Comprime estos archivos utilizando Minifier y reemplaza el contenido de los archivos originales con los archivos minificados.
2. **Optimizar imágenes**
    - Utiliza [TinyPNG](https://tinypng.com/) o [JPEG Optimizer](https://jpeg-optimizer.com/) para optimizar la imagen `image.png`.
    - Reemplaza la imagen original con la versión optimizada.
3. **Usar la caché del navegador**
    - Agrega la cabecera `Cache-Control` en los archivos HTML, CSS y JavaScript para que se almacenen en la caché del navegador. Establece el tiempo de caché a una semana (604800 segundos).
        
        **index.html**
        
        ```html
        <!DOCTYPE html>
        <html>
        <head>
            <title>Mi Página Web</title>
            <meta http-equiv="Cache-Control" content="max-age=604800">
            <link rel="stylesheet" type="text/css" href="styles.css?v=1">
            <script src="script.js?v=1" defer></script>
        </head>
        <body>
            <h1>Bienvenido a mi página web</h1>
            <img src="image.png" alt="Descripción de la imagen">
        </body>
        </html>
        ```
        
        **styles.css**
        
        ```css
        /* archivo estilos.css */
        body {
            background-color: #f1f1f1;
            color: #333;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        ```
        
        **script.js**
        
        ```jsx
        console.log("Hola, mundo!");
        ```
        
4. **Minimizar el uso de scripts externos**
    - Asegúrate de que todos los scripts se carguen de forma asíncrona o con el atributo `defer` para no bloquear la carga de la página.
5. **Utilizar etiquetas de carga Diferida**
    - Agrega el atributo `loading="lazy"` a la etiqueta `<img>` para cargar la imagen de forma diferida.
        
        **index.html**
        
        ```html
        <!DOCTYPE html>
        <html>
        <head>
            <title>Mi Página Web</title>
            <meta http-equiv="Cache-Control" content="max-age=604800">
            <link rel="stylesheet" type="text/css" href="styles.css?v=1">
            <script src="script.js?v=1" defer></script>
        </head>
        <body>
            <h1>Bienvenido a mi página web</h1>
            <img src="image.png" alt="Descripción de la imagen" loading="lazy">
        </body>
        </html>
        ```
        

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mi Página Web</title>
    <meta http-equiv="Cache-Control" content="max-age=604800">
    <link rel="stylesheet" type="text/css" href="styles.css?v=1">
    <script src="script.js?v=1" defer></script>
</head>
<body>
    <h1>Bienvenido a mi página web</h1>
    <img src="image.png" alt="Descripción de la imagen" loading="lazy">
</body>
</html>
```

```css
body{background-color:#f1f1f1;color:#333;font-family:Arial,sans-serif;margin:0;padding:0}
```

```jsx
console.log("Hola, mundo!");
```