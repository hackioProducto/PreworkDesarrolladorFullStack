<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Importancia del buen uso de etiquetas

Utilizar las etiquetas HTML correctas para encapsular el contenido es esencial para la accesibilidad, el SEO (optimización en motores de búsqueda) y la correcta visualización de una página web. A continuación, se explica en detalle por qué es importante y cómo hacerlo correctamente, con varios ejemplos.

## Uso correcto de etiquetas

---

Imagina que tienes un documento con varios tipos de información: títulos, párrafos, listas, etc. HTML tiene etiquetas específicas para cada tipo de información, y es importante usarlas correctamente para que los navegadores y las herramientas de accesibilidad puedan interpretar correctamente el contenido.

Las etiquetas HTML deben ser usadas de acuerdo a su propósito. Aquí hay algunos ejemplos:

**Título principal (Encabezado):** Los títulos o encabezados deben usar las etiquetas de encabezado (`<h1>`, `<h2>`, etc.). El encabezado principal de la página debe ser `<h1>`, los subencabezados deben ser `<h2>`, y así sucesivamente.

```html
<h1>Soy un título</h1>
<!-- Correcto -->
<p>Soy un título</p>
<!-- Incorrecto -->
```

- `<h1>Soy un título</h1>`: Esta es la forma correcta de definir un título principal en una página. La etiqueta `<h1>` indica al navegador y a los motores de búsqueda que este es el título más importante de la página.
- `<p>Soy un título</p>`: Esto es incorrecto porque la etiqueta `<p>` es para párrafos, no para títulos. Usar etiquetas incorrectas puede confundir a los motores de búsqueda y a los usuarios que usan lectores de pantalla.

**Párrafo:** Los párrafos de texto deben estar dentro de etiquetas `<p>`.

```html
<p>Este es un párrafo de ejemplo.</p>
<!-- Correcto -->
<h1>Este es un párrafo de ejemplo.</h1>
<!-- Incorrecto -->
```

- `<p>Este es un párrafo de ejemplo.</p>`: Esta es la forma correcta de encapsular un bloque de texto que forma un párrafo.
- `<h1>Este es un párrafo de ejemplo.</h1>`: Esto es incorrecto porque `<h1>` es para títulos, no para párrafos. Usar una etiqueta de encabezado para un párrafo puede hacer que el contenido se vea mal y sea interpretado incorrectamente.

## Importancia para la Accesibilidad

---

Las etiquetas HTML ayudan a las tecnologías de asistencia, como los lectores de pantalla, a entender y navegar por el contenido de la página web. Por ejemplo, un lector de pantalla usa las etiquetas de encabezado para permitir a los usuarios saltar rápidamente entre secciones de la página.

```html
<h1>Bienvenidos a Mi Página Web</h1>
<p>Este es un párrafo de ejemplo.</p>
<h2>Sección Importante</h2>
<p>Más información en esta sección.</p>
```

En este ejemplo, un lector de pantalla puede decir al usuario que hay un título principal y una subsección, permitiendo una navegación más fácil.

## Importancia para el SEO

---

Los motores de búsqueda utilizan las etiquetas HTML para entender la estructura y el contenido de una página web. Usar las etiquetas correctas ayuda a mejorar la visibilidad de la página en los resultados de búsqueda.

```html
<h1>Guía Completa de Jardinería</h1>
<p>Bienvenidos a nuestra guía completa sobre jardinería.</p>
<h2>Capítulo 1: Introducción</h2>
<p>En este capítulo, aprenderás los conceptos básicos.</p>
```

En este ejemplo, los motores de búsqueda verán que "Guía Completa de Jardinería" es el tema principal de la página, y "Capítulo 1: Introducción" es una subsección, ayudando a indexar y clasificar mejor el contenido.

## Listas

---

Las listas deben estar dentro de etiquetas de lista (`<ul>`, `<ol>`, `<li>`).

**Lista ordenada (Numerada)**

```html
<ol>
  <li>Primero</li>
  <li>Segundo</li>
  <li>Tercero</li>
</ol>
```

**Lista no ordenada (Con Viñetas)**

```html
<ul>
  <li>Elemento uno</li>
  <li>Elemento dos</li>
  <li>Elemento tres</li>
</ul>
```

## Enlaces

---

Los enlaces deben estar dentro de etiquetas `<a>`.

```html
<a href="https://www.ejemplo.com">Visita Ejemplo</a>
```

- `<a href="https://www.ejemplo.com">Visita Ejemplo</a>`: Esto crea un enlace a "[https://www.ejemplo.com](https://www.ejemplo.com/)" con el texto "Visita Ejemplo". Es importante usar enlaces correctamente para que los usuarios puedan navegar fácilmente y los motores de búsqueda puedan rastrear e indexar páginas.
