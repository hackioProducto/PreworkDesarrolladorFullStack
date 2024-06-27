<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Creación de un CV con HTML5

A continuación te facilitamos una guía para crear un CV completo utilizando HTML5, asegurando el uso adecuado de las etiquetas y atributos esenciales para mejorar la accesibilidad y el SEO.

## Paso 1: Estructura básica del documento HTML

---

El objetivo es establecer la estructura básica del documento HTML, incluyendo la declaración `<!DOCTYPE html>`, y las secciones `<html>`, `<head>`, y `<body>`.

### 

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Curriculum Vitae de [Tu Nombre]">
    <meta name="author" content="[Tu Nombre]">
    <meta name="keywords" content="Curriculum Vitae, CV, [Tu Profesión], [Tus Habilidades]">
    <title>Curriculum Vitae de [Tu Nombre]</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Contenido del CV irá aquí -->
</body>
</html>

```

## Paso 2: Cabecera del CV

---

El objetivo es añadir una cabecera que incluya el nombre, una foto y un resumen profesional.

```html
<body>
  <header>
    <h1>[Tu Nombre]</h1>
    <img src="foto.jpg" alt="Foto de [Tu Nombre]" width="150" height="150" />
    <p>Resumen Profesional: [Breve resumen sobre tu carrera y habilidades]</p>
  </header>
  <!-- Otras secciones del CV irán aquí -->
</body>
```

## Paso 3: Sección de información personal

---

El objetivo es añadir una sección que contenga la información personal relevante, como dirección, teléfono, correo electrónico y enlaces a redes sociales.

```html
<body>
  <!-- Cabecera -->
  <header>
    <h1>[Tu Nombre]</h1>
    <img src="foto.jpg" alt="Foto de [Tu Nombre]" width="150" height="150" />
    <p>Resumen Profesional: [Breve resumen sobre tu carrera y habilidades]</p>
  </header>
  <!-- Información Personal -->
  <section>
    <h2>Información Personal</h2>
    <p>Dirección: [Tu Dirección]</p>
    <p>Teléfono: <a href="tel:+34123456789">+34 123 456 789</a></p>
    <p>Email: <a href="mailto:tuemail@dominio.com">tuemail@dominio.com</a></p>
    <p>
      LinkedIn:
      <a href="https://www.linkedin.com/in/tuusuario"
        >linkedin.com/in/tuusuario</a
      >
    </p>
  </section>
  <!-- Otras secciones del CV irán aquí -->
</body>
```

## Paso 4: sección de educación

---

Incluimos una sección que describa la educación del candidato, utilizando etiquetas semánticas para estructurar la información.

```html
<body>
  <!-- Cabecera y Información Personal -->
  <header>
    <h1>[Tu Nombre]</h1>
    <img src="foto.jpg" alt="Foto de [Tu Nombre]" width="150" height="150" />
    <p>Resumen Profesional: [Breve resumen sobre tu carrera y habilidades]</p>
  </header>
  <section>
    <h2>Información Personal</h2>
    <p>Dirección: [Tu Dirección]</p>
    <p>Teléfono: <a href="tel:+34123456789">+34 123 456 789</a></p>
    <p>Email: <a href="mailto:tuemail@dominio.com">tuemail@dominio.com</a></p>
    <p>
      LinkedIn:
      <a href="https://www.linkedin.com/in/tuusuario"
        >linkedin.com/in/tuusuario</a
      >
    </p>
  </section>
  <!-- Educación -->
  <section>
    <h2>Educación</h2>
    <article>
      <h3>Licenciatura en [Tu Carrera]</h3>
      <p>Universidad: [Nombre de la Universidad]</p>
      <p>Año de Graduación: [Año]</p>
      <p>
        Descripción: [Descripción breve de tus logros y actividades en la
        universidad]
      </p>
    </article>
    <article>
      <h3>Máster en [Tu Especialidad]</h3>
      <p>Universidad: [Nombre de la Universidad]</p>
      <p>Año de Graduación: [Año]</p>
      <p>
        Descripción: [Descripción breve de tus logros y actividades en el
        máster]
      </p>
    </article>
  </section>
  <!-- Otras secciones del CV irán aquí -->
