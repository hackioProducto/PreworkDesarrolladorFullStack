<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Atributos comunes en HTML

HTML se compone de etiquetas que estructuran y presentan el contenido en una página web. Además, estas etiquetas pueden tener atributos que modifican su comportamiento o proporcionan información adicional.

## Atributo `id`

---

El atributo `id` se usa para identificar un elemento de manera única dentro de un documento HTML. Este identificador debe ser único en la página, lo que significa que no puede repetirse. Es muy útil para acceder y manipular elementos específicos con JavaScript.

```html
<div id="personal_info">
    <p>Alberto Rivera</p>
    <p>Desarrollador FullStack</p>
</div>
```

En este ejemplo, el `id` es "personal_info", que identifica de manera única al elemento `<div>`.

## Atributo `class`

---

El atributo `class` se usa para definir una clase que puede ser compartida por varios elementos. Esto permite aplicar los mismos estilos o comportamientos a múltiples elementos usando CSS o JavaScript.

```html
<div class="personal_container" id="personal_info">
    <p class="personal_text">Alberto Rivera</p>
    <p class="personal_text">Desarrollador FullStack</p>
</div>
```

En este ejemplo, ambos párrafos `<p>` tienen la clase "personal_text", lo que permite aplicar el mismo estilo a ambos.

**Uso de múltiples clases**. Un elemento puede tener varias clases separadas por espacios.

```html
<p class="personal_text name">Alberto Rivera</p>
<p class="personal_text job">Desarrollador FullStack</p>
```

## Atributo `lang`

---

El atributo `lang` se utiliza para definir el idioma del contenido del elemento. Esto ayuda a los motores de búsqueda y navegadores a entender el idioma del contenido.

```html
<!doctype html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo de Idioma</title>
</head>
<body>
    <p>Texto en español</p>
    <p lang="en">Text in English.</p>
    <p>Saludo en inglés: <span lang="en">hello</span>, que significa hola.</p>
</body>
</html>

```

<aside>
<img src="/icons/directions_gray.svg" alt="/icons/directions_gray.svg" width="40px" /> **Importancia del Atributo `lang`**

1. **Accesibilidad:** Los lectores de pantalla utilizan el atributo `lang` para determinar cómo pronunciar el texto correctamente. Si el idioma no está definido correctamente, puede llevar a una mala interpretación y experiencia de usuario.
2. **SEO:**Los motores de búsqueda utilizan el atributo `lang` para entender el idioma del contenido y presentarlo correctamente en los resultados de búsqueda. Esto puede ayudar a dirigir el tráfico adecuado a tu sitio web.
3. **Correcta representación:** Los navegadores pueden ajustar la representación del contenido basado en el idioma especificado, especialmente en casos de idiomas que se leen de derecha a izquierda (como el árabe o hebreo).
</aside>

## Atributo `translate`

---

El atributo `translate` en HTML se utiliza para indicar si el contenido de un elemento debe ser traducido o no. Esto es especialmente útil cuando hay palabras, términos técnicos o nombres propios que no deberían ser traducidos en las aplicaciones de traducción automática.

El atributo `translate` puede tener dos valores:

- `"yes"`: Indica que el contenido del elemento debe ser traducido.
- `"no"`: Indica que el contenido del elemento no debe ser traducido.

```html
<p>Hoy he comido un <span translate="no">Sandwich</span>.</p>
```

Por defecto si no se indica el atributo `translate` con el valor  “no” será traducido por los navegadores. Es habitual su uso en:

- Nombres Propios (Alberto)
- Marcas Registradas (Iphone)
- Términos Técnicos (WI FI)
- Palabras aceptadas en nuestro idioma (sandwich)

## Atributo `title`

---

El atributo `title` en HTML proporciona información adicional sobre un elemento. Esta información se muestra en un cuadro emergente (tooltip) cuando el usuario coloca el cursor sobre el elemento. El atributo `title` puede ser utilizado en cualquier elemento HTML y es una forma efectiva de proporcionar descripciones o detalles adicionales sin sobrecargar la interfaz visual.

```html
<div>
    <img src="logo.jpg" alt="logotipo" title="Es una imagen con el logotipo" />
</div>
```

