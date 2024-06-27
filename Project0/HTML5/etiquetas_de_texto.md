<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Etiquetas de texto

Las etiquetas de texto en HTML son esenciales para dar formato y significado al contenido. A continuación, se detallan las etiquetas más comunes y cómo se utilizan.

## Etiquetas comunes de texto

---

| Etiqueta | Descripción |
| --- | --- |
| <strong> | Marca el texto en negrita y tiene importancia semántica. |
| <em> | Enfatiza el texto en cursiva con importancia semántica. |
| <mark> | Resalta el texto como con un rotulador. |
| <i> | Texto en cursiva para tono alternativo o estilo. |
| <b> | Texto en negrita sin importancia semántica. |
| <u> | Texto subrayado. |
| <s> | Texto tachado. |
| <span> | Fragmento de texto sin significado semántico. |
| <cite> | Cita obras, libros, etc. |
| <del> | Texto eliminado. |
| <ins> | Texto insertado. |
1. **`<strong>`** y **`<b>`**: `<strong>`: Marca el texto en negrita y se utiliza para dar énfasis importante al texto. Tiene significado semántico, lo que ayuda a los lectores de pantalla a interpretar mejor el contenido. `<b>`: Marca el texto en negrita, pero sin importancia semántica. Solo cambia el aspecto visual.
    
    ```html
    <p>Esta parte es <strong>muy importante.</strong></p>
    <p>Esta parte ni me va ni me <b>viene</b></p>
    
    ```
    
2. **`<em>`** y **`<i>`**: `<em>`: Enfatiza el texto, mostrándolo en cursiva. Tiene significado semántico `<i>`: Muestra el texto en cursiva para tono alternativo o estilo, sin importancia semántica.
    
    ```html
    htmlCopiar código
    <p>Me gustaría hacer un <em>énfasis</em> especial en este punto.</p>
    <p>Esta parte es <i>itálica</i></p>
    
    ```
    
3. **`<mark>`**: Resalta el texto como si estuviera marcado con un rotulador.
    
    ```html
    htmlCopiar código
    <p>Esta parte quiero que esté <mark>subrayada</mark></p>
    
    ```
    
4. **`<u>`**: Subraya el texto.
    
    ```html
    htmlCopiar código
    <p>Si escribo burro con v es <u>vurro</u></p>
    
    ```
    
5. **`<s>`**: Tacha el texto, indicando que ya no es relevante o que se ha eliminado.
    
    ```html
    htmlCopiar código
    <p>Estaba yo pensando... que igual esto no es tan <s>importante.</s></p>
    
    ```
    
6. **`<span>`**: Utilizado para aplicar estilos a partes específicas del texto sin añadir significado semántico.
    
    ```html
    htmlCopiar código
    <p>Esta parte es importante <span style="color: red;">y esta muy importante.</span></p>
    
    ```
    
7. **`<cite>`**: Cita títulos de obras, libros, etc.
    
    ```html
    htmlCopiar código
    <p>Como dijo un sabio <cite>"A programar se aprende programando."</cite></p>
    
    ```
    
8. **`<del>`** y **`<ins>`**: `<del>`: Indica texto eliminado. `<ins>`: Indica texto insertado.
    
    ```html
    htmlCopiar código
    <p>Esta parte me sobraba así que la he <del>eliminado</del></p>
    <p>Me apetecía insertar una palabra random <ins>cacerola</ins>.</p>
    
    ```
    
**Conclusión**

Estas etiquetas de texto en HTML son fundamentales para dar formato y significado a tu contenido. Utilízalas adecuadamente para mejorar la accesibilidad, la semántica y la apariencia de tus páginas web.



## Etiquetas de modificación de texto

---

| Etiqueta | Atributo | Descripción |
| --- | --- | --- |
| <sup> | - | Superíndice. |
| <sub> | - | Subíndice. |
| <small> | - | Texto pequeño. |
| <q> | cite | Cita o quote. |
| <dfn> | title | Definición. |
| <abbr> | title | Abreviatura. |
| <br> | - | Inserta un salto de línea. |
| <wbr> | - | Oportunidad de salto de línea. |

1. **`<sup>`**: Utilizado para representar superíndices.
    
    ```html
    <p>Esto es una potencia 4<sup>2</sup></p>
    ```
    
2. **`<sub>`**: Utilizado para representar subíndices.
    
    ```html
    <p>El agua es H<sub>2</sub>O</p>
    ```
    