</body>
```

## Paso 5: sección de experiencia profesional

---

Añadimos una sección para detallar la experiencia profesional del candidato, incluyendo información sobre los puestos de trabajo, las responsabilidades y los logros.

```html
<body>
  <!-- Cabecera, Información Personal y Educación -->
  <header>
    <h1>[Tu Nombre]</h1>
    <img src="foto.jpg" alt="Foto de [Tu Nombre]" width="150" height="150" />
    <p>Resumen Profesional: [Breve resumen sobre tu carrera y habilidades]</p>
  </header>
  <section>
    <h2>Información Personal</h2>
    <p>Dirección: [Tu Dirección]</p>
    <p>Teléfono: <a href="tel:+34123456789">+34 123 456 789</a></p>
    <p>Email: <a href="mailto:tuemail@dominio.com">tuemail@dominio.com</a></p>
    <p>
      LinkedIn:
      <a href="https://www.linkedin.com/in/tuusuario"
        >linkedin.com/in/tuusuario</a
      >
    </p>
  </section>
  <section>
    <h2>Educación</h2>
    <article>
      <h3>Licenciatura en [Tu Carrera]</h3>
      <p>Universidad: [Nombre de la Universidad]</p>
      <p>Año de Graduación: [Año]</p>
      <p>
        Descripción: [Descripción breve de tus logros y actividades en la
        universidad]
      </p>
    </article>
    <article>
      <h3>Máster en [Tu Especialidad]</h3>
      <p>Universidad: [Nombre de la Universidad]</p>
      <p>Año de Graduación: [Año]</p>
      <p>
        Descripción: [Descripción breve de tus logros y actividades en el
        máster]
      </p>
    </article>
  </section>
  <!-- Experiencia Profesional -->
  <section>
    <h2>Experiencia Profesional</h2>
    <article>
      <h3>Posición: [Tu Puesto]</h3>
      <p>Empresa: [Nombre de la Empresa]</p>
      <p>Fechas: [Fecha de Inicio] - [Fecha de Finalización]</p>
      <p>Descripción: [Descripción de tus responsabilidades y logros]</p>
    </article>
    <article>
      <h3>Posición: [Tu Puesto Anterior]</h3>
      <p>Empresa: [Nombre de la Empresa Anterior]</p>
      <p>Fechas: [Fecha de Inicio] - [Fecha de Finalización]</p>
      <p>Descripción: [Descripción de tus responsabilidades y logros]</p>
    </article>
  </section>
  <!-- Otras secciones del CV irán aquí -->
