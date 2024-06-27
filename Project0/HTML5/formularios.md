<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Formularios

Los formularios son elementos en los que se integran botones y áreas de texto para que los usuarios introduzcan datos o puedan elegir entre varias opciones. Veamos las etiquetas utilizadas para la creación de formularios en HTML5.

Los formularios son las piezas de **HTML5** que nos permiten recoger la información que introduce el usuario. Hay algunos elementos básicos dentro de nuestro formulario.

## Etiqueta `<form>`

---

Siempre usamos la etiqueta `<form>` para englobar todo el contenido del formulario. En esta etiqueta se suelen definir tres atributos principales:

1. **action**: Define la localización donde se enviará la información que se recoja en el formulario.
2. **method**: Define el método HTTP en el que se enviará esta información, puede ser **get** o **post**.
3. **name**: Hace referencia al nombre del formulario.

```html
<form name="miFormulario" action="/next-page" method="post"></form>
```

Otros atributos:

| Atributo | Valor | Descripción |
| --- | --- | --- |
| target | destino | Nombre del lugar donde se abrirá el formulario. _blank para nueva pestaña. |
| enctype | application/x-www-form-urlencoded, multipart/form-data, text/plain | Codificación para el envío del formulario. Importante para envío de archivos. |
| accept-charset | codificación | Fuerza a utilizar una codificación en los parámetros de texto del formulario. |
| autocomplete | on, off | Activa o desactiva el autocompletado para todos los campos del formulario. |
| novalidate |  | Con este atributo presente, el formulario obvia la validación HTML5. |

## Ejemplos de uso etiqueta `<form>`

---

```html
<form action="/action.php" target="_blank" accept-charset="utf-8">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname" /><br /><br />
  <input type="submit" value="Submit" />
</form>
```

```html
<form
  action="/action.asp"
  method="post"
  novalidate
  enctype="multipart/form-data"
>
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname" /><br /><br />
  <label for="lname">Last name:</label>
  <input type="text" id="lname" name="lname" /><br /><br />
  <input type="submit" value="Submit" />
</form>
```

```html
<form action="/action.php" method="get" autocomplete="on">
  <label for="fname">First name:</label>
  <input type="text" id="fname" name="fname" /><br /><br />
  <label for="email">Email:</label>
  <input type="text" id="email" name="email" /><br /><br />
  <input type="submit" />
</form>
```

## Etiqueta `<input>`

---

La etiqueta `<input>` define un campo dentro de un formulario y tiene varios tipos y atributos principales:

- **type**: Define el tipo de campo de entrada. Algunos tipos comunes son **text**, **checkbox**, **date**, **number**, **password**, **radio**, **submit**, **file**.
- **name**: Especifica un nombre a cada campo de entrada del formulario, necesario para enviar los datos al backend.
- **value**: Define el valor por defecto de un campo de entrada.

```html
<input type="button">
<input type="checkbox">
<input type="color">
<input type="date">
<input type="datetime-local">
<input type="email">
<input type="file">
<input type="hidden">
<input type="image">
<input type="month">
<input type="number">
<input type="password">
<input type="radio">
<input type="range">
<input type="reset">
<input type="search">
<input type="submit">
<input type="tel">
<input type="text">
<input type="time">
<input type="url">
<input type="week">
```

## Ejemplos de uso etiqueta `<input>`

---

```html
<label for="fname">First name:</label>
<input type="text" id="fname" name="fname">
<label for="lname">Last name:</label>
<input type="text" id="lname" name="lname">
<input type="submit" value="Submit">
```

## Campos de Texto

---

La etiqueta `<input>` puede tener diferentes tipos para campos de texto:

- **text**: Campo de texto común.
- **password**: Campo de texto para contraseñas, no muestra los caracteres.
- **email**: Campo para correos electrónicos.
- **tel**: Campo para números de teléfono.
- **url**: Campo para URLs.
- **search**: Campo para búsquedas.
- **hidden**: Campo oculto, no visible para el usuario.

```html
<input type="text" id="email" name="email" size="70" value="usuario@dominio.com">
<input type="password" id="clave" name="clave" size="20">
```

## Etiqueta `<textarea>`

---

La etiqueta `<textarea>` define un área de texto de varias líneas. Se utiliza para recoger textos más largos, como comentarios.

```html
<label for="comments">Comentarios:</label>
<textarea id="comments">Este será el contenido de los comentarios</textarea>
```

