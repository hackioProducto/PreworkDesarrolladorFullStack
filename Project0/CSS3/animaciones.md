<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Animaciones

Las animaciones en CSS nos permiten crear transiciones entre estilos de un elemento de nuestra página web. Estas transiciones se pueden crear utilizando la propiedad "animation" y sus sub-propiedades, y se pueden aplicar a cualquier elemento del DOM.

## **Definición de keyframes**

---

Para crear una animación en CSS, primero debemos definir un conjunto de estilos para el elemento en diferentes puntos del tiempo, estos estilos se llaman "keyframes". Para definir un conjunto de keyframes, utilizamos la regla "@keyframes". Por ejemplo, para definir una animación que cambie el color de fondo de un elemento de rojo a azul, podemos hacer lo siguiente:

```css
@keyframes cambiarColor {
  from {
    background-color: red;
  }
  to {
    background-color: blue;
  }
}

```

En este ejemplo, hemos definido un conjunto de keyframes llamado "cambiarColor" que cambia el color de fondo de rojo a azul. El "from" indica el estado inicial del elemento y el "to" indica el estado final.

También podemos definir keyframes en porcentajes. Por ejemplo, si queremos crear una animación que cambie el color de fondo de un elemento de rojo a azul en los primeros 50% y luego de azul a verde en los siguientes 50%, podemos hacer lo siguiente:

```css
@keyframes cambiarColor {
  0% {
    background-color: red;
  }
  50% {
    background-color: blue;
  }
  100% {
    background-color: green;
  }
}
```

En este ejemplo, hemos definido un conjunto de keyframes llamado "cambiarColor" que cambia el color de fondo de rojo a azul en los primeros 50% y luego de azul a verde en los siguientes 50%.

**Aplicación de la animación**

---

Una vez que hemos definido nuestros keyframes, podemos aplicarlos a un elemento utilizando la propiedad "animation". Por ejemplo, para aplicar la animación "cambiarColor" a un elemento con la clase "mi-elemento" durante 2 segundos, podemos hacer lo siguiente:

```css
.mi-elemento {
  animation: cambiarColor 2s;
}
```

En este ejemplo, hemos aplicado la animación "cambiarColor" al elemento con la clase "mi-elemento" durante 2 segundos.

**Control de la animación**

---

La propiedad "animation" tiene varias sub-propiedades que nos permiten controlar aspectos como la duración, el retraso, la cantidad de veces que se repite la animación, etc. Algunas de estas sub-propiedades son:

- "animation-duration": la duración de la animación en segundos o milisegundos.
- "animation-delay": el retraso antes de que comience la animación en segundos o milisegundos.
- "animation-iteration-count": la cantidad de veces que se repite la animación. Puede ser un número o "infinite" para repetir la animación indefinidamente.
- "animation-timing-function": la función de tiempo que se utiliza para controlar la velocidad de la animación.

Por ejemplo, podemos modificar nuestra animación anterior para que se repita indefinidamente y tenga un retraso de 1 segundo antes de comenzar de la siguiente manera:

```css
.mi-elemento {
  animation: cambiarColor 2s infinite;
  animation-delay: 1s;
}
```

En este ejemplo, hemos aplicado la animación "cambiarColor" al elemento con la clase "mi-elemento" durante 2 segundos, y hemos indicado que se repita indefinidamente y tenga un retraso de 1 segundo antes de comenzar.

## Ejemplos de Animaciones en CSS

---

A continuación, se presentan ejemplos prácticos de cómo crear y aplicar animaciones en CSS usando keyframes y la propiedad `animation`. Los ejemplos incluyen cambio de color, rotación, desplazamiento y cambio de opacidad.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplos de Animaciones en CSS</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          display: flex;
          flex-direction: column;
          align-items: center;
          gap: 20px;
          margin: 40px;
      }

      .mi-elemento {
          width: 100px;
          height: 100px;
          background-color: red;
          margin: 20px;
      }

      /* Cambio de color */
      @keyframes cambiarColor {
          from {
              background-color: red;
          }
          to {
              background-color: blue;
          }
      }

      .cambiar-color {
          animation: cambiarColor 2s;
      }

      /* Rotación */
      @keyframes rotar {
          from {
              transform: rotate(0deg);
          }
          to {
              transform: rotate(360deg);
          }
      }

      .rotar {
          animation: rotar 2s;
      }

      /* Desplazamiento */
      @keyframes desplazar {
          from {
              margin-left: 0px;
          }
          to {
              margin-left: 200px;
          }
      }

      .desplazar {
          animation: desplazar 2s;
      }

      /* Cambio de opacidad */
      @keyframes aparecer {
          from {
              opacity: 0;
          }
          to {
              opacity: 1;
          }
      }

      .aparecer {
          animation: aparecer 2s;
      }
    </style>
  </head>
  <body>
    <h1>Ejemplos de Animaciones en CSS</h1>

    <div class="mi-elemento cambiar-color"></div>
    <p>Cambio de color: de rojo a azul en 2 segundos</p>

    <div class="mi-elemento rotar"></div>
    <p>Rotación: 360 grados en 2 segundos</p>

    <div class="mi-elemento desplazar"></div>
    <p>Desplazamiento: 200 píxeles hacia la derecha en 2 segundos</p>

    <div class="mi-elemento aparecer"></div>
    <p>Cambio de opacidad: de 0 a 1 en 2 segundos</p>
  </body>
</html>
```

1. **Cambio de color**:
    - **Keyframes**: Define la animación `cambiarColor` que cambia el color de fondo de rojo a azul.
    - **Aplicación**: La clase `.cambiar-color` aplica esta animación durante 2 segundos al elemento.
    
2. **Rotación**:
    - **Keyframes**: Define la animación `rotar` que rota el elemento desde 0 grados a 360 grados.
    - **Aplicación**: La clase `.rotar` aplica esta animación durante 2 segundos al elemento.
    
3. **Desplazamiento**:
    - **Keyframes**: Define la animación `desplazar` que mueve el elemento 200 píxeles hacia la derecha.
    - **Aplicación**: La clase `.desplazar` aplica esta animación durante 2 segundos al elemento.
    
4. **Cambio de opacidad**:
    - **Keyframes**: Define la animación `aparecer` que cambia la opacidad del elemento de 0 a 1.
    - **Aplicación**: La clase `.aparecer` aplica esta animación durante 2 segundos al elemento.