</body>
```

## Paso 6: sección de habilidades

---

Añadimos una sección para destacar las habilidades y competencias del candidato, utilizando listas para una presentación clara y organizada.

```html
<body>
  <!-- Cabecera, Información Personal, Educación y Experiencia Profesional -->
  <header>
    <h1>[Tu Nombre]</h1>
    <img src="foto.jpg" alt="Foto de [Tu Nombre]" width="150" height="150" />
    <p>Resumen Profesional: [Breve resumen sobre tu carrera y habilidades]</p>
  </header>
  <section>
    <h2>Información Personal</h2>
    <p>Dirección: [Tu Dirección]</p>
    <p>Teléfono: <a href="tel:+34123456789">+34 123 456 789</a></p>
    <p>Email: <a href="mailto:tuemail@dominio.com">tuemail@dominio.com</a></p>
    <p>
      LinkedIn:
      <a href="https://www.linkedin.com/in/tuusuario"
        >linkedin.com/in/tuusuario</a
      >
    </p>
  </section>
  <section>
    <h2>Educación</h2>
    <article>
      <h3>Licenciatura en [Tu Carrera]</h3>
      <p>Universidad: [Nombre de la Universidad]</p>
      <p>Año de Graduación: [Año]</p>
      <p>
        Descripción: [Descripción breve de tus logros y actividades en la
        universidad]
      </p>
    </article>
    <article>
      <h3>Máster en [Tu Especialidad]</h3>
      <p>Universidad: [Nombre de la Universidad]</p>
      <p>Año de Graduación: [Año]</p>
      <p>
        Descripción: [Descripción breve de tus logros y actividades en el
        máster]
      </p>
    </article>
  </section>
  <section>
    <h2>Experiencia Profesional</h2>
    <article>
      <h3>Posición: [Tu Puesto]</h3>
      <p>Empresa: [Nombre de la Empresa]</p>
      <p>Fechas: [Fecha de Inicio] - [Fecha de Finalización]</p>
      <p>Descripción: [Descripción de tus responsabilidades y logros]</p>
    </article>
    <article>
      <h3>Posición: [Tu Puesto Anterior]</h3>
      <p>Empresa: [Nombre de la Empresa Anterior]</p>
      <p>Fechas: [Fecha de Inicio] - [Fecha de Finalización]</p>
      <p>Descripción: [Descripción de tus responsabilidades y logros]</p>
    </article>
  </section>
  <!-- Habilidades -->
  <section>
    <h2>Habilidades</h2>
    <ul>
      <li>Habilidad 1: [Descripción de la Habilidad]</li>
      <li>Habilidad 2: [Descripción de la Habilidad]</li>
      <li>Habilidad 3: [Descripción de la Habilidad]</li>
      <li>Habilidad 4: [Descripción de la Habilidad]</li>
    </ul>
  </section>
  <!-- Otras secciones del CV irán aquí -->
</body>
```

## Paso 7: sección de proyectos

---

Incluimos una sección para detallar los proyectos destacados en los que ha trabajado el candidato, utilizando enlaces para proporcionar más información.

```html
<body>
  <!-- Cabecera, Información Personal, Educación, Experiencia Profesional y Habilidades -->
  <header>
    <h1>[Tu Nombre]</h1>
    <img src="foto.jpg" alt="Foto de [Tu Nombre]" width="150" height="150" />
    <p>Resumen Profesional: [Breve resumen sobre tu carrera y habilidades]</p>
  </header>
  <section>
    <h2>Información Personal</h2>
    <p>Dirección: [Tu Dirección]</p>
    <p>Teléfono: <a href="tel:+34123456789">+34 123 456 789</a></p>
    <p>Email: <a href="mailto:tuemail@dominio.com">tuemail@dominio.com</a></p>
    <p>
      LinkedIn:
      <a href="https://www.linkedin.com/in/tuusuario"
        >linkedin.com/in/tuusuario</a
      >
    </p>
  </section>
  <section>
    <h2>Educación</h2>
    <article>
      <h3>Licenciatura en [Tu Carrera]</h3>
      <p>Universidad: [Nombre de la Universidad]</p>
      <p>Año de Graduación: [Año]</p>
      <p>
        Descripción: [Descripción breve de tus logros y actividades en la
        universidad]
      </p>
    </article>
    <article>
      <h3>Máster en [Tu Especialidad]</h3>
      <p>Universidad: [Nombre de la Universidad]</p>
      <p>Año de Graduación: [Año]</p>
      <p>
        Descripción: [Descripción breve de tus logros y actividades en el
        máster]
      </p>
    </article>
  </section>
  <section>
    <h2>Experiencia Profesional</h2>
    <article>
      <h3>Posición: [Tu Puesto]</h3>
      <p>Empresa: [Nombre de la Empresa]</p>
      <p>Fechas: [Fecha de Inicio] - [Fecha de Finalización]</p>
      <p>Descripción: [Descripción de tus responsabilidades y logros]</p>
    </article>
    <article>
      <h3>Posición: [Tu Puesto Anterior]</h3>
      <p>Empresa: [Nombre de la Empresa Anterior]</p>
      <p>Fechas: [Fecha de Inicio] - [Fecha de Finalización]</p>
      <p>Descripción: [Descripción de tus responsabilidades y logros]</p>
    </article>
  </section>
  <section>
    <h2>Habilidades</h2>
    <ul>
      <li>Habilidad 1: [Descripción de la Habilidad]</li>
      <li>Habilidad 2: [Descripción de la Habilidad]</li>
      <li>Habilidad 3: [Descripción de la Habilidad]</li>
      <li>Habilidad 4: [Descripción de la Habilidad]</li>
    </ul>
  </section>
  <!-- Proyectos -->
  <section>
    <h2>Proyectos</h2>
    <article>
      <h3>
        Proyecto 1:
        <a href="https://enlace-a-proyecto1.com">Nombre del Proyecto</a>
      </h3>
      <p>
        Descripción: [Breve descripción del proyecto, tecnologías utilizadas y
        tu rol en el proyecto]
      </p>
    </article>
    <article>
      <h3>
        Proyecto 2:
        <a href="https://enlace-a-proyecto2.com">Nombre del Proyecto</a>
      </h3>
      <p>
        Descripción: [Breve descripción del proyecto, tecnologías utilizadas y
        tu rol en el proyecto]
      </p>
    </article>
  </section>
  <!-- Otras secciones del CV irán aquí -->