## Campos Numéricos

---

Para obtener información numérica en un formulario, utilizamos:

- **number**: Campo para números.
- **range**: Barra de rango.

Atributos adicionales:

- **min**: Valor mínimo permitido.
- **max**: Valor máximo permitido.
- **step**: Intervalo de números legales.

```html
<form method="post" action="/user">
    <label for="age">Edad:</label>
    <input type="number" name="age" placeholder="Su edad" min="14" max="99">
    <button type="submit">Enviar</button>
</form>
```

## Campos de Fecha y Hora

---

Para recoger fechas y horas, utilizamos:

- **date**: Campo de fecha.
- **datetime-local**: Campo de fecha y hora locales.
- **month**: Campo de mes.
- **time**: Campo de hora.
- **week**: Campo de semana.

```html
<form name="formulario" method="post" action="/send.php">
  <input type="date" name="fecha" min="2034-03-25" max="2038-05-25" step="2">
  <input type="time" name="hora" min="18:00" max="21:00" step="3600">
</form>
```

## Botones, Checkbox y Radios

---

Botón `<input type="button">`: Se utiliza para realizar operaciones como enviar formularios o manipular datos.

```html
<input type="button" value="TextoBotón">
```

Checkbox `<input type="checkbox">`: Permite seleccionar múltiples opciones.

```html
<input type="checkbox" id="identificador" name="nombre">
<input type="checkbox" id="identificador" name="nombre" checked="checked">
```

```html
<input type="checkbox" name="lenguaje" value="html">HTML
<input type="checkbox" name="lenguaje" value="javascript">Javascript
<input type="checkbox" name="lenguaje" value="css">CSS
<input type="checkbox" name="lenguaje" value="xml">XML
```

Radio `<input type="radio">`: Permite seleccionar solo una opción de un grupo.

```html
<input type="radio" id="identificador" value="valor" name="nombre">
<input type="radio" id="identificador" value="valor" name="nombre" checked="checked">
```

```html
<input type="radio" id="menos18" value="menos18" name="edad">Menos de 18
<input type="radio" id="18a30" value="18a30" name="edad">18 a 30
<input type="radio" id="31a50" value="31a50" name="edad">31 a 50
<input type="radio" id="mas50" value="mas50" name="edad">Más de 50
```

## Listas de selección

---

Etiqueta `<select>`: Crea una lista desplegable. Dentro de la etiqueta `<select>` habrá diferentes etiquetas `<option>`.

```html
<label for="avengers">Elige una opción:</label>
<select name="avengers" id="avengers">
  <option value="thor">Thor</option>
  <option value="hulk">Hulk</option>
  <option value="ironman">Ironman</option>
</select>
```

Etiqueta `<optgroup>`: Agrupa opciones dentro de un `<select>`.

```html
<select name="ciudad">
  <optgroup label="Europa">
    <option>Madrid</option>
    <option>Londres</option>
    <option>Paris</option>
  </optgroup>
  <optgroup label="Suramerica">
    <option>Santiago</option>
    <option>Sao Paulo</option>
    <option>Lima</option>
    <option>Bogota</option>
  </optgroup>
  <optgroup label="Africa">
    <option>Casablanca</option>
    <option>Ciudad del Cabo</option>
  </optgroup>
</select>
```

Etiqueta `<datalist>`: Crea una lista abierta, donde el usuario puede seleccionar una opción de las sugeridas o crear la suya propia.

```html
<form name="formulario" method="post" action="/send.php">
  <input type="text" list="items">
  <datalist id="items">
    <option value="1">Opción 1</option>
    <option value="2">Opción 2</option>
    <option value="3">Opción 3</option>
  </datalist>
</form>
```

Selección de Color: HTML5 introduce un campo de entrada de tipo color.

```html
<form name="formulario" method="post" action="/send.php">
  Selecciona el color deseado:
  <input type="color" name="color" value="#FF0000">
</form>
```

Selección de Ficheros: HTML nos proporciona un input de tipo file para seleccionar, adjuntar y enviar archivos.

```html
<input type="file" id="identificador" value="valor" name="nombre">
```

Atributo `multiple`: Permite seleccionar varios archivos.

```html
<form>
  <label for="files">Select files:</label>
  <input type="file" id="files" name="files" multiple>
</form>
```

## Organización de Campos

---

