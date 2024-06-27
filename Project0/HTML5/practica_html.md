<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Practica HTML5

A continuación, te presentamos una práctica autoevaluable diseñada para que pongas en práctica los conceptos que has aprendido sobre HTML5, su estructura, etiquetas semánticas, contenido multimedia, formularios y optimización. Al final de cada sección encontrarás preguntas para autoevaluarte.

## Sección 1: Creación de una Página Principal

---

**Objetivo:** Crear la estructura básica de una página web utilizando etiquetas semánticas de HTML5.

**Autoevaluación:**

1. ¿Utilizaste las etiquetas semánticas correctamente (header, nav, main, section, footer)?
2. ¿La estructura del documento incluye las secciones `<head>` y `<body>`?
3. ¿Agregaste los enlaces a la hoja de estilos CSS y al archivo JavaScript?

**Solución**:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Mi Sitio Web</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <header>
      <h1>Bienvenidos a Mi Sitio Web</h1>
      <nav>
        <ul>
          <li><a href="#inicio">Inicio</a></li>
          <li><a href="#sobre-mi">Sobre Mí</a></li>
          <li><a href="#contacto">Contacto</a></li>
        </ul>
      </nav>
    </header>
    <main>
      <section id="inicio">
        <h2>Inicio</h2>
        <p>Esta es la sección de inicio de mi sitio web.</p>
      </section>
      <section id="sobre-mi">
        <h2>Sobre Mí</h2>
        <p>Información sobre mí.</p>
      </section>
      <section id="contacto">
        <h2>Contacto</h2>
        <p>Formulario de contacto aquí.</p>
      </section>
    </main>
    <footer>
      <p>&copy; 2023 Mi Sitio Web. Todos los derechos reservados.</p>
    </footer>
    <script src="scripts.js"></script>
  </body>
</html>
```

## Sección 2: Inclusión de Contenido Multimedia

---

**Objetivo:** Integrar contenido multimedia en la página principal.

**Autoevaluación:**

1. ¿Agregaste correctamente las etiquetas `<video>` y `<audio>`?
2. ¿Incluiste los atributos `controls` en ambas etiquetas?
3. ¿Proporcionaste las fuentes de video y audio dentro de las etiquetas `<source>`?

**Solución**:

```html
<section id="inicio">
  <h2>Inicio</h2>
  <p>Esta es la sección de inicio de mi sitio web.</p>
  <video controls>
    <source src="video.mp4" type="video/mp4" />
    Tu navegador no soporta la etiqueta de video.
  </video>
  <audio controls>
    <source src="audio.mp3" type="audio/mpeg" />
    Tu navegador no soporta la etiqueta de audio.
  </audio>
</section>
```

### Sección 3: Creación de un Formulario de Contacto

---

**Objetivo:** Crear un formulario de contacto con validaciones HTML5.

**Autoevaluación:**

1. ¿Incluiste los campos de nombre, correo electrónico y mensaje?
    - Nombre (input type="text", obligatorio)
    - Correo electrónico (input type="email", obligatorio)
    - Mensaje (textarea, obligatorio)
    - Botón de envío (input type="submit")
2. ¿Utilizaste el atributo `required` para validar los campos obligatorios?
3. ¿Agregaste el botón de envío con el atributo `type="submit"`?

**Solución**:

```html
htmlCopiar código
<section id="contacto">
    <h2>Contacto</h2>
    <form action="/enviar" method="post">
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" name="nombre" required>
        <label for="email">Correo Electrónico:</label>
        <input type="email" id="email" name="email" required>
        <label for="mensaje">Mensaje:</label>
        <textarea id="mensaje" name="mensaje" required></textarea>
        <input type="submit" value="Enviar">
    </form>
</section>

```

### Sección 4: Optimización del Rendimiento

---

**Objetivo:** Optimizar la carga y el rendimiento de la página.

**Autoevaluación:**

1. ¿Minificaste los archivos CSS y JavaScript correctamente?
2. ¿Configuraste la caché del navegador utilizando el atributo `http-equiv="Cache-Control"`?
3. ¿Utilizaste la técnica de carga diferida para las imágenes y otros elementos no críticos?

**Solución**:

```html
<!-- Archivo HTML -->
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="Cache-Control" content="max-age=604800">
    <title>Mi Sitio Web</title>
    <link rel="stylesheet" href="styles.css?v=1">
</head>
<body>
    <header>
        <h1>Bienvenidos a Mi Sitio Web</h1>
        <nav>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#sobre-mi">Sobre Mí</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="inicio">
            <h2>Inicio</h2>
            <p>Esta es la sección de inicio de mi sitio web.</p>
            <video controls>
                <source src="video.mp4" type="video/mp4">
                Tu navegador no soporta la etiqueta de video.
            </video>
            <audio controls>
                <source src="audio.mp3" type="audio/mpeg">
                Tu navegador no soporta la etiqueta de audio.
            </audio>
        </section>
        <section id="sobre-mi">
            <h2>Sobre Mí</h2>
            <p>Información sobre mí.</p>
        </section>
        <section id="contacto">
            <h2>Contacto</h2>
            <form action="/enviar" method="post">
                <label for="nombre">Nombre:</label>
                <input type="text" id="nombre" name="nombre" required>
                <label for="email">Correo Electrónico:</label>
                <input type="email" id="email" name="email" required>
                <label for="mensaje">Mensaje:</label>
                <textarea id="mensaje" name="mensaje" required></textarea>
                <input type="submit" value="Enviar">
            </form>
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Mi Sitio Web. Todos los derechos reservados.</p>
    </footer>
    <script src="scripts.js?v=1"></script>
</body>
</html>
```