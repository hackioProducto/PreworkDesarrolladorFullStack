<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Display: Flex - Diseño básico de Cards

Este ejemplo vamos a mostrar cómo usar Flex y media queries para crear un layout de cards de contenido que se adapta a diferentes tamaños de pantalla, siguiendo las mejores prácticas de diseño responsivo y mobile-first.

- **Mobile First**: Comienza con una tarjeta que ocupa el 100% del ancho disponible en pantallas pequeñas.
- **Media Queries**: A medida que el ancho de la pantalla aumenta, las tarjetas se reorganizan en una cuadrícula de 2 columnas (para pantallas medianas) y 3 columnas (para pantallas grandes).
- **Flexbox**: Se utiliza para organizar las tarjetas de contenido en una cuadrícula flexible y responsiva.

## Arquitectura de la información

---

- `<!DOCTYPE html>`: Define el documento como HTML5.
- `<html lang="en">`: Inicia el documento HTML y establece el idioma como inglés.
- `<head>`: Contiene metadatos sobre el documento.
    - `<meta charset="UTF-8" />`: Especifica la codificación de caracteres como UTF-8.
    - `<meta name="viewport" content="width=device-width, initial-scale=1.0" />`: Hace que el sitio sea responsivo en dispositivos móviles.
    - `<title>Tarjetas de Contenido</title>`: Define el título de la página.
    - `<style>`: Contiene las reglas CSS para la página.
- `<body>`: Contiene el contenido visible de la página.
    - `<div class="container">`: Un contenedor principal que agrupa las cards.
        - `<div class="card">`: Define una card de contenido.
            - `<img src="URL" alt="Description" />`: Muestra una imagen con una URL y una descripción alternativa.
            - `<div class="card-content">`: Contiene el contenido textual de la card.
                - `<h2>Title</h2>`: Título de la card.
                - `<p class="price">$Price</p>`: Precio del producto.
                - `<a href="#" class="cta">Shop now</a>`: Un enlace con una llamada a la acción.
                

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tarjetas de Contenido</title>
    <style>
      /* Aquí va el CSS */
    </style>
  </head>
  <body>
    <div class="container">
      <div class="card">
        <img
          src="https://images.pexels.com/photos/12248920/pexels-photo-12248920.jpeg"
          alt="Image 1"
        />
        <div class="card-content">
          <h2>Lounge Chair</h2>
          <p class="price">$149</p>
        </div>
      </div>
      <div class="card">
        <img
          src="https://images.pexels.com/photos/12248920/pexels-photo-12248920.jpeg"
          alt="Image 2"
        />
        <div class="card-content">
          <h2>Take it outside carpet</h2>
          <p class="price">$500</p>
          <a href="#" class="cta">Shop now</a>
        </div>
      </div>
      <div class="card">
        <img
          src="https://images.pexels.com/photos/12248920/pexels-photo-12248920.jpeg"
          alt="Image 3"
        />
        <div class="card-content">
          <h2>Modern Table</h2>
          <p class="price">$299</p>
        </div>
      </div>
    </div>
  </body>
