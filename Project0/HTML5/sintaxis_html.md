<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Sintaxis de HTML

Las páginas web son esencialmente documentos de texto que contienen información estructurada mediante etiquetas HTML. Estas etiquetas indican al navegador cómo debe presentarse el contenido.

## Composición de una etiqueta HTML

---

Una etiqueta HTML tiene el siguiente formato

```html
<nombre-etiqueta nombre-atributo="valor-atributo">contenido</nombre-etiqueta>
```

La parte fundamental de una etiqueta HTML está compuesta por:

- **Apertura de la etiqueta**: `<nombre-etiqueta>`
- **Cierre de la etiqueta**: `</nombre-etiqueta>`

```html
<h1>Soy un título</h1>
<p>Soy un párrafo</p>
```

Es importante usar las etiquetas correctas, ya que los motores de búsqueda y otros sistemas automatizados utilizan estas etiquetas para entender y procesar el contenido de la página.

### Importancia del buen uso de etiquetas

El contenido debe estar encapsulado correctamente dentro de las etiquetas adecuadas.

```html
<h1>Soy un título</h1> <!-- Correcto -->
<p>Soy un título</p> <!-- Incorrecto -->
```

Utilizar etiquetas incorrectas puede afectar negativamente la accesibilidad y el SEO de la página.

## Atributos HTML

---

Las etiquetas HTML pueden tener atributos que proporcionan información adicional sobre el elemento o modifican su comportamiento. Los atributos se especifican en la etiqueta de apertura y suelen tener pares de nombre/valor, como `nombre="valor"`.

```html
<p id="nombre">Alberto Rivera</p>
```

En este ejemplo, la etiqueta `<p>` tiene un atributo `id` con el valor "nombre".

**Reglas para Atributos**

- Todos los elementos HTML pueden tener atributos.
- Los atributos proporcionan información adicional sobre los elementos.
- Los atributos siempre se especifican en la etiqueta de inicio.
- Los atributos generalmente vienen en pares de nombre/valor, como `nombre="valor"`.


## Comentarios en HTML

---

Los comentarios en HTML son útiles para dejar notas en el código que no serán visibles para los usuarios en el navegador.

```html
<!-- Esto es un comentario y el navegador no lo muestra -->
```

### Atajo de teclado para comentarios

- **Windows/Linux**: `Shift + Alt + A`
- **Mac**: `⌘K ⌘C`


Te recomendamos explorar las diferentes etiquetas HTML y crear documentos usando diversas etiquetas. Puedes consultar la referencia completa de HTML en [MDN Web Docs](https://developer.mozilla.org/es/docs/Web/HTML/Reference).

## Reto Coding

---

Crear un documento HTML que utilice una variedad de etiquetas, atributos y comentarios.

### **Instrucciones**:

1. Dentro de tu carpeta llamada `HTML` crea un archivo `sintax.html`.
2. En el archivo `index.html`, escribe la estructura básica de HTML e incluye varios elementos con atributos y comentarios.

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de HTML con Atributos y Comentarios</title>
</head>
<body>
    <h1 id="titulo-principal">Mi Primer Encabezado</h1>
    <p class="parrafo-introduccion">Este es mi primer párrafo.</p>
    <img src="imagen.jpg" alt="Descripción de la imagen">
    <a href="https://example.com" target="_blank">Enlace a Example.com</a>
    <!-- Este es un comentario que no será visible en el navegador -->
</body>
</html>
```

