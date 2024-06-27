<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Etiquetas hipervínculo o navegables

La etiqueta `<a>` es fundamental en HTML para crear enlaces o hipervínculos. Los enlaces permiten a los usuarios navegar entre diferentes páginas web o recursos.

## Atributos comunes de `<a>`

---

| Atributo | Valores | Descripción |
| --- | --- | --- |
| href | URL | Dirección del enlace. |
| download | nombre.ext | Descarga el enlace en lugar de abrirlo. |
| target | _blank, _self, _parent, _top | Define dónde abrir el enlace. |
| hreflang | Código ISO 639-1 | Idioma del documento enlazado. |
| rel | alternate, author, bookmark, help, license, prev, next, nofollow, noreferrer, prefetch, search, tag | Define la relación entre el documento actual y el enlazado. |

## Ejemplo de Uso de `<a>`

---

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Hipervínculos</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          margin: 20px;
      }
      .section {
          margin-bottom: 20px;
      }
    </style>
  </head>
  <body>
    <h1>Ejemplos de Hipervínculos</h1>

    <div class="section">
      <h2>Enlaces Externos</h2>
      <p><a href="https://www.google.com">Ir a la página web de Google</a></p>
      <ul>
        <li>
          <a rel="author" target="_self" href="http://www.mipagina.com/"
            >mipagina</a
          >
        </li>
        <li><a href="http://mipagina/" target="_blank">mipagina</a></li>
        <li><a href="http://cv.pdf" download="A-38.pdf">Descargar PDF</a></li>
        <li><a href="http://documento.pdf" hreflang="en">PDF en inglés</a></li>
      </ul>
    </div>

    <div class="section">
      <h2>Enlaces Internos</h2>
      <p><a href="#section1">Ir a la Sección 1</a></p>
      <p><a href="#section2">Ir a la Sección 2</a></p>
    </div>

    <div class="section" id="section1">
      <h2>Sección 1</h2>
      <p>Contenido de la Sección 1...</p>
      <p><a href="#top">Volver al Inicio</a></p>
    </div>

    <div class="section" id="section2">
      <h2>Sección 2</h2>
      <p>Contenido de la Sección 2...</p>
      <p><a href="#top">Volver al Inicio</a></p>
    </div>
  </body>
</html>
```

**Enlaces externos**: [**Ir a Google]** Este enlace lleva al usuario a la página de Google.

```html
<p><a href="https://www.google.com">Ir a la página web de Google</a></p>
```

**Relación y objetivo**

```html
<ul>
  <li>
    <a rel="author" target="_self" href="http://www.mipagina.com/">mipagina</a>
  </li>
  <li><a href="http://mipagina/" target="_blank">mipagina</a></li>
  <li><a href="http://cv.pdf" download="A-38.pdf">Descargar PDF</a></li>
  <li><a href="http://documento.pdf" hreflang="en">PDF en inglés</a></li>
</ul>
```

- El primer enlace tiene el atributo `rel="author"` indicando que es la página del autor, y `target="_self"` que abre el enlace en la misma pestaña.
- El segundo enlace usa `target="_blank"` para abrir el enlace en una nueva pestaña.
- El tercer enlace utiliza `download` para descargar el archivo en lugar de abrirlo.
- El cuarto enlace usa `hreflang="en"` para indicar que el documento enlazado está en inglés.

**Enlaces Internos**

```html
<p><a href="#section1">Ir a la Sección 1</a></p>
<p><a href="#section2">Ir a la Sección 2</a></p>
```

**Ir a Sección 1 y Sección 2**: Estos enlaces permiten la navegación interna dentro de la misma página, desplazándose a las secciones especificadas por los IDs `section1` y `section2`.

```html
<p><a href="#top">Volver al Inicio</a></p>
```

**Volver al Inicio**: Este enlace permite volver al inicio de la página.

## Esquema de URL

---

Una URL completa se compone de varias partes que se describen a continuación.

```
https://blog.minegocioonline.com/categoria/contenido
```

| Parte | Descripción |
| --- | --- |
| https:// | Protocolo de transferencia de hipertexto seguro. |
| blog | Subdominio. |
| minegocioonline | Dominio. |
| .com | TLD (dominio de nivel superior). |
| /categoria | Subcarpeta. |
| /contenido | Página o archivo. |

## Enlace con `target="_blank"` y `rel="noopener noreferrer"`

---

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Visitar Example</a>
```

`target="_blank"` abre el enlace en una nueva pestaña.

`rel="noopener noreferrer"` mejora la seguridad previniendo que la página enlazada pueda acceder al objeto `window.opener`.

## Enlace de descarga

---

```html
<a href="/downloads/ebook.pdf" download="ebook.pdf">Descargar eBook</a>
```

`download="ebook.pdf"` hace que el enlace descargue el archivo `ebook.pdf` en lugar de abrirlo.

## Enlace con `hreflang`

---

```html
<a href="https://example.com/en" hreflang="en">English Version</a>
```

`hreflang="en"` indica que el contenido enlazado está en inglés.

## Enlace con descripción de relación

---

```html
<a href="https://authorwebsite.com" rel="author">Autor del Sitio</a>
```

`rel="author"` describe que el enlace es hacia la página del autor del documento actual.

## Enlace interno

---

```html
<a href="#section3">Ir a la Sección 3</a>
```

`href="#section3"` navega dentro de la misma página a un elemento con el `id="section3"`.

## Reto Coding

---

Practicar el uso de la etiqueta `<a>` para crear enlaces tanto internos como externos y comprender la estructura de una URL.

### Instrucciones:

1. **Crea un documento HTML** que contenga varios enlaces, tanto a recursos externos como internos en la misma página.
2. **Usa diferentes atributos** como `target`, `download`, `hreflang`, y `rel` para demostrar sus usos.
3. Usa el CSS asociado para mejorar la presentación.

```html
  <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .section {
            margin-bottom: 20px;
        }
    </style>
```

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Hipervínculos</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .section {
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <h1>Ejemplos de Hipervínculos</h1>

    <div class="section">
        <h2>Enlaces Externos</h2>
        <p><a href="https://www.google.com" target="_blank">Ir a Google</a></p>
        <p><a href="https://www.wikipedia.org" hreflang="en" target="_blank" rel="noreferrer">Ir a Wikipedia en Inglés</a></p>
        <p><a href="https://www.example.com/document.pdf" download="documento.pdf">Descargar PDF</a></p>
    </div>

    <div class="section">
        <h2>Enlaces Internos</h2>
        <p><a href="#section1">Ir a la Sección 1</a></p>
        <p><a href="#section2">Ir a la Sección 2</a></p>
    </div>

    <div class="section" id="section1">
        <h2>Sección 1</h2>
        <p>Contenido de la Sección 1...</p>
        <p><a href="#top">Volver al Inicio</a></p>
    </div>

    <div class="section" id="section2">
        <h2>Sección 2</h2>
        <p>Contenido de la Sección 2...</p>
        <p><a href="#top">Volver al Inicio</a></p>
    </div>
</body>
</html>
```

## Contenido asociado
---
- [Video: Etiquetas hipervinculos](https://vimeo.com/846205968/2bff559bab)
