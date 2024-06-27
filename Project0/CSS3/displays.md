<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Displays

Es importante entender que cada elemento HTML en una página web es una caja rectangular. Todos los elementos, sin importar su apariencia, son representados como rectángulos por el navegador. No existen elementos triangulares, redondos o poligonales. Esta es una de las bases del modelo de cajas de CSS.

## Elementos en Línea e Elementos en Bloque

---

- **Elementos en Línea (Inline)**: Se colocan uno al lado del otro horizontalmente. Ocupan solo el ancho necesario para su contenido, no todo el ancho disponible. Ejemplos comunes de elementos en línea son `<span>`, `<a>`, y `<img>`.
- **Elementos en Bloque (Block)**: Ocupan toda la anchura disponible y se apilan uno debajo del otro. Ejemplos comunes de elementos en bloque son `<div>`, `<h1>`, `<p>`, y `<section>`.

## Modificando el Comportamiento con la Propiedad `display`

---

La propiedad `display` permite cambiar el comportamiento por defecto de los elementos. Aquí están los valores más comunes:

- **block**: Hace que el elemento ocupe toda la anchura disponible y se apile verticalmente.
- **inline**: Adapta el ancho del elemento al contenido. No tiene en cuenta los valores de `width` o `height`.
- **inline-block**: Combina los dos anteriores, permitiendo establecer `width` y `height` mientras el elemento sigue comportándose en línea.
- **flex**: Utiliza un modelo de cajas flexibles, muy útil para diseños responsivos.
- **grid**: Utiliza un modelo basado en cuadrículas, ideal para diseños complejos.
- **contents**: Elimina la caja del elemento, pero mantiene los hijos en el flujo de diseño. Útil en ciertas manipulaciones con `flex` o `grid`.
- **none**: Oculta el elemento, similar a `visibility: hidden`, pero también elimina el espacio ocupado por el elemento en el flujo del documento.

## Demostración Display

---

Vamos a utilizar un ejemplo sencillo para demostrar cómo diferentes valores de la propiedad `display` afectan el comportamiento de los elementos. Aquí tienes el HTML y CSS básico. Luego, cambiarás el valor de `display` en el CSS para ver los diferentes efectos.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ejemplo de Display</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <span class="box">1</span>
    <span class="box">2</span>
    <span class="box">3</span>
  </div>
</body>
</html>
```

```css
.container {
  margin: 0;
  padding: 0;
  display: block;
  background-color: crimson;
}

.box {
  background-color: steelblue;
  width: 100px;
  height: 50px;
  padding: 30px;
  text-align: center;
  margin: 10px 10px;
  list-style-type: none;
  color: white;
  font-size: 20px;
}
```

## Cambiando el `display`

---

```css
.container {
  display: block;
}
```

**Resultado**: El contenedor `.container` ocupa todo el ancho disponible y los elementos `.box` se apilan uno debajo del otro.

```css
.container {
  display: inline;
}
```

**Resultado**: El contenedor `.container` ocupa solo el espacio necesario para sus contenidos. Los elementos `.box` se apilan uno al lado del otro en línea, ignorando los valores de `width` y `height`.

```css

.container {
  display: inline-block;
}
```

**Resultado**: El contenedor `.container` se comporta como un elemento en línea, pero permite que los elementos `.box` respeten los valores de `width` y `height`, apilándose en línea.

```css
.container {
  display: flex;
}
```

**Resultado**: Los elementos `.box` se organizan en una fila (o columna, si se especifica), utilizando el modelo de cajas flexibles. Esto permite un control más sofisticado sobre la disposición de los elementos hijos.

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```

**Resultado**: Los elementos `.box` se organizan en una cuadrícula con tres columnas iguales. Esto permite un control preciso sobre la disposición en dos dimensiones.

**Resumen**

Cambiando el valor de `display`, puedes controlar cómo los elementos se comportan y se disponen en la página. Aquí hay una tabla resumen de los diferentes comportamientos:

| display | Descripción |
| --- | --- |
| block | Ocupa todo el ancho disponible, elementos se apilan verticalmente. |
| inline | Ocupa solo el espacio necesario, elementos se apilan horizontalmente. |
| inline-block | Combina características de block e inline, respetando width y height. |
| flex | Organiza elementos en una fila o columna flexible. |
| grid | Organiza elementos en una cuadrícula bidimensional. |
