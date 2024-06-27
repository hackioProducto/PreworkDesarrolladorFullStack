<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Estructura básica del documento HTML
HTML (HyperText Markup Language) es el lenguaje que usamos para crear páginas web. Imagina que HTML es como las instrucciones para construir una casa de Lego. Te dice qué piezas usar y dónde ponerlas para construir la casa. Cada pieza de Lego es como una "etiqueta" HTML.

## Tipo de documento (DOCTYPE)

---

La primera línea en cualquier documento HTML es `<!DOCTYPE html>`. Esta línea no es una etiqueta HTML normal, sino una declaración especial que le dice al navegador (el programa que usas para ver páginas web, como Chrome o Firefox) cómo debe mostrar la página.

### ¿Por qué es importante DOCTYPE?

Imagina que estás jugando un juego y hay diferentes versiones del juego con diferentes reglas. `<!DOCTYPE html>` le dice al navegador que use la versión más reciente y mejor de las reglas para mostrar la página web.

```html
<!DOCTYPE html>
```

Esta línea es como decir: "¡Hey, navegador! Usa las reglas modernas para mostrar esta página web."

## Elemento `<html>`

---

El elemento `<html>` es como la caja que contiene todas las piezas de tu página web. Todo el contenido de la página va dentro de esta caja.

### ¿Por qué es importante el elemento `<html>`?

El elemento `<html>` le dice al navegador que todo lo que está dentro de él es parte de la página web.

```html
htmlCopiar código
<html>
  <!-- Aquí irá todo el contenido de la página web -->
</html>
```

## Atributo de Idioma (`lang`)

---

El atributo `lang` le dice al navegador en qué idioma está escrita la página. Esto es útil para que los motores de búsqueda (como Google) y las herramientas de accesibilidad (como los lectores de pantalla para personas ciegas) sepan qué idioma están leyendo.

### ¿Por qué es importante el atributo `lang`?

Si tienes una página en español, puedes decirle al navegador que la página está en español. Esto ayuda a que la página se muestre correctamente y sea entendida por más personas.

```html
<html lang="es">
  <!-- Contenido en español -->
</html>
```

## Encabezado del documento (`<head>`)

---

El `<head>` es una sección del documento HTML que contiene información sobre la página web que no se muestra directamente en la pantalla, pero que es crucial para el funcionamiento de la página.

### ¿Por qué es importante el `<head>`?

El `<head>` contiene cosas como el título de la página (que se muestra en la pestaña del navegador), la codificación de caracteres (para que se muestren correctamente las letras y símbolos), y otros metadatos importantes.

```html
<html lang="es">
  <head>
    <!-- Aquí va la información importante sobre la página -->
  </head>
  <body>
    <!-- Aquí va el contenido visible de la página -->
  </body>
</html>
```

## Codificación de caracteres (`<meta charset="utf-8">`)

---

La codificación de caracteres es como un conjunto de reglas que le dice al navegador cómo mostrar letras, números y símbolos. `UTF-8` es un tipo de codificación que puede mostrar prácticamente cualquier letra o símbolo del mundo.

### ¿Por qué es importante la codificación de caracteres?

Sin la codificación correcta, algunos caracteres podrían no mostrarse correctamente. Por ejemplo, letras con acentos o símbolos especiales podrían aparecer como signos extraños.

```html
<html lang="es">
  <head>
    <meta charset="utf-8">
  </head>
  <body>
    <!-- Contenido de la página -->
  </body>
</html>
```

## Título del documento (`<title>`)

---

El título del documento es el texto que aparece en la pestaña del navegador cuando visitas una página web. También es el texto que ves cuando guardas la página en tus favoritos.

### ¿Por qué es importante el título del documento?

El título ayuda a los usuarios a saber de qué trata la página y es importante para los motores de búsqueda.

```html
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Mi Página Web</title>
  </head>
  <body>
    <!-- Contenido de la página -->
  </body>
</html>
```

## Metadatos de Viewport (`<meta name="viewport" content="width=device-width, initial-scale=1">`)

---

El viewport es el área visible de la página web en la pantalla. Dependiendo del dispositivo (computadora, tableta, teléfono), el tamaño del viewport puede cambiar.

