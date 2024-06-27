<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# HTML & CSS

Implementar CSS en un documento HTML es crucial para separar el contenido y la estructura del documento (HTML) del estilado visual (CSS). Esto hace que sea más fácil de mantener y modificar.

## Formas de aplicar CSS

---

**CSS en línea:** Aplicar estilos directamente en las etiquetas HTML usando el atributo `style`.

```html
<p style="color: crimson; padding: 8px; font-weight: bold">¡Bienvenidos!</p>
```

**Bloque de estilos internos:** Usar la etiqueta `<style>` en la sección `<head>` del documento HTML.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Mi aplicación web</title>
    <style>
        body {
            background: crimson;
            color: black;
        }
    </style>
</head>
...
</html>
```

**Hoja de estilos externa:** Enlazar un archivo CSS externo desde la cabecera del documento HTML usando la etiqueta `<link>`.

```html
<link rel="stylesheet" href="style.css" />
```

## ¿Cuál es la manera recomendada?

---

La manera recomendada es usar un archivo CSS externo. Esto te permite mantener el código HTML limpio y separar claramente la estructura del documento de su estilo visual. Además, facilita la reutilización de estilos y la gestión de tu código.

Enlazar una Hoja de Estilo Externa. Para enlazar un archivo CSS externo, sigue estos pasos:

**Crea la estructura de archivos:**

```markdown
PROYECTO
    🟥 index.html
    🟦 style.css
```

**Modifica el documento HTML para enlazar la hoja de estilo:**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Document</title>
  </head>
  <body>
    <header>
      <h1>Esto es un título</h1>
    </header>
    <main>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae
        labore praesentium, nihil soluta molestias nemo, quidem possimus culpa
        magni provident consequuntur placeat nisi aut doloribus, sunt cum quos
        officiis dignissimos?
      </p>
    </main>
  </body>
</html>
```

**Crea el archivo style.css con reglas básicas:**

```css
body {
    background-color: whitesmoke;
    color: crimson;
}

p {
    color: rgb(109, 11, 31);
    font-style: italic;
}
```

## Estructura completa del proyecto

---

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Document</title>
  </head>
  <body>
    <header>
      <h1>Esto es un título</h1>
    </header>
    <main>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Repudiandae
        labore praesentium, nihil soluta molestias nemo, quidem possimus culpa
        magni provident consequuntur placeat nisi aut doloribus, sunt cum quos
        officiis dignissimos?
      </p>
    </main>
  </body>
</html>
```

```css
body {
    background-color: whitesmoke;
    color: crimson;
}

p {
    color: rgb(109, 11, 31);
    font-style: italic;
}
```

## Reto Coding

---

Para practicar estos conceptos, vamos a generar un documento HTML con el siguiente contenido y enlazar un archivo CSS externo:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Document</title>
  </head>
  <body>
    <header>
      <h1>Enlazando hojas de estilos</h1>
    </header>
    <main>
      <ol>
        <li>Generar un fichero style.css</li>
        <li>Utilizar correctamente la etiqueta link</li>
        <li>Aplicar reglas de estilo</li>
      </ol>
    </main>
  </body>
</html>
```

```css
body {
  background-color: rgb(43, 43, 43);
  color: whitesmoke;
}

h1 {
  text-transform: uppercase;
}

li {
  color: crimson;
  font-style: italic;
}
```

1. Crea los archivos `index.html` y `style.css`.
2. Enlaza correctamente el archivo `style.css` en `index.html` usando la etiqueta `<link>`.
3. Aplica las reglas de estilo proporcionadas y observa los cambios en el navegador.
4. Experimenta cambiando los valores de las reglas CSS para ver cómo afectan la apariencia de la página.

**Solución Reto Coding**

Vamos a crear los archivos `index.html` y `style.css` y enlazarlos correctamente. Aquí tienes las instrucciones paso a paso:

Crea un archivo llamado `index.html` con el siguiente contenido:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Document</title>
  </head>
  <body>
    <header>
      <h1>Enlazando hojas de estilos</h1>
    </header>
    <main>
      <ol>
        <li>Generar un fichero style.css</li>
        <li>Utilizar correctamente la etiqueta link</li>
        <li>Aplicar reglas de estilo</li>
      </ol>
    </main>
  </body>
</html>
```

Crea un archivo llamado `style.css` con el siguiente contenido:

```css
body {
  background-color: rgb(43, 43, 43);
  color: whitesmoke;
}

h1 {
  text-transform: uppercase;
}

li {
  color: crimson;
  font-style: italic;
}
```

Ya hemos enlazado el archivo CSS en el archivo HTML usando la etiqueta `<link>` dentro de la sección `<head>`:

```html
<link rel="stylesheet" href="style.css" />
```

Abre el archivo `index.html` en tu navegador para ver los cambios aplicados por el archivo `style.css`. Deberías ver los siguientes estilos aplicados:

- El fondo de la página debería ser de color `rgb(43, 43, 43)`.
- El texto de la página debería ser de color `whitesmoke`.
- El encabezado (`<h1>`) debería aparecer en mayúsculas.
- Los elementos de la lista (`<li>`) deberían ser de color `crimson` y tener un estilo de fuente en cursiva.

Para entender mejor cómo funcionan las reglas CSS, intenta cambiar algunos valores en `style.css` y observa los efectos en el navegador. Por ejemplo, puedes cambiar el color de fondo o el estilo de los elementos de la lista:

```css
body {
  background-color: lightblue; /* Cambia el color de fondo a lightblue */
  color: black; /* Cambia el color del texto a negro */
}

h1 {
  text-transform: lowercase; /* Cambia el texto a minúsculas */
}

li {
  color: blue; /* Cambia el color de los elementos de la lista a azul */
  font-style: normal; /* Cambia el estilo de fuente a normal */
}
```

Guarda los cambios y actualiza la página en tu navegador para ver el nuevo aspecto.