3. **`<small>`**: Utilizado para reducir el tamaño del texto.
    
    ```html
    <p><small>Este es un texto más pequeño.</small></p>
    ```
    
4. **`<q>`**: Utilizado para incluir citas cortas. El atributo `cite` puede proporcionar la fuente de la cita.
    
    ```html
    <p><q cite="https://es.wikipedia.org/wiki/Don_Quijote_de_la_Mancha">En un lugar de la Mancha...</q></p>
    ```
    
5. **`<dfn>`**: Utilizado para definir términos. El atributo `title` proporciona la definición del término.
    
    ```html
    <p>La palabra <dfn title="Hipotálamo">hipotálamo</dfn> es una parte del cerebro.</p>
    ```
    
6. **`<abbr>`**: Utilizado para abreviaturas y acrónimos. El atributo `title` proporciona la forma completa de la abreviatura.
    
    ```html
    <p>La <abbr title="Organización de las Naciones Unidas">ONU</abbr> es una organización internacional.</p>
    ```
    
7. **`<br>`**: Utilizado para insertar saltos de línea.
    
    ```html
    <p>Primera línea<br>Segunda línea</p>
    ```
    
8. **`<wbr>`**: Utilizado para sugerir oportunidades de salto de línea.
    
    ```html
    <p>Esto es un texto largo<wbr> que podría necesitar<wbr> un salto de línea.</p>
    ```
    

**Conclusión**

Estas etiquetas de modificación de texto en HTML permiten representar de manera más precisa y semántica diferentes formatos y significados en el contenido. Utilizarlas adecuadamente mejora la accesibilidad y la claridad de la información presentada en la página web.



## Etiquetas de desarrollo

---

Estas etiquetas en HTML están diseñadas para representar entradas de usuario, salidas de programas, variables y otros elementos específicos del desarrollo de software. A continuación, se detallan algunas de las etiquetas más comunes y cómo se utilizan.

| Etiqueta | Atributo | Descripción |
| --- | --- | --- |
| <kbd> | - | Entrada de información del usuario (teclado). |
| <samp> | - | Salida de información de un programa. |
| <var> | - | Variable (matemáticas o informática). |
| <time> | datetime | Indica una fecha/hora. |
| <data> | value | Información equivalente orientada a máquinas. |
| <code> | - | Fragmento de código fuente (en línea). |

1. **`<kbd>`**: Representa una entrada de teclado del usuario.
    
    ```html
    htmlCopiar código
    <p>Pulsa las teclas <kbd>CTRL</kbd>+<kbd>T</kbd> para abrir una nueva pestaña.</p>
    
    ```
    
2. **`<samp>`**: Representa una salida de texto de un programa.
    
    ```html
    htmlCopiar código
    <p>El programa mostró el siguiente mensaje: <samp>Error 404: Página no encontrada</samp></p>
    ```
    
3. **`<var>`**: Representa una variable en matemáticas o programación.
    
    ```html
    <p>Para resolver la ecuación, asigna un valor a la variable <var>x</var>.</p>
    ```
    
4. **`<time>`**: Representa una fecha o una hora. El atributo `datetime` proporciona un valor de fecha/hora en un formato estándar.
    
    ```html
    htmlCopiar código
    <p>La reunión es el <time datetime="2023-06-05T10:00">5 de junio de 2023 a las 10:00</time>.</p>
    
    ```
    
5. **`<data>`**: Representa contenido orientado a máquinas. El atributo `value` proporciona el valor equivalente.
    
    ```html
    htmlCopiar código
    <p>El valor de <data value="42">la respuesta</data> a la vida, el universo y todo lo demás.</p>
    
    ```
    
6. **`<code>`**: Representa un fragmento de código fuente en línea.

```html
htmlCopiar código
<p>Para mostrar un mensaje en la consola, usa el siguiente código: <code>console.log('Hola, mundo');</code></p>

```

**Conclusión**
Estas etiquetas de desarrollo en HTML son útiles para mostrar entradas de usuario, salidas de programas, variables, fechas, datos orientados a máquinas y fragmentos de código de una manera semántica y clara. Utilizarlas adecuadamente mejora la legibilidad y la semántica del contenido relacionado con el desarrollo de software en tu página web.



## Etiquetas de edición

---

Las etiquetas de edición en HTML se utilizan para mostrar fragmentos de texto que han sido añadidos o eliminados, proporcionando información adicional sobre cuándo y por qué se realizó la modificación. Esto es útil para el control de versiones y para proporcionar contexto sobre los cambios en el contenido.