### ¿Por qué es importante la metaetiqueta viewport?

Esta metaetiqueta ayuda a que tu página web se vea bien en todos los dispositivos ajustando el ancho de la página al ancho de la pantalla.

```html
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Mi Página Web</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
  <body>
    <!-- Contenido de la página -->
  </body>
</html>
```

## Cuerpo del documento (`<body>`)

---

El `<body>` es la parte del documento HTML que contiene todo el contenido visible de la página web, como textos, imágenes, videos, etc.

### ¿Por qué es importante el `<body>`?

Todo lo que ves en una página web está dentro del `<body>`. Es donde va todo el contenido que los visitantes verán y con el que interactuarán.

```html
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Mi Página Web</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
  <body>
    <h1>Bienvenidos a Mi Página Web</h1>
    <p>Este es un párrafo de ejemplo.</p>
  </body>
</html>
```

### Estructura Básica de un Documento HTML

1. **`<!DOCTYPE html>`**: Esta es la primera línea del documento y sirve para indicar el tipo de documento. Es esencial para que los navegadores interpreten correctamente el HTML.
2. **`<html>`**: Este es el elemento raíz de una página HTML. Puedes especificar el idioma de la página usando el atributo `lang`, por ejemplo, `<html lang="es">` para español.
3. **`<head>`**: Contiene metainformación sobre la página HTML. Se usa para insertar diferentes metadatos, como el título de la página (`<title>`), enlaces a hojas de estilo (`<link>`), y scripts (`<script>`).
4. **`<body>`**: Define el cuerpo del documento y es un contenedor para todos los contenidos visibles, como encabezados, párrafos, imágenes, hipervínculos, tablas, listas, etc.
</aside>

## Ejemplos completo con todos los componentes

---

Vamos a desglosar el siguiente documento HTML en sus partes y dar varios ejemplos detallados. Para ello os presentamos la base que todo documento HTML debería tener por defecto

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Mi Página Web</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
  <body>
    <h1>Bienvenidos a Mi Página Web</h1>
    <p>Este es un párrafo de ejemplo.</p>
  </body>
</html>
```

**Snippet en VSCode**
Para generar automáticamente la estructura de un documento HTML en VSCode, simplemente escribe `html:5` y presiona `Enter`. Esto creará una plantilla básica de HTML5.

Aquí tienes algunos ejemplos adicionales que muestran cómo puedes variar los componentes del documento HTML para diferentes situaciones.

**Página en Inglés con título diferente**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Welcome to My Web Page</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
  <body>
    <h1>Welcome to My Web Page</h1>
    <p>This is an example paragraph.</p>
  </body>
</html>
```

**Página en Español con contenido adicional**

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Página de Ejemplo</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
  <body>
    <h1>Página de Ejemplo</h1>
    <p>Este es un párrafo de ejemplo en español.</p>
    <p>Aquí hay otro párrafo.</p>
  </body>
</html>

```

**Página multilingüe**

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="utf-8">
    <title>Página Bilingüe</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
  <body>
    <h1>Página Bilingüe</h1>
    <p lang="en">This is a paragraph in English.</p>
    <p>Este es un párrafo en español.</p>
  </body>
</html>
```

Estos ejemplos muestran cómo puedes personalizar cada parte del documento HTML para diferentes necesidades. Cada componente es importante para asegurarte de que tu página web funcione correctamente y se vea bien en todos los dispositivos.

## Reto Coding

---

Crea tu propio documento HTML sin usar los snippets de tu editor de código (VSCode).

### Instrucciones:

1. Crea una carpeta llamada `HTML`
2. Abre dicha carpeta en tu navegador.
3. Crea un nuevo archivo HTML llamado `basic_structures.hmtl`.
4. Escribe manualmente la estructura básica de un documento HTML siguiendo uno de los ejemplos proporcionados.

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Documento HTML Manual</title>
</head>
<body>
    <h1>Encabezado Creado Manualmente</h1>
    <p>Párrafo creado sin snippets.</p>
</body>
</html>

```
## Contenido asociado
---
- [Video: Estructura del documento HTML](https://vimeo.com/845880953/9d9577e5b0)