En este ejemplo el atributo `title` se aplica a una imagen (`<img>`) y el texto "Es una imagen con el logotipo" aparecerá en un cuadro emergente cuando el usuario pase el cursor sobre la imagen.

Aquí tienes un ejemplo completo que muestra cómo usar el atributo `title` en varios elementos

```html
<!doctype html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo de Atributo Title</title>
</head>
<body>
    <h1 title="Este es el título principal">Bienvenido a mi página web</h1>
    <p title="Información adicional sobre este párrafo">Este es un párrafo de ejemplo.</p>
    <a href="https://www.ejemplo.com" title="Visita Ejemplo">Visita nuestro sitio web</a>
    <button title="Haz clic para enviar el formulario">Enviar</button>
    <div>
        <img src="logo.jpg" alt="logotipo" title="Es una imagen con el logotipo" />
    </div>
</body>
</html>
```

Consideraciones Importantes que debemos tener en cuenta para usar el atributo `title`

1. **Accesibilidad:** El atributo `title` puede mejorar la accesibilidad al proporcionar descripciones adicionales. Sin embargo, no debe ser el único medio de transmitir información importante, ya que algunos usuarios de tecnologías de asistencia pueden no tener acceso a los tooltips.
2. **Usabilidad:** Asegúrate de que los tooltips proporcionados por el atributo `title` sean claros y útiles. Evita usar demasiada información en el tooltip, ya que debe ser breve y fácil de entender.
3. **Compatibilidad:** Aunque el atributo `title` es ampliamente soportado, algunos navegadores móviles pueden no mostrar tooltips. Considera este comportamiento al diseñar tu contenido.

## Atributo `dir`

---

El atributo `dir` en HTML se utiliza para especificar la dirección del texto dentro de un elemento. Esto es particularmente útil para idiomas que se leen de derecha a izquierda, como el árabe o el hebreo. Los valores posibles para el atributo `dir` son:

- `ltr` (left-to-right): Para texto que se lee de izquierda a derecha.
- `rtl` (right-to-left): Para texto que se lee de derecha a izquierda.

```html
<p>Texto de izquierda a derecha.</p>
<p dir="rtl">Texto de derecha a izquierda.</p>
```

Pero su uso se verá más claro cuando en un documento tengamos textos con diferentes direcciones.

```html
<!doctype html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ejemplo de Dirección del Texto</title>
</head>
<body>
    <p>Texto de izquierda a derecha.</p>
    <p dir="rtl">هذا نص من اليمين إلى اليسار.</p>
    <p dir="rtl">שָׁלוֹם</p>
</body>
</html>

```

- El primer párrafo se muestra en español de izquierda a derecha.
- El segundo párrafo contiene texto en árabe, que se muestra de derecha a izquierda.
- El tercer párrafo contiene texto en hebreo, que también se muestra de derecha a izquierda.

También es útil en los texto mixtos, es decir un mismo párrafo que contiene diferentes idiomas.

```html
<!doctype html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Texto Mixto</title>
</head>
<body>
    <p>Este es un ejemplo de texto en inglés y <span dir="rtl">עִברִית</span> en el mismo párrafo.</p>
</body>
</html>

```

Consideraciones Importantes que debemos tener en cuenta para usar el atributo `dir` 

1. **Compatibilidad de idiomas:** El atributo `dir` es crucial para la correcta visualización de idiomas que se leen de derecha a izquierda. No usarlo puede resultar en una experiencia de lectura confusa para los usuarios de esos idiomas.
2. **Uso con otros atributos:** El atributo `dir` se puede combinar con otros atributos como `lang` para proporcionar más contexto sobre el idioma y la dirección del texto.
3. **Accesibilidad:** Definir correctamente la dirección del texto mejora la accesibilidad, especialmente para los usuarios de lectores de pantalla y otras tecnologías de asistencia.

## Atributo `data-*`

---

Los atributos con prefijo `data-` se utilizan para almacenar datos personalizados en los elementos HTML. Estos datos pueden ser utilizados por JavaScript para realizar operaciones dinámicas. *Por ello lo veremos con mayor profundidad cuando dominemos Javascript.

