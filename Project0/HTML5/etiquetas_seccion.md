<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Etiquetas de sección | Estructura semántica

HTML5 introdujo varias etiquetas de sección que mejoran la semántica del contenido, permitiendo una estructura más clara y accesible para los usuarios y motores de búsqueda.

### Ejemplo de estructura semántica

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Estructura Semántica</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        header, main, aside, footer {
            margin-bottom: 20px;
            padding: 10px;
            border: 1px solid #ccc;
        }
    </style>
</head>
<body>
    <header>
        <h1>Título del Sitio</h1>
        <nav>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#sobre-nosotros">Sobre Nosotros</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article>
            <h2>Título del Artículo</h2>
            <p>Contenido del artículo...</p>
        </article>

        <aside>
            <h2>Información Complementaria</h2>
            <p>Contenido del aside...</p>
        </aside>
    </main>

    <footer>
        <p>&copy; 2023 Mi Sitio Web. Todos los derechos reservados.</p>
    </footer>
</body>
</html>
```

## `<header>`

---

El elemento `<header>` se utiliza para contener información introductoria o de navegación. Generalmente incluye:

- Logotipo del sitio.
- Encabezados.
- Enlaces de navegación.

```html
<header>
    <h1>Título del Sitio</h1>
    <nav>
        <ul>
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#sobre-nosotros">Sobre Nosotros</a></li>
            <li><a href="#contacto">Contacto</a></li>
        </ul>
    </nav>
</header>
```

## `<nav>`

---

El elemento `<nav>` contiene el bloque principal de enlaces de navegación. Puede incluir enlaces a las diferentes secciones del sitio web.

```html
<nav>
    <ul>
        <li><a href="#inicio">Inicio</a></li>
        <li><a href="#sobre-nosotros">Sobre Nosotros</a></li>
        <li><a href="#contacto">Contacto</a></li>
    </ul>
</nav>
```

## `<main>`

---

El elemento `<main>` contiene el contenido principal del documento. Solo debe haber un `<main>` por documento, y no debe estar anidado dentro de otros elementos de contenido como `<article>`, `<aside>`, `<footer>`, `<header>`, o `<nav>`.

```html
<main>
    <article>
        <h2>Título del Artículo</h2>
        <p>Contenido del artículo...</p>
    </article>

    <aside>
        <h2>Información Complementaria</h2>
        <p>Contenido del aside...</p>
    </aside>
</main>
```

## `<article>`

---

El elemento `<article>` se utiliza para contener contenido independiente, que podría ser distribuido por sí solo. Es ideal para artículos de blog, publicaciones de redes sociales, noticias, etc.

```html
<article>
    <h3>Título del Artículo</h3>
    <p>Contenido del artículo...</p>
</article>
```

## `<aside>`

---

El elemento `<aside>` contiene información complementaria que está relacionada indirectamente con el contenido principal. Esto puede incluir biografías de autores, listas de enlaces relacionados, anuncios, etc.

```html
<aside>
    <h2>Información Complementaria</h2>
    <p>Contenido del aside...</p>
</aside>
```

## `<footer>`

---

El elemento `<footer>` se utiliza para contener información de autoría, enlaces de pie de página, derechos de autor, y otros contenidos que generalmente se encuentran al final de la página o sección.

```html
<footer>
    <p>&copy; 2023 Mi Sitio Web. Todos los derechos reservados.</p>
