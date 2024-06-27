<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Estructura tipo de un fichero CSS con variables y composición por bloques

Dado el siguiente html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Proyecto CSS</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Bienvenidos a Mi Sitio Web</h1>
  </header>

  <nav>
    <ul>
      <li><a href="#home">Inicio</a></li>
      <li><a href="#about">Sobre Nosotros</a></li>
      <li><a href="#services">Servicios</a></li>
      <li><a href="#contact">Contacto</a></li>
    </ul>
  </nav>

  <main>
    <div class="container">
      <section id="about">
        <h2>Sobre Nosotros</h2>
        <p>Somos una empresa dedicada a proporcionar soluciones tecnológicas innovadoras.</p>
        <p>Nuestro equipo está compuesto por profesionales altamente cualificados en diversas áreas de la tecnología.</p>
      </section>

      <section id="services">
        <h2>Servicios</h2>
        <div class="card">
          <h3>Desarrollo Web</h3>
          <p>Ofrecemos servicios de desarrollo web utilizando las últimas tecnologías y mejores prácticas.</p>
        </div>
        <div class="card">
          <h3>Consultoría IT</h3>
          <p>Brindamos asesoramiento experto para ayudar a las empresas a optimizar sus recursos tecnológicos.</p>
        </div>
        <div class="card">
          <h3>Soporte Técnico</h3>
          <p>Nuestro equipo de soporte técnico está disponible 24/7 para resolver cualquier problema técnico que pueda surgir.</p>
        </div>
      </section>
    </div>
  </main>

  <footer>
    <p>&copy; 2023 Mi Sitio Web. Todos los derechos reservados.</p>
  </footer>
</body>
</html>
```

Os vamos a proporcionar una referencia que puedes usar al comenzar un proyecto. Esta estructura está organizada en bloques, y utiliza variables CSS (custom properties) para definir colores, tamaños, espaciados y otros valores reutilizables.

```css
/* === Variables Globales === */
:root {
  /* Colores */
  --color-primary: #3498db;
  --color-secondary: #2ecc71;
  --color-accent: #e74c3c;
  --color-background: #f4f4f4;
  --color-text: #333;

  /* Tipografías */
  --font-family-base: 'Arial, sans-serif';
  --font-size-base: 16px;
  --font-size-lg: 1.25rem;
  --font-size-sm: 0.875rem;

  /* Espaciados */
  --spacing-xs: 4px;
  --spacing-sm: 8px;
  --spacing-md: 16px;
  --spacing-lg: 32px;
  --spacing-xl: 64px;

  /* Bordes y Sombras */
  --border-radius: 4px;
  --box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);

  /* Transiciones */
  --transition-speed: 0.3s;
}

/* === Reset CSS === */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

/* === Tipografía Global === */
body {
  font-family: var(--font-family-base);
  font-size: var(--font-size-base);
  line-height: 1.6;
  color: var(--color-text);
  background-color: var(--color-background);
}

/* === Espaciado Global === */
.container {
  width: 80%;
  margin: 0 auto;
  padding: var(--spacing-lg);
}

/* === Cabecera === */
header {
  background-color: var(--color-primary);
  color: white;
  padding: var(--spacing-md) 0;
  text-align: center;
}

header h1 {
  font-size: var(--font-size-lg);
}

/* === Navegación === */
nav {
  background-color: var(--color-secondary);
  padding: var(--spacing-sm) 0;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
}

nav ul li {
  margin: 0 var(--spacing-sm);
}

nav ul li a {
  color: white;
  text-decoration: none;
  padding: var(--spacing-xs) var(--spacing-sm);
  transition: background-color var(--transition-speed);
}

nav ul li a:hover {
  background-color: var(--color-accent);
}

/* === Contenido Principal === */
main {
  padding: var(--spacing-lg) 0;
}

main h2 {
  font-size: var(--font-size-lg);
  color: var(--color-primary);
  border-bottom: 2px solid var(--color-secondary);
  padding-bottom: var(--spacing-xs);
  margin-bottom: var(--spacing-md);
}

main p {
  margin-bottom: var(--spacing-md);
}

/* === Tarjetas === */
.card {
  background: white;
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  padding: var(--spacing-md);
  margin-bottom: var(--spacing-md);
}

.card h3 {
  font-size: var(--font-size-lg);
  margin-bottom: var(--spacing-sm);
}

.card p {
  font-size: var(--font-size-sm);
}

/* === Pie de Página === */
footer {
  background-color: var(--color-primary);
  color: white;
  text-align: center;
  padding: var(--spacing-md) 0;
  position: relative;
  bottom: 0;
  width: 100%;
}

/* === Media Queries === */
@media screen and (max-width: 768px) {
  .container {
    width: 90%;
  }

  nav ul {
    flex-direction: column;
    align-items: center;
  }

  nav ul li {
    margin: var(--spacing-xs) 0;
  }
}

@media screen and (max-width: 480px) {
  header h1 {
    font-size: var(--font-size-base);
  }

  main h2 {
    font-size: var(--font-size-base);
  }

  .card {
    padding: var(--spacing-sm);
  }

  .card h3 {
    font-size: var(--font-size-base);
  }
}
```

1. **Variables Globales**: Define las variables globales en el `:root` para colores, tipografías, espaciados, bordes, sombras y transiciones. Estas variables se utilizan en todo el archivo para mantener la coherencia y facilitar los cambios.
2. **Reset CSS**: Aplica un reset básico para asegurarse de que todos los elementos tienen el mismo estilo inicial.
3. **Tipografía Global**: Define las propiedades tipográficas básicas para el `body`.
4. **Espaciado Global**: Define una clase `.container` para el ancho y el padding globales.
5. **Cabecera**: Estilos específicos para el `header`, incluyendo el color de fondo, color de texto y padding.
6. **Navegación**: Estilos para la barra de navegación (`nav`), incluyendo la disposición de los elementos de la lista.
7. **Contenido Principal**: Estilos para el contenido principal (`main`), incluyendo los títulos y los párrafos.
8. **Tarjetas**: Define estilos para las tarjetas (`.card`), que incluyen fondo blanco, borde redondeado, sombra y padding.
9. **Pie de Página**: Estilos específicos para el `footer`, incluyendo el color de fondo, color de texto y padding.
10. **Media Queries**: Ajustes responsivos para diferentes tamaños de pantalla. Aquí se ajustan los anchos de los contenedores, la disposición de la navegación y el tamaño de las fuentes en dispositivos móviles.

## Contenido asociado
---
- [Video: Estructura tipo de un fichero CSS](https://vimeo.com/966736716/1384b2efdd?share=copy)
