<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Clave:valor

Antes de empezar a desarrollar los estilos en un archivo CSS, es importante entender la estructura y los elementos que lo componen.

## Estructura y reglas del código CSS

---

En un archivo CSS, la estructura básica de una regla se ve así:

```css
selector {
	propiedad: valor; /* regla */
	propiedad: valor; /* regla */
	propiedad: valor; /* regla */
}
```

- **Selector:** El elemento del documento HTML al que se aplicará el estilo.
- **Propiedad:** La característica del elemento que se va a modificar.
- **Valor:** La asignación que cambiará el comportamiento de la propiedad.

Cada par de propiedad y valor se llama **regla**, y es importante finalizar cada regla con un punto y coma.

## Ejemplo práctico aplicando reglas

---

Veamos un ejemplo sencillo con un documento HTML y una hoja de estilos enlazada:

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
      <h1>Hola, soy un título</h1>
    </header>
  </body>
</html>
```

```css
h1 {
  color: crimson;
}
```

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/35501d42-9e1c-449b-b408-af021f62cb70/Captura_de_pantalla_2022-11-29_a_las_16.04.38.png](./Imagenes/clave_valor.png)

En este ejemplo, el selector es `h1`, y la regla define la propiedad `color` con el valor `crimson`. Esto cambia el color del texto del `h1` al color especificado.

## Reto Coding

---

Vamos a practicar aplicando estilos a un documento HTML dado. Aquí está el HTML de ejemplo:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Movies</title>
  </head>
  <body>
    <header>
      <h1>Movies</h1>
    </header>
    <main>
      <p>Best movies of 2022 ranked:</p>
      <ol>
        <li>The Quiet Girl</li>
        <li>Happening</li>
        <li>Come from Away</li>
        <li>Aftersun</li>
        <li>Hellbender</li>
      </ol>
    </main>
  </body>
</html>
```

### Instrucciones:

1. Crea un archivo `style.css` en el mismo directorio que tu archivo HTML.
2. Aplica los siguientes estilos en `style.css`:
    - La etiqueta `p` debe tener el color `skyblue`.
    - La etiqueta `h1` debe tener el color `white`.
    - La etiqueta `li` debe tener el color `whitesmoke`.
    - La etiqueta `body` debe tener el color de fondo `rgb(52, 52, 52)`.

**Solución Reto Coding**

```css
body {
  background-color: rgb(52, 52, 52);
  color: whitesmoke; /* Estilo adicional para asegurar legibilidad */
}

h1 {
  color: white;
}

p {
  color: skyblue;
}

li {
  color: whitesmoke;
}
```

1. Asegúrate de que el archivo `style.css` está enlazado correctamente en el HTML usando la etiqueta `<link>`.
2. Abre el archivo `index.html` en tu navegador para ver los cambios aplicados por `style.css`.

Después de aplicar los estilos, tu página web debería reflejar los cambios especificados en el archivo CSS. Aquí tienes el resultado visual esperado:

- El fondo de la página debe ser `rgb(52, 52, 52)`.
- El texto de `h1` debe ser `white`.
- El texto de `p` debe ser `skyblue`.
- Los elementos de la lista `li` deben ser `whitesmoke`.

¡Bien hecho! Ahora has aprendido cómo aplicar estilos CSS a un documento HTML utilizando selectores, propiedades y valores.

## Contenido asociado
---
- [Video: Clave: valor](https://vimeo.com/819140139/95cd8f9120)