```html
<div id="compartir">
    <a href="https://twitter.com/mitweet" data-share="190">Twitter</a>
    <a href="https://www.facebook.com/mipost" data-share="340">Facebook</a>
</div>
```

## Atributo `accesskey`

---

El atributo `accesskey` se utiliza en HTML para definir un atajo de teclado que permite a los usuarios acceder rápidamente a un elemento específico de la página. Esto puede mejorar la accesibilidad y la eficiencia de navegación, especialmente para usuarios que prefieren o necesitan utilizar el teclado en lugar del ratón.

```html
<form>
    <input accesskey="N" placeholder="Nombre (ALT+N)" />
    <input accesskey="A" placeholder="Apellidos (ALT+A)" />
    <a accesskey="L" href="#">Enlace (ALT+L)</a>
    <button accesskey="B">Botón (ALT+B)</button>
</form>
```

- Cada elemento del formulario tiene un `accesskey` asignado.
- Al presionar `ALT` (o `ALT + SHIFT` en algunos navegadores) junto con la tecla especificada (`N`, `A`, `L`, `B`), el enfoque se moverá al elemento correspondiente.

## Atributo `style`

---

El atributo `style` se utiliza para aplicar estilos CSS directamente en un elemento HTML. Aunque es posible, no es la mejor práctica para proyectos grandes debido a la falta de separación de estilos y estructura.

```html
<p style="background: blue; color: whitesmoke;">Usando el atributo style</p>
```

El atributo `style` se usa para aplicar un fondo azul (`background: blue`) y un color de texto blanco ahumado (`color: whitesmoke`) al párrafo (`<p>`).

Consideraciones Importantes que debemos tener en cuenta para usar el atributo `style`

1. **Mantenimiento del código:** Usar el atributo `style` para aplicar estilos directamente en los elementos puede hacer que el código sea más difícil de mantener, especialmente en proyectos grandes. Es mejor usar hojas de estilo CSS externas o internas para una mejor separación de estilos y contenido.
2. **Reusabilidad:** Aplicar estilos en línea con el atributo `style` limita la reusabilidad de los estilos. Usar clases CSS permite aplicar el mismo estilo a múltiples elementos fácilmente.
3. **Prioridad de estilos:** Los estilos aplicados con el atributo `style` tienen una alta prioridad y pueden sobrescribir estilos definidos en hojas de estilo externas o internas.

<aside>
<img src="/icons/directions_gray.svg" alt="/icons/directions_gray.svg" width="40px" /> **Consejos y Práctica**

Te recomendamos que practiques creando documentos HTML utilizando estos atributos para familiarizarte con su uso. Aquí tienes un enlace a la referencia completa de HTML en [MDN Web Docs](https://developer.mozilla.org/es/docs/Web/HTML/Reference).

</aside>

## Reto Coding

---

Crea una página web que utilice una variedad de atributos para diferentes elementos.

### **Instrucciones**:

1. Ve a tu carpeta llamada `HTML`.
2. Dentro de esta carpeta, crea un archivo `atributes.html`.
3. En el archivo `atributes.html`, escribe la estructura básica de HTML y utiliza varios atributos en diferentes elementos.
    1. id
    2. class
    3. lang
    4. dir
    5. data-share
    6. style
    7. accesskey

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Atributos HTML</title>
</head>
<body>
    <h1 id="titulo_principal">Atributos HTML</h1>
    <p class="texto_informativo" lang="es">Este es un párrafo con información importante.</p>
    <p class="texto_informativo" lang="en">This is a paragraph with important information.</p>
    <div data-share="100" title="Se ha compartido 100 veces">Compartido</div>
    <img src="imagen.jpg" alt="Descripción de la imagen" style="width:100px; height:100px;" />
    <form>
        <input accesskey="N" placeholder="Nombre (ALT+N)" />
        <input accesskey="A" placeholder="Apellidos (ALT+A)" />
        <button accesskey="B">Enviar (ALT+B)</button>
    </form>
    <!-- Este es un comentario que no será visible en el navegador -->
</body>
</html>
```

## Contenido asociado
---
- [Video: Atributos HTML5](https://vimeo.com/845882512/42b7c87d09)