</html>
```

## Estilos CSS

---

- `:root`: Define variables CSS.
    - `-gap`: Espacio entre elementos.
    - `-bg-color`: Color de fondo del cuerpo.
    - `-card-bg-color`: Color de fondo de las tarjetas.
    - `-text-color`: Color del texto.
- `body`: Define el estilo del cuerpo del documento.
    - `margin: 0`: Elimina el margen predeterminado.
    - `font-family: Arial, sans-serif`: Establece la fuente.
    - `background-color: var(--bg-color)`: Aplica el color de fondo usando la variable.
    - `display: flex`: Usa el modelo de caja flexible.
    - `justify-content: center`: Centra el contenido horizontalmente.
    - `padding: 20px`: Agrega un relleno alrededor del cuerpo.
- `.container`: Define el estilo del contenedor principal.
    - `display: flex`: Usa el modelo de caja flexible.
    - `flex-wrap: wrap`: Permite que los elementos se envuelvan en varias líneas.
    - `gap: var(--gap)`: Define el espacio entre las tarjetas.
    - `max-width: 1200px`: Establece el ancho máximo del contenedor.
- `.card`: Define el estilo de las tarjetas.
    - `background-color: var(--card-bg-color)`: Color de fondo de la tarjeta.
    - `padding: 20px`: Agrega un relleno interno.
    - `box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1)`: Aplica una sombra alrededor de la tarjeta.
    - `flex: 1 1 calc(100% - var(--gap))`: Define la flexibilidad de la tarjeta.
- `.card img`: Define el estilo de las imágenes dentro de las tarjetas.
    - `max-width: 100%`: Asegura que la imagen no exceda el ancho del contenedor.
    - `height: auto`: Mantiene la proporción de la imagen.
- `.card-content`: Estilo del contenedor de contenido textual dentro de la tarjeta.
    - `margin-top: 10px`: Espacio superior entre la imagen y el contenido.
- `.card-content h2`: Estilo para los títulos de las tarjetas.
    - `margin: 0`: Elimina el margen superior e inferior.
    - `color: var(--text-color)`: Aplica el color del texto.
- `.card-content p`: Estilo para los párrafos dentro de las tarjetas.
    - `color: var(--text-color)`: Aplica el color del texto.
- `.card-content .price`: Estilo para el precio del producto.
    - `color: #4CAF50`: Color verde.
    - `font-weight: bold`: Texto en negrita.
    - `margin-top: 10px`: Espacio superior.
- `.card-content .cta`: Estilo para el enlace de llamada a la acción.
    - `color: #4CAF50`: Color verde.
    - `text-decoration: none`: Elimina el subrayado del enlace.
    - `font-weight: bold`: Texto en negrita.
- `@media (min-width: 768px)`: Media query para pantallas con un ancho mínimo de 768px.
    - `.card`: Define el ancho de las tarjetas.
        - `flex: 1 1 calc(50% - var(--gap))`: Las tarjetas ocupan el 50% del ancho menos el espacio entre ellas.
- `@media (min-width: 1024px)`: Media query para pantallas con un ancho mínimo de 1024px.
    - `.card`: Define el ancho de las tarjetas.
        - `flex: 1 1 calc(33.333% - var(--gap))`: Las tarjetas ocupan el 33.333% del ancho menos el espacio entre ellas.

```css
:root {
    --gap: 20px;
    --bg-color: #f4f4f4;
    --card-bg-color: #ffffff;
    --text-color: #333;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: var(--bg-color);
    display: flex;
    justify-content: center;
    padding: 20px;
}

.container {
    display: flex;
    flex-wrap: wrap;
    gap: var(--gap);
    max-width: 1200px;
}

.card {
    background-color: var(--card-bg-color);
    padding: 20px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    flex: 1 1 calc(100% - var(--gap));
}

.card img {
    max-width: 100%;
    height: auto;
}

.card-content {
    margin-top: 10px;
}

.card-content h2 {
    margin: 0;
    color: var(--text-color);
}

.card-content p {
    color: var(--text-color);
}

.card-content .price {
    color: #4CAF50;
    font-weight: bold;
    margin-top: 10px;
}

.card-content .cta {
    color: #4CAF50;
    text-decoration: none;
    font-weight: bold;
}

@media (min-width: 768px) {
    .card {
        flex: 1 1 calc(50% - var(--gap));
    }
}

@media (min-width: 1024px) {
    .card {
        flex: 1 1 calc(33.333% - var(--gap));
    }
}

```

## Contenido para probar en un PEN

---

Para probar nuestro contenido y ver el resultado final podemos usar codepen

