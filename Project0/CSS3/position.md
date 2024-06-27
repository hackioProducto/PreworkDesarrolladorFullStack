<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Position

En CSS, el posicionamiento se refiere a cómo se ubican los elementos en una página web. Existen varios tipos de posicionamiento que determinan la ubicación de los elementos y su comportamiento en el flujo del documento. Aquí se explican los diferentes tipos de posicionamiento con ejemplos para que sea más fácil de entender para los principiantes.

## Posicionamiento `static`

---

`static` es el valor por defecto para la propiedad `position`. Los elementos se posicionan según el flujo normal del documento.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .box {
        width: 100px;
        height: 100px;
        background: lightblue;
        border: 1px solid black;
        margin: 10px;
      }
    </style>
  </head>
  <body>
    <div class="box">Caja 1</div>
    <div class="box">Caja 2</div>
    <div class="box">Caja 3</div>
  </body>
</html>
```

**Uso típico**: La mayoría de los elementos en una página web utilizan el posicionamiento `static` de forma predeterminada. Es adecuado para contenido que sigue el flujo normal del documento.

## Posicionamiento `relative`

---

**Definición**: `relative` posiciona los elementos de manera relativa a su posición original. Se pueden usar las propiedades `top`, `bottom`, `left`, y `right` para ajustar la posición del elemento.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .box {
        width: 100px;
        height: 100px;
        background: lightblue;
        border: 1px solid black;
        margin: 10px;
      }
      #relative-box {
        position: relative;
        top: 20px;
        left: 30px;
        background: lightcoral;
      }
    </style>
  </head>
  <body>
    <div class="box">Caja 1</div>
    <div id="relative-box" class="box">Caja 2 (relative)</div>
    <div class="box">Caja 3</div>
  </body>
</html>
```

**Uso típico**: El posicionamiento `relative` es útil cuando se necesita ajustar ligeramente la posición de un elemento sin sacarlo del flujo normal del documento.

## Posicionamiento `absolute`

---

**Definición**: `absolute` posiciona los elementos en relación con el primer contenedor ancestro que tenga un posicionamiento diferente de `static`. Si no hay un contenedor así, se posiciona en relación con el elemento `<body>`.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .container {
        position: relative;
        width: 300px;
        height: 200px;
        background: lightgrey;
        border: 1px solid black;
      }
      .box {
        position: absolute;
        width: 100px;
        height: 100px;
        background: lightblue;
        border: 1px solid black;
      }
      #absolute-box {
        top: 50px;
        left: 50px;
        background: lightcoral;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="box">Caja 1</div>
      <div id="absolute-box" class="box">Caja 2 (absolute)</div>
    </div>
  </body>
</html>
```

**Uso típico**: `absolute` es útil para colocar elementos en posiciones específicas dentro de un contenedor posicionado. Se usa frecuentemente en menús desplegables y modales.

## Posicionamiento `fixed`

---

**Definición**: `fixed` posiciona los elementos de manera fija en relación con la ventana del navegador. El elemento permanece en la misma posición aunque se haga scroll.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .box {
        width: 100px;
        height: 100px;
        background: lightblue;
        border: 1px solid black;
        margin: 10px;
      }
      #fixed-box {
        position: fixed;
        top: 20px;
        right: 20px;
        background: lightcoral;
      }
    </style>
  </head>
  <body>
    <div class="box">Caja 1</div>
    <div class="box">Caja 2</div>
    <div class="box">Caja 3</div>
    <div id="fixed-box" class="box">Caja 4 (fixed)</div>
    <div class="box">Caja 5</div>
    <div class="box">Caja 6</div>
  </body>
</html>
```

**Uso típico**: `fixed` es útil para elementos que deben permanecer visibles en la pantalla, como barras de navegación fija, botones de ayuda o anuncios.

## Posicionamiento `sticky`

---

**Definición**: `sticky` combina características de `relative` y `fixed`. El elemento se comporta como `relative` hasta que alcanza un punto específico en la ventana del navegador, momento en el cual se comporta como `fixed`.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .box {
        width: 100px;
        height: 100px;
        background: lightblue;
        border: 1px solid black;
        margin: 10px;
      }
      #sticky-box {
        position: -webkit-sticky; /* Safari */
        position: sticky;
        top: 10px;
        background: lightcoral;
      }
    </style>
  </head>
  <body>
    <div class="box">Caja 1</div>
    <div class="box">Caja 2</div>
    <div id="sticky-box" class="box">Caja 3 (sticky)</div>
    <div class="box">Caja 4</div>
    <div class="box">Caja 5</div>
    <div class="box">Caja 6</div>
  </body>