Etiqueta `<fieldset>`: Define una agrupación de elementos comunes dentro del formulario.

```html
<form action="/next-page" method="post">
  <fieldset>
    <legend>Datos Básicos</legend>
  </fieldset>
</form>
```

Etiqueta `<label>`: Acompaña a un campo del formulario con un título descriptivo.

```html
<label for="name">Nombre</label>
<input type="text" name="name" id="name">
```

## Botones de Envío de Formularios

---

Submit: Envía los datos del formulario al servidor.

```html
<input type="submit" value="Enviar">
```

```html
<form name="formulario" method="post" action="/send.php">
  Usuario: <input type="text" name="usuario">
  <input type="image" src="enviar.png" alt="Enviar" width="80" height="28">
</form>
```

Reset: Borra los datos del formulario.

```html
<input type="reset" value="Borrar">

```

Botón Personalizado `<button>`: Se utiliza para desencadenar eventos de JavaScript.

```html
<button type="submit">Enviar</button>
```

## Medidores y Barras de Progreso

---

Barra de Progreso `<progress>`: Muestra una barra de progreso.

```html
<progress max="100" value="10"></progress>
```

Medidor Personalizado `<meter>`: Crea medidores personalizados.

```html
<form name="formulario" method="post" action="/send.php">
  <meter min="0" max="100" low="25" high="75" optimum="100" value="75"></meter>
</form>
```

## Validaciones HTML5

---

Las herramientas de validación nos sirven para establecer pautas a la hora de indicar al usuario que la información que ha introducido es correcta o debe modificarla. Tipos de validaciones:

1. **Sin validación**: El usuario puede escribir cualquier información sin restricciones.
2. **Validación en el front-end**: La información se verifica antes de enviarla al servidor.
3. **Validación solo en el back-end**: La información se verifica solo en el servidor.
4. **Doble validación en front-end y back-end**: Lo ideal para mayor seguridad y eficiencia.

Atributos de Validación:

- **required**: Campo obligatorio.
- **minlength** y **maxlength**: Tamaño mínimo y máximo de caracteres.
- **min** y **max**: Valores mínimos y máximos para campos numéricos.
- **disabled**: Deshabilita un campo del formulario.
- **readonly**: Campo de solo lectura.
- **pattern**: Usa expresiones regulares para validar el campo.

```html
<form method="post" action="/nombre">
  <label for="name">Nombre:</label>
  <input type="text" name="name" placeholder="Su nombre" required />
  <button type="submit">Enviar</button>
</form>

<form method="post" action="/user">
  <label for="nick">nickName:</label>
  <input
    type="text"
    name="nick"
    placeholder="Su nick"
    minlength="2"
    maxlength="8"
  />
  <button type="submit">Enviar</button>
</form>

<form method="post" action="/user">
  <label for="age">Edad:</label>
  <input type="number" name="age" placeholder="Su edad" min="14" max="99" />
  <button type="submit">Enviar</button>
</form>
```

## Reto Coding

---

Crear un formulario en HTML que incluya diversos tipos de entradas, tales como texto, correo electrónico, contraseña, fecha, número, opciones de selección, checkboxes, y botones de envío. Además, aplicar validaciones utilizando atributos HTML5.

### Instrucciones:

1. **Crear un documento HTML** que incluya:
    - Un formulario que recoja el nombre del usuario, correo electrónico, contraseña, fecha de nacimiento, número de teléfono, selección de género, lenguajes de programación preferidos, y un botón de envío.
    - Validaciones HTML5 para asegurarse de que los campos obligatorios sean completados correctamente.
2. **Contenido del formulario**:
    - El formulario debe contener etiquetas `<form>`, `<input>`, `<label>`, `<select>`, `<option>`, `<textarea>`, y `<button>`.
    - Los campos deben tener validaciones como `required`, `minlength`, `maxlength`, `pattern`, `min`, `max`, etc.