</footer>
```

<aside>
<img src="/icons/directions_gray.svg" alt="/icons/directions_gray.svg" width="40px" /> **Conclusión**
Las etiquetas de sección en HTML5, como `<header>`, `<nav>`, `<main>`, `<article>`, `<aside>`, y `<footer>`, mejoran la semántica del contenido y facilitan una estructura más clara y accesible. Usarlas correctamente ayuda a los usuarios y motores de búsqueda a entender mejor la organización del contenido de la página.

</aside>

## Ejemplos detallados

---

Arquitectura de la información **`<nav>`**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Nav</title>
  <style>
    nav {
      border-bottom: 1px solid black;
    }
    .crumbs ol {
      list-style-type: none;
      padding-left: 0;
    }
    .crumb {
      display: inline-block;
    }
    .crumb a::after {
      display: inline-block;
      color: #000;
      content: ">";
      font-size: 80%;
      font-weight: bold;
      padding: 0 3px;
    }
  </style>
</head>
<body>
  <nav class="crumbs">
    <ol>
      <li class="crumb"><a href="#">Bikes</a></li>
      <li class="crumb"><a href="#">BMX</a></li>
      <li class="crumb">Jump Bike 3000</li>
    </ol>
  </nav>
  <h1>Jump Bike 3000</h1>
  <p>This BMX bike is a solid step into the pro world. It looks as legit as it rides and is built to polish your skills.</p>
</body>
</html>
```

Arquitectura de la información **`<aside>` :**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Aside</title>
  <style>
    aside {
      width: 40%;
      padding-left: 0.5rem;
      margin-left: 0.5rem;
      float: right;
      box-shadow: inset 5px 0 5px -5px #29627e;
      font-style: italic;
      color: #29627e;
    }
    aside > p {
      margin: 0.5rem;
    }
    p {
      font-family: "Fira Sans", sans-serif;
    }
  </style>
</head>
<body>
  <p>Salamanders are a group of amphibians with a lizard-like appearance, including short legs and a tail in both larval and adult forms.</p>
  <aside>
    <p>The Rough-skinned Newt defends itself with a deadly neurotoxin.</p>
  </aside>
  <p>Several species of salamander inhabit the temperate rainforest of the Pacific Northwest, including the Ensatina, the Northwestern Salamander and the Rough-skinned Newt. Most salamanders are nocturnal, and hunt for insects, worms and other small creatures.</p>
</body>
</html>
```

Arquitectura de la información `<**article**>` :

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Article</title>
  <style>
    .forecast {
      margin: 0;
      padding: 0.3rem;
      background-color: #eee;
      font: 1rem "Fira Sans", sans-serif;
    }
    .forecast > h1, .day-forecast {
      margin: 0.5rem;
      padding: 0.3rem;
      font-size: 1.2rem;
    }
    .day-forecast {
      background: right/contain content-box border-box no-repeat url("rain.svg") white;
    }
    .day-forecast > h2, .day-forecast > p {
      margin: 0.2rem;
      font-size: 1rem;
    }
  </style>
</head>
<body>
  <article class="forecast">
    <h1>Weather forecast for Seattle</h1>
    <article class="day-forecast">
      <h2>03 March 2018</h2>
      <p>Rain.</p>
    </article>
    <article class="day-forecast">
      <h2>04 March 2018</h2>
      <p>Periods of rain.</p>
    </article>
    <article class="day-forecast">
      <h2>05 March 2018</h2>
      <p>Heavy rain.</p>
    </article>
  </article>
</body>
</html>

```

Arquitectura de la información `<**footer**>` :

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Footer</title>
  <style>
    article {
      min-height: 100%;
      display: grid;
      grid-template-rows: auto 1fr auto;
    }
    footer {
      display: flex;
      justify-content: center;
      padding: 5px;
      background-color: #45a1ff;
      color: #fff;
    }
  </style>
</head>
<body>
  <article>
    <h1>How to be a wizard</h1>
    <ol>
      <li>Grow a long, majestic beard.</li>
      <li>Wear a tall, pointed hat.</li>
      <li>Have I mentioned the beard?</li>
    </ol>
    <footer>
      <p>© 2018 Gandalf</p>
    </footer>
  </article>