</body>
```

## Paso 8: optimización del rendimiento

---

Implementamos técnicas para optimizar el rendimiento del CV, incluyendo compresión de archivos y uso de la caché del navegador.

Compresión de archivos

```html
<link rel="stylesheet" href="styles.min.css">
```

Uso de la caché del navegador

```html
<meta http-equiv="Cache-Control" content="max-age=604800">
<link rel="stylesheet" type="text/css" href="styles.css?v=1">
```

**Reducción de solicitudes HTTP:** Combina múltiples archivos CSS en uno solo.

```html
<link rel="stylesheet" href="combined.min.css">
```

## Ejemplo completo de un CV en HTML5

---

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="Curriculum Vitae de [Tu Nombre]" />
    <meta name="author" content="[Tu Nombre]" />
    <meta
      name="keywords"
      content="Curriculum Vitae, CV, [Tu Profesión], [Tus Habilidades]"
    />
    <meta http-equiv="Cache-Control" content="max-age=604800" />
    <title>Curriculum Vitae de [Tu Nombre]</title>
    <link rel="stylesheet" href="styles.min.css" />
    <script src="scripts.min.js" defer></script>
  </head>
  <body>
    <header>
      <h1>[Tu Nombre]</h1>
      <img src="foto.jpg" alt="Foto de [Tu Nombre]" width="150" height="150" />
      <p>Resumen Profesional: [Breve resumen sobre tu carrera y habilidades]</p>
    </header>
    <section>
      <h2>Información Personal</h2>
      <p>Dirección: [Tu Dirección]</p>
      <p>Teléfono: <a href="tel:+34123456789">+34 123 456 789</a></p>
      <p>Email: <a href="mailto:tuemail@dominio.com">tuemail@dominio.com</a></p>
      <p>
        LinkedIn:
        <a href="https://www.linkedin.com/in/tuusuario"
          >linkedin.com/in/tuusuario</a
        >
      </p>
    </section>
    <section>
      <h2>Educación</h2>
      <article>
        <h3>Licenciatura en [Tu Carrera]</h3>
        <p>Universidad: [Nombre de la Universidad]</p>
        <p>Año de Graduación: [Año]</p>
        <p>
          Descripción: [Descripción breve de tus logros y actividades en la
          universidad]
        </p>
      </article>
      <article>
        <h3>Máster en [Tu Especialidad]</h3>
        <p>Universidad: [Nombre de la Universidad]</p>
        <p>Año de Graduación: [Año]</p>
        <p>
          Descripción: [Descripción breve de tus logros y actividades en el
          máster]
        </p>
      </article>
    </section>
    <section>
      <h2>Experiencia Profesional</h2>
      <article>
        <h3>Posición: [Tu Puesto]</h3>
        <p>Empresa: [Nombre de la Empresa]</p>
        <p>Fechas: [Fecha de Inicio] - [Fecha de Finalización]</p>
        <p>Descripción: [Descripción de tus responsabilidades y logros]</p>
      </article>
      <article>
        <h3>Posición: [Tu Puesto Anterior]</h3>
        <p>Empresa: [Nombre de la Empresa Anterior]</p>
        <p>Fechas: [Fecha de Inicio] - [Fecha de Finalización]</p>
        <p>Descripción: [Descripción de tus responsabilidades y logros]</p>
      </article>
    </section>
    <section>
      <h2>Habilidades</h2>
      <ul>
        <li>Habilidad 1: [Descripción de la Habilidad]</li>
        <li>Habilidad 2: [Descripción de la Habilidad]</li>
        <li>Habilidad 3: [Descripción de la Habilidad]</li>
        <li>Habilidad 4: [Descripción de la Habilidad]</li>
      </ul>
    </section>
    <section>
      <h2>Proyectos</h2>
      <article>
        <h3>
          Proyecto 1:
          <a href="https://enlace-a-proyecto1.com">Nombre del Proyecto</a>
        </h3>
        <p>
          Descripción: [Breve descripción del proyecto, tecnologías utilizadas y
          tu rol en el proyecto]
        </p>
      </article>
      <article>
        <h3>
          Proyecto 2:
          <a href="https://enlace-a-proyecto2.com">Nombre del Proyecto</a>
        </h3>
        <p>
          Descripción: [Breve descripción del proyecto, tecnologías utilizadas y
          tu rol en el proyecto]
        </p>
      </article>
    </section>
  </body>
</html>
```