[CodePen](https://codepen.io/)

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tarjetas de Contenido</title>
    <style>
      :root {
          --gap: 20px;
          --bg-color: #f4f4f4;
          --card-bg-color: #ffffff;
          --text-color: #333;
      }

      body {
          margin: 0;
          font-family: Arial, sans-serif;
          background-color: var(--bg-color);
          display: flex;
          justify-content: center;
          padding: 20px;
      }

      .container {
          display: flex;
          flex-wrap: wrap;
          gap: var(--gap);
          max-width: 1200px;
      }

      .card {
          background-color: var(--card-bg-color);
          padding: 20px;
          box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
          flex: 1 1 calc(100% - var(--gap));
      }

      .card img {
          max-width: 100%;
          height: auto;
      }

      .card-content {
          margin-top: 10px;
      }

      .card-content h2 {
          margin: 0;
          color: var(--text-color);
      }

      .card-content p {
          color: var(--text-color);
      }

      .card-content .price {
          color: #4CAF50;
          font-weight: bold;
          margin-top: 10px;
      }

      .card-content .cta {
          color: #4CAF50;
          text-decoration: none;
          font-weight: bold;
      }

      @media (min-width: 768px) {
          .card {
              flex: 1 1 calc(50% - var(--gap));
          }
      }

      @media (min-width: 1024px) {
          .card {
              flex: 1 1 calc(33.333% - var(--gap));
          }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="card">
        <img
          src="https://images.pexels.com/photos/12248920/pexels-photo-12248920.jpeg"
          alt="Image 1"
        />
        <div class="card-content">
          <h2>Lounge Chair</h2>
          <p class="price">$149</p>
        </div>
      </div>
      <div class="card">
        <img
          src="https://images.pexels.com/photos/12248920/pexels-photo-12248920.jpeg"
          alt="Image 2"
        />
        <div class="card-content">
          <h2>Take it outside carpet</h2>
          <p class="price">$500</p>
          <a href="#" class="cta">Shop now</a>
        </div>
      </div>
      <div class="card">
        <img
          src="https://images.pexels.com/photos/12248920/pexels-photo-12248920.jpeg"
          alt="Image 3"
        />
        <div class="card-content">
          <h2>Modern Table</h2>
          <p class="price">$299</p>
        </div>
      </div>
    </div>
  </body>
</html>
```

## Mejorando la colección de tarjetas de contenido

---

- **Mobile First**: Comienza con tarjetas que ocupan el 100% del ancho disponible en pantallas pequeñas.
- **Media Queries**: A medida que el ancho de la pantalla aumenta, las tarjetas se reorganizan en una cuadrícula de 2 columnas (para pantallas medianas) y 3 columnas (para pantallas grandes).
- **Flexbox**: Se utiliza para organizar las tarjetas de contenido en una cuadrícula flexible y responsiva.

Este ejemplo muestra cómo usar Flexbox y media queries para crear un layout de tarjetas de contenido que se adapta a diferentes tamaños de pantalla, siguiendo las mejores prácticas de diseño responsivo y mobile-first.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Colección de Tarjetas de Contenido</title>
    <style>
        :root {
            --gap: 20px;
            --bg-color: #ffffff;
            --card-bg-color: #f9f9f9;
            --text-color: #333;
            --highlight-color: #000;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: var(--bg-color);
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            gap: var(--gap);
            max-width: 1200px;
            justify-content: center;
        }

        .card {
            background-color: var(--card-bg-color);
            padding: 20px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            flex: 1 1 calc(33.333% - var(--gap));
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        .card img {
            max-width: 100%;
            height: auto;
        }

        .card-content {
            margin-top: 10px;
        }

        .card-content h2 {
            margin: 10px 0;
            font-size: 2rem;
            color: var(--highlight-color);
        }

        .card-content p {
            color: var(--text-color);
        }

        .card-content .cta {
            color: var(--highlight-color);
            text-decoration: none;
            font-weight: bold;
        }

        .header {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        @media (max-width: 767px) {
            .card {
                flex: 1 1 calc(50% - var(--gap));
            }

            .header {
                font-size: 2rem;
            }
        }

        @media (max-width: 480px) {
            .card {
                flex: 1 1 100%;
            }

            .header {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="header">TRAVEL EXPERIENCE</div>
    <div class="container">
        <div class="card">
            <img src="https://images.pexels.com/photos/12248920/pexels-photo-12248920.jpeg" alt="Image 1">
            <div class="card-content">
                <h2>01/</h2>
                <p>The open sea, the salty breeze, the warm sun. We love travel as much as you do, so let's plan your next trip together.</p>
                <a href="#" class="cta">Read more →</a>
            </div>
        </div>
        <div class="card">
            <img src="https://images.pexels.com/photos/12248920/pexels-photo-12248920.jpeg" alt="Image 2">
            <div class="card-content">
                <h2>02/</h2>
                <p>The open sea, the salty breeze, the warm sun. We love travel as much as you do, so let's plan your next trip together.</p>
                <a href="#" class="cta">Read more →</a>
            </div>
        </div>
        <div class="card">
            <img src="https://images.pexels.com/photos/12248920/pexels-photo-12248920.jpeg" alt="Image 3">
            <div class="card-content">
                <h2>03/</h2>
                <p>The open sea, the salty breeze, the warm sun. We love travel as much as you do, so let's plan your next trip together.</p>
                <a href="#" class="cta">Read more →</a>
            </div>
        </div>
    </div>
</body>
</html>
```

## Tabla de Precios

---

Vamos a replicar el diseño de la tabla de precios utilizando Flexbox, media queries y la metodología "mobile-first". A continuación, se presenta el HTML y CSS integrado para que puedas copiar y ver el funcionamiento directamente en tu navegador.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabla de Precios</title>
    <style>
        :root {
            --gap: 20px;
            --bg-color: #4a4e69;
            --card-bg-color: #ffffff;
            --text-color: #333;
            --highlight-color: #9a8c98;
            --button-color: #22223b;
            --button-text-color: #ffffff;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: var(--bg-color);
            color: var(--card-bg-color);
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }

        .header {
            font-size: 2.5rem;
            margin-bottom: 40px;
            text-align: center;
            color: var(--card-bg-color);
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            gap: var(--gap);
            justify-content: center;
            max-width: 1200px;
        }

        .pricing-card {
            background-color: var(--card-bg-color);
            padding: 20px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
            text-align: center;
            flex: 1 1;
        }

        .pricing-card h2 {
            margin: 10px 0;
            font-size: 1.5rem;
            color: var(--highlight-color);
        }

        .pricing-card p {
            color: var(--text-color);
        }

        .pricing-card .price {
            font-size: 2rem;
            margin: 10px 0;
            color: var(--highlight-color);
        }

        .pricing-card .cta {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 20px;
            background-color: var(--button-color);
            color: var(--button-text-color);
            text-decoration: none;
            border-radius: 5px;
        }

        @media (max-width: 767px) {
            .pricing-card {
                flex: 1 1 calc(50% - var(--gap));
            }

            .header {
                font-size: 2rem;
            }
        }

        @media (max-width: 480px) {
            .pricing-card {
                flex: 1 1 100%;
            }

            .header {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        Your plan, your choice.
    </div>
    <div class="container">
        <div class="pricing-card">
            <h2>Starter</h2>
            <p class="price">$49</p>
            <p>No setup fee</p>
            <p>Unlimited products</p>
            <p>Mobile storefront</p>
            <p>Mobile app</p>
            <a href="#" class="cta">Get Started</a>
        </div>
        <div class="pricing-card">
            <h2>Personal</h2>
            <p class="price">$99</p>
            <p>No setup fee </p>
            <p>Unlimited products</p>
            <p>Mobile storefront</p>
            <p>Mobile app</p>
            <a href="#" class="cta">Get Started</a>
        </div>
        <div class="pricing-card">
            <h2>Team</h2>
            <p class="price">$229</p>
            <p>No setup fee</p>
            <p>Unlimited products</p>
            <p>Mobile storefront</p>
            <p>Mobile app</p>
            <a href="#" class="cta">Get Started</a>
        </div>
    </div>
</body>
</html>
```

- **Mobile First**: Comienza con tarjetas que ocupan el 100% del ancho disponible en pantallas pequeñas.
- **Media Queries**: A medida que el ancho de la pantalla aumenta, las tarjetas se reorganizan en una cuadrícula de 2 columnas (para pantallas medianas) y 3 columnas (para pantallas grandes).
- **Flexbox**: Se utiliza para organizar las tarjetas de contenido en una cuadrícula flexible y responsiva.

Este ejemplo muestra cómo usar Flexbox y media queries para crear un layout de tabla de precios que se adapta a diferentes tamaños de pantalla, siguiendo las mejores prácticas de diseño responsivo y mobile-first.

## Formulario

---

Vamos a replicar el diseño de un formulario básico utilizando Flexbox, media queries y la metodología "mobile-first". A continuación, se presenta el HTML y CSS integrado para que puedas copiar y ver el funcionamiento directamente en tu navegador.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulario Flexbox</title>
    <style>
        :root {
            --bg-color: #e8e8e4;
            --card-bg-color: #ffffff;
            --text-color: #333;
            --highlight-color: #000;
            --input-border-color: #ccc;
            --input-focus-border-color: #333;
            --button-bg-color: #000;
            --button-text-color: #fff;
            --gap: 20px;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }

        .form-container {
            background-color: var(--card-bg-color);
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            max-width: 800px;
            width: 100%;
            text-align: center;
        }

        .form-container h2 {
            margin-bottom: 20px;
            font-size: 1.5rem;
        }

        .form-container input[type="email"] {
            width: 80%;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid var(--input-border-color);
            border-radius: 5px;
            font-size: 1rem;
            outline: none;
        }

        .form-container input[type="email"]:focus {
            border-color: var(--input-focus-border-color);
        }

        .form-container button {
            background-color: var(--button-bg-color);
            color: var(--button-text-color);
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            cursor: pointer;
        }

        .info-section {
            display: flex;
            flex-wrap: wrap;
            gap: var(--gap);
            justify-content: space-between;
            margin-top: 40px;
            max-width: 1200px;
            width: 100%;
        }

        .info-box {
            flex: 1 1 calc(33.333% - var(--gap));
            background-color: var(--card-bg-color);
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .info-box img {
            max-width: 50px;
            margin-bottom: 10px;
        }

        .info-box p {
            margin: 5px 0;
        }

        @media (max-width: 767px) {
            .info-box {
                flex: 1 1 calc(50% - var(--gap));
            }

            .form-container h2 {
                font-size: 1.25rem;
            }
        }

        @media (max-width: 480px) {
            .info-box {
                flex: 1 1 100%;
            }

            .form-container h2 {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="form-container">
        <h2>Sign up for Exclusive Access</h2>
        <input type="email" placeholder="Enter your email here">
        <button>SEND</button>
    </div>
    <div class="info-section">
        <div class="info-box">
            <img src="https://via.placeholder.com/50" alt="Free shipping">
            <p><strong>FREE shipping</strong></p>
            <p>All orders over $99</p>
        </div>
        <div class="info-box">
            <img src="https://via.placeholder.com/50" alt="3 days delivery">
            <p><strong>3 days delivery</strong></p>
            <p>Carefully packed with love</p>
        </div>
        <div class="info-box">
            <img src="https://via.placeholder.com/50" alt="Buy now, pay later">
            <p><strong>Buy now, pay later</strong></p>
            <p>With Karnos credit card</p>
        </div>
        <div class="info-box">
            <img src="https://via.placeholder.com/50" alt="Safe payment">
            <p><strong>Safe payment</strong></p>
            <p>Secure online payments</p>
        </div>
        <div class="info-box">
            <img src="https://via.placeholder.com/50" alt="Support 24/7">
            <p><strong>Support 24/7</strong></p>
            <p>(555) 555-5555</p>
        </div>
    </div>
</body>
</html>

```

- **Mobile First**: Comienza con elementos que ocupan el 100% del ancho disponible en pantallas pequeñas.
- **Media Queries**: A medida que el ancho de la pantalla aumenta, las cajas de información se reorganizan en una cuadrícula de 2 columnas (para pantallas medianas) y 3 columnas (para pantallas grandes).
- **Flexbox**: Se utiliza para organizar las cajas de información en una cuadrícula flexible y responsiva.
- **Formulario**: Incluye un campo de entrada de correo electrónico y un botón de envío, con estilos responsivos.

Este ejemplo muestra cómo usar Flexbox y media queries para crear un layout de formulario que se adapta a diferentes tamaños de pantalla, siguiendo las mejores prácticas de diseño responsivo y mobile-first.