| Etiqueta | Atributo | Descripción |
| --- | --- | --- |
| <ins> | cite, datetime | Fragmento de texto o información añadida a posteriori. |
| <del> | cite, datetime | Fragmento de texto o información eliminada a posteriori. |
1. **`<ins>`**: Utilizada para marcar texto que ha sido añadido a un documento.
    - Atributo `cite`: Proporciona una URL que explica el cambio o la fuente del cambio.
    - Atributo `datetime`: Proporciona la fecha y hora en que se realizó la adición.
    
    ```html
    <p>El texto actualizado es: <ins cite="http://ejemplo.com/actualizado" datetime="2023-06-02">Este es el texto añadido</ins></p>
    ```
    
    - `cite="http://ejemplo.com/actualizado"` proporciona una referencia a la fuente del cambio.
    - `datetime="2023-06-02"` indica la fecha y hora en que se realizó el cambio.
    
2. **`<del>`**: Utilizada para marcar texto que ha sido eliminado de un documento.
    - Atributo `cite`: Proporciona una URL que explica el motivo del cambio o la fuente del cambio.
    - Atributo `datetime`: Proporciona la fecha y hora en que se realizó la eliminación.
    
    ```html
    <p>El texto original es: <del cite="http://ejemplo.com/original" datetime="2023-06-01">Este es el texto eliminado</del></p>
    ```
    
    - `cite="http://ejemplo.com/original"` proporciona una referencia a la fuente del cambio.
    - `datetime="2023-06-01"` indica la fecha y hora en que se realizó el cambio.

**Conclusión**

Las etiquetas `<ins>` y `<del>` son útiles para documentar y visualizar cambios en el contenido, proporcionando contexto sobre cuándo y por qué se realizaron las modificaciones. Esto es especialmente valioso en entornos colaborativos y para el control de versiones de documentos. Utilizarlas adecuadamente puede mejorar la claridad y la transparencia en la gestión de contenido.

## Reto Coding

---

Practicar el uso de etiquetas de texto para cambiar la visualización y el significado semántico del contenido.

### Instrucciones:

1. **Crea un documento HTML** que contenga al menos un ejemplo de cada una de las etiquetas de texto mencionadas.
2. **Asegúrate de incluir ejemplos** que muestren tanto la apariencia visual como el significado semántico del contenido.

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Etiquetas de Texto</title>
    <style>
        .important { color: red; }
        .highlight { background-color: yellow; }
    </style>
</head>
<body>
    <h1>Ejemplos de Etiquetas de Texto en HTML</h1>
    <p>Este es un <em>texto enfatizado</em> y este es un <strong>texto fuerte</strong>.</p>
    <p>Este texto está <mark>resaltado</mark> como con un rotulador.</p>
    <p>Esta es una palabra en <i>cursiva</i> y esta es una palabra en <b>negrita</b>.</p>
    <p>Esta palabra está <u>subrayada</u> y esta está <s>tachada</s>.</p>
    <p>Texto sin significado semántico en un <span class="highlight">span</span>.</p>
    <p>Citando un libro: <cite>"Don Quijote de la Mancha"</cite>.</p>
    <p>Texto <del>eliminado</del> y texto <ins>insertado</ins>.</p>
    <p>Esta es una potencia: 5<sup>2</sup>.</p>
    <p>El agua es H<sub>2</sub>O.</p>
    <p>Este es un texto en <small>tamaño pequeño</small>.</p>
    <p>Una cita breve: <q cite="https://es.wikipedia.org/wiki/Don_Quijote_de_la_Mancha">En un lugar de la Mancha...</q></p>
    <p>Definiendo un término: <dfn title="Hypertext Markup Language">HTML</dfn>.</p>
    <p>Abreviatura: <abbr title="Cascading Style Sheets">CSS</abbr>.</p>
    <p>Este es un salto de línea<br>y este es otro.</p>
    <p>Oportunidad de salto de línea<wbr>aquí.</p>
    <p>Pulsa las teclas <kbd>CTRL</kbd>+<kbd>T</kbd> para abrir una nueva pestaña.</p>
    <p>La salida del programa fue: <samp>Error 404: Not Found</samp>.</p>
    <p>Definiendo una variable: <var>x</var> = 5</p>
    <p>La reunión es a las <time datetime="2023-06-15T14:00">2:00 PM</time>.</p>
    <p>El dato es: <data value="12345">12345</data>.</p>
    <p>Código en línea: <code>console.log('Hola Mundo');</code></p>
</body>
</html>
```