3. Estilos asociados
    
    ```html
     <style>
            body {
                font-family: Arial, sans-serif;
                background-color: #f2f2f2;
                margin: 0;
                padding: 0;
                display: flex;
                justify-content: center;
                align-items: center;
                height: 100vh;
            }
            form {
                background-color: white;
                padding: 20px;
                border-radius: 5px;
                box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            }
            label {
                display: block;
                margin-bottom: 8px;
            }
            input, select, textarea, button {
                width: 100%;
                padding: 10px;
                margin-bottom: 10px;
                border: 1px solid #ccc;
                border-radius: 5px;
            }
            button {
                background-color: #4285f4;
                color: white;
                border: none;
                cursor: pointer;
            }
            button:hover {
                background-color: #357ae8;
            }
        </style>
    ```
    

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Formulario de Registro</title>
    <style>
      body {
          font-family: Arial, sans-serif;
          background-color: #f2f2f2;
          margin: 0;
          padding: 0;
          display: flex;
          justify-content: center;
          align-items: center;
          height: 100vh;
      }
      form {
          background-color: white;
          padding: 20px;
          border-radius: 5px;
          box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      }
      label {
          display: block;
          margin-bottom: 8px;
      }
      input, select, textarea, button {
          width: 100%;
          padding: 10px;
          margin-bottom: 10px;
          border: 1px solid #ccc;
          border-radius: 5px;
      }
      button {
          background-color: #4285f4;
          color: white;
          border: none;
          cursor: pointer;
      }
      button:hover {
          background-color: #357ae8;
      }
    </style>
  </head>
  <body>
    <form action="/submit" method="post">
      <fieldset>
        <legend>Datos Personales</legend>

        <label for="nombre">Nombre:</label>
        <input
          type="text"
          id="nombre"
          name="nombre"
          required
          minlength="3"
          maxlength="50"
          placeholder="Escribe tu nombre"
        />

        <label for="email">Correo Electrónico:</label>
        <input
          type="email"
          id="email"
          name="email"
          required
          placeholder="Escribe tu correo electrónico"
        />

        <label for="password">Contraseña:</label>
        <input
          type="password"
          id="password"
          name="password"
          required
          minlength="6"
          placeholder="Escribe tu contraseña"
        />

        <label for="fecha_nacimiento">Fecha de Nacimiento:</label>
        <input
          type="date"
          id="fecha_nacimiento"
          name="fecha_nacimiento"
          required
        />

        <label for="telefono">Número de Teléfono:</label>
        <input
          type="tel"
          id="telefono"
          name="telefono"
          required
          pattern="[0-9]{9}"
          placeholder="Escribe tu número de teléfono"
        />

        <label for="genero">Género:</label>
        <select id="genero" name="genero" required>
          <option value="">Selecciona tu género</option>
          <option value="masculino">Masculino</option>
          <option value="femenino">Femenino</option>
          <option value="otro">Otro</option>
        </select>
      </fieldset>

      <fieldset>
        <legend>Preferencias</legend>

        <label>Lenguajes de Programación:</label>
        <input type="checkbox" id="html" name="lenguajes" value="HTML" />
        <label for="html">HTML</label>
        <input type="checkbox" id="css" name="lenguajes" value="CSS" />
        <label for="css">CSS</label>
        <input
          type="checkbox"
          id="javascript"
          name="lenguajes"
          value="JavaScript"
        />
        <label for="javascript">JavaScript</label>
        <input type="checkbox" id="python" name="lenguajes" value="Python" />
        <label for="python">Python</label>
      </fieldset>

      <button type="submit">Enviar</button>
      <button type="reset">Borrar</button>
    </form>
  </body>
</html>
```

### Explicación del **Reto Coding**

1. **Estructura del Documento**: El documento HTML comienza con la declaración `<!DOCTYPE html>`, seguida de las etiquetas `<html>`, `<head>`, y `<body>`.
2. **Meta Etiquetas**: Se incluyen meta etiquetas para la codificación de caracteres y el viewport.
3. **Estilos CSS**: Se agregan estilos básicos para mejorar la apariencia del formulario.
4. **Formulario**: La etiqueta `<form>` incluye los atributos `action` y `method`.
5. **Fieldset y Legend**: Se utilizan para agrupar los campos del formulario en secciones lógicas.
6. **Etiquetas de Entrada**: Se utilizan varias etiquetas `<input>` con diferentes tipos como `text`, `email`, `password`, `date`, `tel`, y `checkbox`.
7. **Select**: Para seleccionar el género.
8. **Botones**: Se incluyen botones de envío y reseteo.

## Contenido asociado
---
- [Video: Estructura](https://vimeo.com/846233392/2937f45c3e)
- [Video: Inputs](https://vimeo.com/846233359/c6038eff88)
- [Video: Conclusiones](https://vimeo.com/846233309/649a76e934)