</html>
```

**Uso típico**: `sticky` es útil para elementos que deben estar visibles mientras el usuario hace scroll, como barras de navegación o encabezados de sección.

## Propiedades `top`, `bottom`, `left` y `right`

---

Las propiedades `top`, `bottom`, `left` y `right` en CSS se utilizan para ajustar la posición de los elementos cuando se usa un tipo de posicionamiento que no sea `static` (`relative`, `absolute`, `fixed`, `sticky`). A continuación, se explican cada una de estas propiedades con ejemplos detallados.

**Propiedad `top` :** La propiedad `top` especifica la distancia entre el borde superior de un elemento y el borde superior de su contenedor de referencia.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .box {
        position: relative;
        width: 100px;
        height: 100px;
        background: lightblue;
        border: 1px solid black;
        top: 20px;
      }
    </style>
  </head>
  <body>
    <div class="box">Caja con top</div>
  </body>
</html>
```

**Uso típico**: Ajustar la posición de un elemento un poco más arriba o abajo de su ubicación original en el flujo del documento.

**Propiedad `bottom`**: La propiedad `bottom` especifica la distancia entre el borde inferior de un elemento y el borde inferior de su contenedor de referencia.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .container {
        position: relative;
        width: 300px;
        height: 200px;
        background: lightgrey;
        border: 1px solid black;
      }
      .box {
        position: absolute;
        width: 100px;
        height: 100px;
        background: lightblue;
        border: 1px solid black;
        bottom: 20px;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="box">Caja con bottom</div>
    </div>
  </body>
</html>
```

**Uso típico**: Colocar un elemento en la parte inferior de su contenedor.

**Propiedad `left`**: La propiedad `left` especifica la distancia entre el borde izquierdo de un elemento y el borde izquierdo de su contenedor de referencia.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .container {
        position: relative;
        width: 300px;
        height: 200px;
        background: lightgrey;
        border: 1px solid black;
      }
      .box {
        position: absolute;
        width: 100px;
        height: 100px;
        background: lightblue;
        border: 1px solid black;
        left: 50px;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="box">Caja con left</div>
    </div>
  </body>
</html>
```

**Uso típico**: Colocar un elemento a una distancia específica desde el borde izquierdo de su contenedor.

**Propiedad `right`**: La propiedad `right` especifica la distancia entre el borde derecho de un elemento y el borde derecho de su contenedor de referencia.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .box {
        position: fixed;
        width: 100px;
        height: 100px;
        background: lightblue;
        border: 1px solid black;
        right: 20px;
      }
    </style>
  </head>
  <body>
    <div class="box">Caja con right</div>
  </body>
</html>
```

**Uso típico**: Colocar un elemento en la parte derecha de la ventana del navegador, independientemente del scroll.

## **Combinaciones y Usos Comunes**

---

Centrar un Elemento Absolutamente Posicionado

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      .container {
        position: relative;
        width: 300px;
        height: 300px;
        background: lightgrey;
        border: 1px solid black;
      }
      .box {
        position: absolute;
        width: 100px;
        height: 100px;
        background: lightblue;
        border: 1px solid black;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="box">Centrado</div>
    </div>
  </body>
</html>
```

Sticky Header

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      header {
        position: sticky;
        top: 0;
        background: lightblue;
        padding: 10px;
        border: 1px solid black;
      }
      section {
        height: 200vh;
      }
    </style>
  </head>
  <body>
    <header>Este es un encabezado sticky</header>
    <section>
      <p>Contenido de la página...</p>
    </section>
  </body>
</html>
```

**Uso típico**: Un encabezado o menú que permanece en la parte superior de la ventana del navegador mientras el usuario hace scroll.

<aside>
<img src="/icons/directions_gray.svg" alt="/icons/directions_gray.svg" width="40px" /> **Resumen**

- **`top`**: Ajusta la posición desde el borde superior del contenedor.
- **`bottom`**: Ajusta la posición desde el borde inferior del contenedor.
- **`left`**: Ajusta la posición desde el borde izquierdo del contenedor.
- **`right`**: Ajusta la posición desde el borde derecho del contenedor.

Estas propiedades son fundamentales para el control preciso del posicionamiento de los elementos en una página web, permitiendo diseños flexibles y dinámicos.

</aside>

## Propiedad `z-index`

---

La propiedad `z-index` en CSS controla la superposición de los elementos en el eje Z (profundidad). Esta propiedad determina el orden de apilamiento de los elementos posicionados (`relative`, `absolute`, `fixed`, `sticky`), es decir, cuál elemento se coloca delante o detrás de otro. Un valor más alto de `z-index` indica que el elemento estará más adelante en la pila de apilamiento.

Reglas Básicas de `z-index` :

1. **Aplica Solo a Elementos Posicionados**: La propiedad `z-index` solo funciona en elementos con una posición distinta de `static`.
2. **Valores**: Puede tomar valores enteros (positivos o negativos) o `auto`. Los valores más altos se apilan encima de los más bajos.

### 

Vamos a crear un ejemplo donde tres cajas se superponen usando diferentes valores de `z-index`.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de z-index</title>
    <style>
      .container {
          position: relative;
          width: 300px;
          height: 300px;
          background: lightgrey;
      }

      .box {
          position: absolute;
          width: 100px;
          height: 100px;
          border: 1px solid black;
      }

      .red {
          background: red;
          top: 50px;
          left: 50px;
          z-index: 1;
      }

      .green {
          background: green;
          top: 80px;
          left: 80px;
          z-index: 2;
      }

      .blue {
          background: blue;
          top: 110px;
          left: 110px;
          z-index: 3;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="box red">Rojo (z-index: 1)</div>
      <div class="box green">Verde (z-index: 2)</div>
      <div class="box blue">Azul (z-index: 3)</div>
    </div>
  </body>
</html>
```

En este ejemplo, la caja azul con `z-index: 3` estará delante de las cajas verde y roja. La caja verde con `z-index: 2` estará detrás de la azul, pero delante de la roja. La caja roja con `z-index: 1` estará detrás de las otras dos.

Uso Común de `z-index` :

1. **Ventanas Modales y Diálogos**: Asegurarse de que los diálogos modales se superpongan a otros contenidos.
2. **Menús Desplegables**: Garantizar que los menús desplegables se muestren por encima del contenido principal.
3. **Banners y Notificaciones**: Mostrar banners o notificaciones por encima del contenido de la página.

## Ejemplo de Menú Desplegable

---

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Menú Desplegable</title>
    <style>
      .menu {
          position: relative;
          width: 200px;
          background: lightblue;
          padding: 10px;
          border: 1px solid black;
      }

      .dropdown {
          position: absolute;
          top: 100%;
          left: 0;
          width: 100%;
          background: lightcoral;
          display: none;
          z-index: 10;
          border: 1px solid black;
      }

      .menu:hover .dropdown {
          display: block;
      }

      .content {
          margin-top: 50px;
          padding: 10px;
          background: lightgrey;
          height: 150px;
      }
    </style>
  </head>
  <body>
    <div class="menu">
      Menú
      <div class="dropdown">
        Item 1<br />
        Item 2<br />
        Item 3
      </div>
    </div>
    <div class="content">Contenido principal</div>
  </body>
</html>
```

En este ejemplo, el menú desplegable (`.dropdown`) se muestra sobre el contenido principal (`.content`) gracias a su `z-index: 10`.

## Ejemplo de Ventana Modal

---

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Ejemplo de Ventana Modal</title>
    <style>
      .container {
          position: relative;
          width: 100%;
          height: 100vh;
          background: lightgrey;
      }

      .modal {
          position: fixed;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
          width: 300px;
          height: 200px;
          background: white;
          border: 1px solid black;
          box-shadow: 0 4px 8px rgba(0,0,0,0.1);
          z-index: 100;
      }

      .backdrop {
          position: fixed;
          top: 0;
          left: 0;
          width: 100%;
          height: 100%;
          background: rgba(0,0,0,0.5);
          z-index: 99;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="modal">Esta es una ventana modal</div>
      <div class="backdrop"></div>
    </div>
  </body>
</html>
```

En este ejemplo, la ventana modal (`.modal`) tiene un `z-index: 100` para asegurarse de que se superpone al fondo (`.backdrop`), que tiene un `z-index: 99`. La superposición adecuada asegura que el modal se vea por encima del fondo sombreado.

**Resumen**

- **`z-index`**: Controla el orden de apilamiento de los elementos posicionados.
- **Valores**: Enteros (positivos o negativos), donde los valores más altos se apilan encima de los valores más bajos.
- **Requiere Posicionamiento**: Solo funciona en elementos con `position` distinta de `static`.

## Contenido asociado
---
- [Video: Position](https://vimeo.com/742971406/146f041da2)
