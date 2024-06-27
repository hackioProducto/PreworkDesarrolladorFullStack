<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Etiquetas de agrupación

Las etiquetas de agrupación en HTML se utilizan para contener y organizar el contenido en bloques lógicos. Estas etiquetas son fundamentales para estructurar adecuadamente una página web.

## Etiqueta `<p>`

---

La etiqueta `<p>` se utiliza para contener párrafos de texto. Es una de las etiquetas más básicas y comunes en HTML.

```html
<article>
   <h1>¡Hola a todos!</h1>
   <p>Soy un párrafo</p>
   <p>Soy un párrafo en otra línea</p>
</article>
```

## Etiqueta `<div>`

---

La etiqueta `<div>` es ampliamente utilizada para agrupar bloques de contenido. Es una etiqueta de contenedor que no tiene un significado específico por sí sola, pero se usa para aplicar estilos o scripts a grupos de elementos.

```html
<div>
    <h2>Steve Rogers</h2>
    <p>Soldier</p>
    <p>Tel: 658 22 77 66</p>
</div>
<div>
    <h2>Bruce Banner</h2>
    <p>Scientist</p>
    <p>Tel: 658 22 77 66</p>
</div>
```

## Etiqueta `<ul>`

---

Para listas desordenadas, usamos la etiqueta `<ul>` (unordered list) con elementos `<li>` (list item).

```html
<ul>
    <li>Elemento Uno</li>
    <li>Elemento Dos</li>
    <li>Elemento Tres</li>
</ul>
```

## Etiqueta `<ol>`

---

Para listas ordenadas, usamos la etiqueta `<ol>` (ordered list) con elementos `<li>`.

```html
<ol>
    <li>Elemento Uno</li>
    <li>Elemento Dos</li>
    <li>Elemento Tres</li>
</ol>
```

## Etiqueta `<blockquote>`

---

Para citas literarias o citas largas, usamos la etiqueta `<blockquote>`. Esta etiqueta se utiliza para delimitar bloques de contenido que son citas de otra fuente.

```html
<blockquote cite="https://www.sensacine.com/noticias/cine/noticia-18592299/">
  <p>Yo soy IronMan</p>
  <footer>
    <cite class="author">Tony Stark</cite> en
    <cite class="title">Avengers End Game</cite>
  </footer>
</blockquote>
```

## Etiqueta `<figure>`

---

Para agrupar imágenes y sus pies de foto, usamos `<figure>` y `<figcaption>`. Esta combinación se utiliza para asociar una imagen con su pie de foto o descripción.

```html
<figure>
    <img src="ruta-imagen" alt="texto-alternativo"/>
    <figcaption>Escuela de Desarrollo Web</figcaption>
</figure>
```

## Etiqueta `<dl>`

---

Para listas de descripciones, usamos `<dl>` (description list), `<dt>` (description term) y `<dd>` (description definition). Esta estructura se utiliza comúnmente para términos y sus definiciones.

```html
<dl>
  <dt>Gallina</dt>
  <dd>Animal de granja</dd>
  <dd>Persona que carece de valor</dd>
</dl>
```

## Reto Coding

---

Practicar el uso de etiquetas de agrupación para organizar y estructurar contenido en una página HTML.

### Instrucciones:

1. **Crea un documento HTML** que contenga ejemplos de todas las etiquetas de agrupación mencionadas.
2. **Estructura el contenido** de manera lógica y semánticamente correcta.
3. **Asocia estilos CSS básicos** para mejorar la presentación visual de los elementos.
    
    ```html
        <style>
            body {
                font-family: Arial, sans-serif;
                margin: 20px;
            }
            .container {
                border: 1px solid #ccc;
                padding: 20px;
                margin-bottom: 20px;
            }
            blockquote {
                border-left: 5px solid #ccc;
                padding-left: 10px;
                margin-left: 0;
            }
            figure {
                margin: 0;
            }
            figcaption {
                text-align: center;
                font-size: 0.9em;
                color: #555;
            }
            dl {
                margin: 20px 0;
            }
            dt {
                font-weight: bold;
            }
            dd {
                margin-left: 20px;
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
    <title>Ejemplo de Etiquetas de Agrupación</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .container {
            border: 1px solid #ccc;
            padding: 20px;
            margin-bottom: 20px;
        }
        blockquote {
            border-left: 5px solid #ccc;
            padding-left: 10px;
            margin-left: 0;
        }
        figure {
            margin: 0;
        }
        figcaption {
            text-align: center;
            font-size: 0.9em;
            color: #555;
        }
        dl {
            margin: 20px 0;
        }
        dt {
            font-weight: bold;
        }
        dd {
            margin-left: 20px;
        }
    </style>
</head>
<body>
    <article>
        <h1>¡Hola a todos!</h1>
        <p>Soy un párrafo</p>
        <p>Soy un párrafo en otra línea</p>
    </article>

    <div class="container">
        <h2>Steve Rogers</h2>
        <p>Soldier</p>
        <p>Tel: 658 22 77 66</p>
    </div>
    <div class="container">
        <h2>Bruce Banner</h2>
        <p>Scientist</p>
        <p>Tel: 658 22 77 66</p>
    </div>

    <ul>
        <li>Elemento Uno</li>
        <li>Elemento Dos</li>
        <li>Elemento Tres</li>
    </ul>

    <ol>
        <li>Elemento Uno</li>
        <li>Elemento Dos</li>
        <li>Elemento Tres</li>
    </ol>

    <blockquote cite="https://www.sensacine.com/noticias/cine/noticia-18592299/">
        <p>Yo soy IronMan</p>
        <footer>
            <cite class="author">Tony Stark</cite> en
            <cite class="title">Avengers End Game</cite>
        </footer>
    </blockquote>

    <figure>
        <img src="ruta-imagen" alt="Texto alternativo" width="300"/>
        <figcaption>Escuela de Desarrollo Web</figcaption>
    </figure>

    <dl>
        <dt>Gallina</dt>
        <dd>Animal de granja</dd>
        <dd>Persona que carece de valor</dd>
    </dl>
</body>
</html>

```

## Contenido asociado
---
- [Video: Etiquetas de agrupación](https://vimeo.com/846180941/ff9e20e07a)