## CSS asociado

---

- **General Styles**:
    - Definimos una fuente base (`Arial`) para todo el documento y ajustamos los márgenes y el padding.
    - Configuramos el color de fondo del `body` a un gris claro y el color de texto a un tono oscuro para mejorar la legibilidad.
- **Header**:
    - Establecemos un fondo oscuro con texto blanco para el `header`.
    - Añadimos un padding para dar espacio alrededor del contenido.
    - Centramos el texto y hacemos que la imagen sea redonda y tenga un margen superior.
- **Section**:
    - Creamos un fondo blanco para cada sección, con márgenes automáticos para centrar el contenido y un padding para la separación interna.
    - Añadimos un borde redondeado y una sombra para darle profundidad.
- **Article**:
    - Añadimos un margen inferior para separar los artículos.
    - Definimos un color oscuro para los títulos de los artículos.
- **Listas**:
    - Establecemos un fondo gris claro para los elementos de la lista, con márgenes y paddings para la separación.
    - Añadimos una barra lateral a la izquierda con un borde sólido para destacar los elementos.
- **Enlaces**:
    - Establecemos un color azul para los enlaces con un efecto hover que subraya el texto.
- **Responsive Design**:
    - Ajustamos el padding y el margen para pantallas pequeñas (menores a 600px).
    - Reducimos el tamaño de la imagen del `header` para adaptarse mejor a pantallas pequeñas.

```css
/* General Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.6;
    color: #333;
    background-color: #f4f4f4;
}

header {
    background: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
}

header img {
    border-radius: 50%;
    margin-top: 10px;
}

header h1 {
    margin: 0;
}

section {
    background: #fff;
    margin: 20px auto;
    padding: 20px;
    border-radius: 5px;
    max-width: 800px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

section h2 {
    border-bottom: 2px solid #333;
    padding-bottom: 5px;
    margin-bottom: 20px;
    color: #333;
}

article {
    margin-bottom: 20px;
}

article h3 {
    color: #333;
    margin-bottom: 10px;
}

ul {
    list-style-type: none;
    padding: 0;
}

ul li {
    background: #f4f4f4;
    margin: 5px 0;
    padding: 10px;
    border-left: 5px solid #333;
}

a {
    color: #333;
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
}

/* Specific Styles for Contact Information */
section p {
    margin: 5px 0;
}

section a {
    color: #007BFF;
}

section a:hover {
    text-decoration: underline;
}

/* Styles for responsive design */
@media (max-width: 600px) {
    header, section {
        padding: 10px;
    }

    section {
        margin: 10px;
    }

    header img {
        width: 100px;
        height: 100px;
    }
}

```