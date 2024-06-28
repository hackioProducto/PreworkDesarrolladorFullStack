<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Display: Flex

Flexbox, o simplemente flex, es un sistema de diseño flexible que facilita la disposición de los elementos en una página web. A continuación, exploraremos las características y elementos básicos de Flexbox y proporcionaremos ejemplos prácticos en un solo archivo HTML para ayudarte a comprender cómo funciona.

## Características y Elementos Básicos de Flexbox

---

1. **Contenedor Flex**: El elemento padre que contiene los elementos flexibles.
    - **Eje principal**: Por defecto, es el eje horizontal (x).
    - **Eje secundario**: Perpendicular al eje principal; por defecto, es el eje vertical (y).
    
2. **Elemento Flex**: Los elementos hijos que están contenidos dentro del contenedor flex.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo Básico de Flexbox</title>
    <style>
      .container {
          display: flex;
          border: 2px solid black;
          padding: 10px;
      }

      .hijo {
          width: 100px;
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo">1</div>
      <div class="hijo">2</div>
      <div class="hijo">3</div>
    </div>
  </body>
</html>
```

## Propiedades de Flexbox

---

**Flex Direction**: La propiedad `flex-direction` define la dirección del eje principal.

- **row**: Eje horizontal (por defecto).
- **row-reverse**: Eje horizontal invertido.
- **column**: Eje vertical.
- **column-reverse**: Eje vertical invertido.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Flex Direction</title>
    <style>
      .container {
          display: flex;
          flex-direction: column; /* Cambiar a row, row-reverse, column, column-reverse */
          border: 2px solid black;
          padding: 10px;
      }

      .hijo {
          width: 100px;
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo">1</div>
      <div class="hijo">2</div>
      <div class="hijo">3</div>
    </div>
  </body>
</html>
```

**Flex Wrap**: La propiedad `flex-wrap` controla si los elementos flexibles deben forzar una sola línea o pueden envolverse en varias líneas.

- **nowrap**: Una sola línea (por defecto).
- **wrap**: Envolvimiento en varias líneas.
- **wrap-reverse**: Envolvimiento en varias líneas en orden inverso.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Flex Wrap</title>
    <style>
      .container {
          display: flex;
          flex-wrap: wrap; /* Cambiar a nowrap, wrap, wrap-reverse */
          border: 2px solid black;
          padding: 10px;
      }

      .hijo {
          width: 100px;
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo">1</div>
      <div class="hijo">2</div>
      <div class="hijo">3</div>
      <div class="hijo">4</div>
      <div class="hijo">5</div>
      <div class="hijo">6</div>
    </div>
  </body>
</html>
```

**Flex Flow**: La propiedad `flex-flow` es un atajo para definir `flex-direction` y `flex-wrap`.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Flex Flow</title>
    <style>
      .container {
          display: flex;
          flex-flow: column wrap; /* Cambiar a combinaciones de flex-direction y flex-wrap */
          border: 2px solid black;
          padding: 10px;
      }

      .hijo {
          width: 100px;
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo">1</div>
      <div class="hijo">2</div>
      <div class="hijo">3</div>
      <div class="hijo">4</div>
      <div class="hijo">5</div>
      <div class="hijo">6</div>
    </div>
  </body>
</html>
```

**Justify Content** : La propiedad `justify-content` alinea los elementos hijos a lo largo del eje principal.

- **flex-start**: Alínea los hijos al inicio del eje principal.
- **flex-end**: Alínea los hijos al final del eje principal.
- **center**: Alínea los hijos al centro del eje principal.
- **space-between**: Distribuye los hijos dejando espacio entre ellos.
- **space-around**: Deja espacio alrededor de los hijos.
- **space-evenly**: Deja el mismo espacio alrededor de cada hijo.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Justify Content</title>
    <style>
      .container {
          display: flex;
          justify-content: center; /* Cambiar a flex-start, flex-end, center, space-between, space-around, space-evenly */
          border: 2px solid black;
          padding: 10px;
      }

      .hijo {
          width: 100px;
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo">1</div>
      <div class="hijo">2</div>
      <div class="hijo">3</div>
    </div>
  </body>
</html>
```

**Align Items:** La propiedad `align-items` alinea los elementos hijos a lo largo del eje secundario.

- **flex-start**: Alínea los hijos al inicio del eje secundario.
- **flex-end**: Alínea los hijos al final del eje secundario.
- **center**: Alínea los hijos al centro del eje secundario.
- **stretch**: Estira los hijos para llenar el contenedor.
- **baseline**: Alínea los hijos según la línea base de su contenido.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Align Items</title>
    <style>
      .container {
          display: flex;
          align-items: center; /* Cambiar a flex-start, flex-end, center, stretch, baseline */
          border: 2px solid black;
          padding: 10px;
          height: 300px; /* Ajustar para observar mejor la alineación */
      }

      .hijo {
          width: 100px;
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo">1</div>
      <div class="hijo">2</div>
      <div class="hijo">3</div>
    </div>
  </body>
</html>
```

**Align Content**: La propiedad `align-content` controla el espacio entre las líneas del contenedor flex cuando hay múltiples líneas.

- **flex-start**: Agrupa los ítems al inicio del eje principal.
- **flex-end**: Agrupa los ítems al final del eje principal.
- **center**: Agrupa los ítems al centro del eje principal.
- **space-between**: Agrupa los ítems dejando espacio entre ellos.
- **space-around**: Deja espacio alrededor de los ítems.
- **stretch**: Estira los ítems para llenar el espacio disponible.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Align Content</title>
    <style>
      .container {
          display: flex;
          flex-wrap: wrap;
          align-content: center; /* Cambiar a flex-start, flex-end, center, space-between, space-around, stretch */
          border: 2px solid black;
          padding: 10px;
          height: 300px; /* Ajustar para observar mejor la alineación */
      }

      .hijo {
          width: 100px;
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo">1</div>
      <div class="hijo">2</div>
      <div class="hijo">3</div>
      <div class="hijo">4</div>
      <div class="hijo">5</div>
      <div class="hijo">6</div>
    </div>
  </body>
</html>
```

**Align Self**: La propiedad `align-self` permite alinear un elemento hijo de forma diferente a los demás.

```css
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Align Self</title>
    <style>
        .container {
            display: flex;
            align-items: center; /* Alineación por defecto */
            border: 2px solid black;
            padding: 10px;
            height: 300px; /* Ajustar para observar mejor la alineación */
        }

        .hijo {
            width: 100px;
            height: 100px;
            background-color: blueviolet;
            color: whitesmoke;
            margin: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .hijo.flex-start {
            align-self: flex-start; /* Alineación individual */
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="hijo">1</div>
        <div class="hijo">2</div>
        <div class="hijo flex-start">3</div>
        <div class="hijo">4</div>
    </div>
</body>
</html>

```

**Flex Grow**: La propiedad `flex-grow` define la capacidad de un elemento para crecer si es necesario.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Flex Grow</title>
    <style>
      .container {
          display: flex;
          border: 2px solid black;
          padding: 10px;
      }

      .hijo {
          width: 100px;
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }

      .hijo.flex-grow {
          flex-grow: 1; /* Elemento crece para llenar el espacio disponible */
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo">1</div>
      <div class="hijo flex-grow">2</div>
      <div class="hijo">3</div>
    </div>
  </body>
</html>
```

**Flex Shrink**: La propiedad `flex-shrink` define la capacidad de un elemento para reducir su tamaño si es necesario.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Flex Shrink</title>
    <style>
      .container {
          display: flex;
          border: 2px solid black;
          padding: 10px;
          width: 300px; /* Reducir el ancho del contenedor para observar el efecto */
      }

      .hijo {
          width: 100px;
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }

      .hijo.flex-shrink {
          flex-shrink: 1; /* Elemento se reduce para adaptarse al espacio disponible */
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo flex-shrink">1</div>
      <div class="hijo">2</div>
      <div class="hijo">3</div>
    </div>
  </body>
</html>
```

**Flex Basis**: La propiedad `flex-basis` define el tamaño inicial de un elemento antes de que se distribuya el espacio restante.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Flex Basis</title>
    <style>
      .container {
          display: flex;
          border: 2px solid black;
          padding: 10px;
      }

      .hijo {
          flex-basis: 50px; /* Cambiar tamaño base de los elementos */
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }

      .hijo.flex-basis {
          flex-basis: 150px; /* Tamaño base específico para este elemento */
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo">1</div>
      <div class="hijo flex-basis">2</div>
      <div class="hijo">3</div>
    </div>
  </body>
</html>
```

**Flex (Atajo):** La propiedad `flex` es un atajo para definir `flex-grow`, `flex-shrink` y `flex-basis`.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Flex (Atajo)</title>
    <style>
      .container {
          display: flex;
          border: 2px solid black;
          padding: 10px;
      }

      .hijo {
          flex: 1 2 100px; /* flex-grow, flex-shrink, flex-basis */
          height: 100px;
          background-color: blueviolet;
          color: whitesmoke;
          margin: 10px;
          display: flex;
          justify-content: center;
          align-items: center;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="hijo">1</div>
      <div class="hijo">2</div>
      <div class="hijo">3</div>
    </div>
  </body>
</html>
```

## Recursos Adicionales

---

Para practicar y aprender más sobre Flexbox, aquí tienes algunos recursos adicionales:

[Flexbox Froggy](https://flexboxfroggy.com/#es)

[Flexbox Defense](http://www.flexboxdefense.com/)

[Play Flex Box Adventure - CSS Game to Learn Flexbox](https://codingfantasy.com/games/flexboxadventure)

[A Complete Guide to Flexbox | CSS-Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

**Resumen**

1. Qué es Flexbox, qué nos ofrece y sus propiedades más esenciales.
2. Propiedades específicas para alinear elementos.
3. Las propiedades con las que podremos maquetar elementos hijos concretos dentro de los contenedores padres.
4. Recursos extras con los que podéis completar el aprendizaje de manera divertida!