</body>
</html>
```

Arquitectura de la información de un **Blog Personal**:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blog Personal</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        header, main, aside, footer {
            margin-bottom: 20px;
            padding: 10px;
            border: 1px solid #ccc;
        }
    </style>
</head>
<body>
    <header>
        <h1>Mi Blog Personal</h1>
        <nav>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#sobre-mi">Sobre Mí</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article>
            <h2>Título del Artículo</h2>
            <p>Este es el contenido de mi artículo...</p>
        </article>

        <aside>
            <h2>Sobre el Autor</h2>
            <p>Esta es una breve biografía del autor...</p>
        </aside>
    </main>

    <footer>
        <p>&copy; 2023 Mi Blog Personal. Todos los derechos reservados.</p>
    </footer>
</body>
</html>
```

Arquitectura de la información de un **Página Corporativa:**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página Corporativa</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        header, main, aside, footer {
            margin-bottom: 20px;
            padding: 10px;
            border: 1px solid #ccc;
        }
    </style>
</head>
<body>
    <header>
        <h1>Empresa XYZ</h1>
        <nav>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#servicios">Servicios</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article>
            <h2>Nuestros Servicios</h2>
            <p>Descripción de los servicios ofrecidos por la empresa...</p>
        </article>

        <aside>
            <h2>Noticias Recientes</h2>
            <p>Últimas noticias y actualizaciones de la empresa...</p>
        </aside>
    </main>

    <footer>
        <p>&copy; 2023 Empresa XYZ. Todos los derechos reservados.</p>
    </footer>
</body>
</html>
```

## Reto Coding

---

Practicar el uso de las etiquetas de sección para estructurar una página web semánticamente correcta.

### Instrucciones:

1. **Crea un documento HTML** que incluya todas las etiquetas de sección vistas (`<header>`, `<nav>`, `<aside>`, `<article>`, `<footer>`).
2. **Estructura el contenido** de manera lógica y semánticamente correcta, utilizando las etiquetas adecuadas para cada sección.
3. **Aplica estilos CSS básicos** para mejorar la presentación visual de los elementos.
    
    ```html
    <style>
            body {
                font-family: Arial, sans-serif;
                margin: 0;
                padding: 0;
            }
            header, footer {
                background-color: #f4f4f4;
                padding: 20px;
                text-align: center;
            }
            nav {
                background-color: #333;
                color: white;
                padding: 10px;
                text-align: center;
            }
            nav a {
                color: white;
                margin: 0 10px;
                text-decoration: none;
            }
            main {
                padding: 20px;
                display: flex;
                flex-direction: row;
            }
            article {
                flex: 3;
                margin-right: 20px;
            }
            aside {
                flex: 1;
                background-color: #f9f9f9;
                padding: 20px;
            }
            footer {
                margin-top: 20px;
            }
    ```
    

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo Completo de Etiquetas de Sección</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header, footer {
            background-color: #f4f4f4;
            padding: 20px;
            text-align: center;
        }
        nav {
            background-color: #333;
            color: white;
            padding: 10px;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 10px;
            text-decoration: none;
        }
        main {
            padding: 20px;
            display: flex;
            flex-direction: row;
        }
        article {
            flex: 3;
            margin-right: 20px;
        }
        aside {
            flex: 1;
            background-color: #f9f9f9;
            padding: 20px;
        }
        footer {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Mi Sitio Web</h1>
    </header>
    <nav>
        <a href="#">Inicio</a>
        <a href="#">Acerca de</a>
        <a href="#">Contacto</a>
    </nav>
    <main>
        <article>
            <h2>Artículo Principal</h2>
            <p>Este es el contenido principal del artículo. Aquí podemos hablar sobre diversos temas de interés.</p>
        </article>
        <aside>
            <h2>Barra Lateral</h2>
            <p>Esta es la barra lateral que contiene información adicional, enlaces, o anuncios.</p>
        </aside>
    </main>
    <footer>
        <p>© 2024 Mi Sitio Web</p>
    </footer>
</body>
</html>
```

## Contenido asociado
---
- [Video: Etiquetas de sección](https://vimeo.com/846187504/95a3f5e3b2)
