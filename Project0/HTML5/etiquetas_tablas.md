<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Etiquetas de tablas

Las tablas en HTML permiten organizar datos en filas y columnas, facilitando la presentación estructurada de la información.

## Etiquetas de tabla

---

Para crear una tabla, usamos las siguientes etiquetas:

- `<table>`: Define una tabla.
- `<thead>`: Agrupa el contenido del encabezado de una tabla.
- `<tbody>`: Agrupa el contenido del cuerpo de una tabla.
- `<tfoot>`: Agrupa el contenido del pie de una tabla.
- `<caption>`: Proporciona un título o una descripción para la tabla.
- `<tr>`: Define una fila en una tabla.
- `<th>`: Define una celda de encabezado en una tabla.
- `<td>`: Define una celda estándar en una tabla.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabla de Vehículos</title>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }
        caption {
            font-weight: bold;
            margin-bottom: 10px;
        }
        th, td {
            border: 1px solid #000;
            padding: 8px;
            text-align: left;
        }
        thead {
            background-color: #f2f2f2;
        }
        tfoot {
            background-color: #f2f2f2;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <table>
        <caption>Listado de Vehículos</caption>
        <thead>
            <tr>
                <th>Marca</th>
                <th>Modelo</th>
                <th>Color</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Peugeot</td>
                <td>406</td>
                <td>Rojo</td>
            </tr>
            <tr>
                <td>Ford</td>
                <td>Mustang</td>
                <td>Negro</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="3">Total de Vehículos: 2</td>
            </tr>
        </tfoot>
    </table>
</body>
</html>

```

## Agrupar columnas en HTML

---

Podemos usar las etiquetas `<colgroup>` y `<col>` para aplicar estilos a grupos de columnas en una tabla. Estas etiquetas permiten definir un grupo de columnas y aplicarles estilos específicos, mejorando la presentación y la legibilidad de la tabla.

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Agrupación de Columnas</title>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #000;
            padding: 8px;
            text-align: left;
        }
        thead {
            background-color: #f2f2f2;
        }
        colgroup col {
            border: 1px solid #000;
        }
    </style>
</head>
<body>
    <table>
        <colgroup>
            <col span="2" style="background-color: lightgray;">
            <col style="background-color: lightblue;">
        </colgroup>
        <thead>
            <tr>
                <th>Alumno</th>
                <th>Curso</th>
                <th>Edad</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Alberto Rivera</td>
                <td>Fullstack</td>
                <td>26</td>
            </tr>
            <tr>
                <td>Gandalf el Gris</td>
                <td>Master en Istar</td>
                <td>Indeterminado</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

1. **`<table>`**: Define la tabla.
2. **`<colgroup>`**:
    - Agrupa una o más columnas para aplicarles estilos comunes.
    - En este ejemplo, el primer `<col>` aplica un estilo de fondo gris claro a las primeras dos columnas, y el segundo `<col>` aplica un fondo azul claro a la tercera columna.
3. **`<col>`**:
    - Define columnas individuales dentro de un `<colgroup>`.
    - El atributo `span` especifica el número de columnas a las que se aplica el estilo.
    
    ```html
    <colgroup>
        <col span="2" style="background-color: lightgray;">
        <col style="background-color: lightblue;">
    </colgroup>
    ```
    
4. **`<thead>`**: Agrupa el contenido del encabezado de la tabla.
    
    ```html
    <thead>
        <tr>
            <th>Alumno</th>
            <th>Curso</th>
            <th>Edad</th>
        </tr>
    </thead>
    ```
    
5. **`<tbody>`**: Agrupa el contenido del cuerpo de la tabla.
    
    ```html
    <tbody>
        <tr>
            <td>Alberto Rivera</td>
            <td>Fullstack</td>
            <td>26</td>
        </tr>
        <tr>
            <td>Gandalf el Gris</td>
            <td>Master en Istar</td>
            <td>Indeterminado</td>
        </tr>
    </tbody>
    
    ```
    

## Más ejemplos de agrupación de columnas

---

Tabla con **diferentes estilos** de columnas:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabla de Estudiantes</title>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #000;
            padding: 8px;
            text-align: left;
        }
        thead {
            background-color: #f2f2f2;
        }
        colgroup col {
            border: 1px solid #000;
        }
    </style>
</head>
<body>
    <table>
        <colgroup>
            <col style="background-color: lightcoral;">
            <col style="background-color: lightgreen;">
            <col style="background-color: lightyellow;">
        </colgroup>
        <thead>
            <tr>
                <th>Nombre</th>
                <th>Apellido</th>
                <th>Edad</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>María</td>
                <td>García</td>
                <td>22</td>
            </tr>
            <tr>
                <td>Juan</td>
                <td>Pérez</td>
                <td>24</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

- Cada columna tiene un color de fondo diferente.
- La primera columna tiene un fondo rojo claro (`lightcoral`), la segunda verde claro (`lightgreen`) y la tercera amarillo claro (`lightyellow`).

Tabla con **agrupación y alineación** de Columnas:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabla de Ventas</title>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #000;
            padding: 8px;
            text-align: left;
        }
        thead {
            background-color: #f2f2f2;
        }
        colgroup col {
            border: 1px solid #000;
        }
        .right-align {
            text-align: right;
        }
    </style>
</head>
<body>
    <table>
        <colgroup>
            <col style="background-color: lightgray;">
            <col class="right-align" style="background-color: lightyellow;">
            <col class="right-align" style="background-color: lightblue;">
        </colgroup>
        <thead>
            <tr>
                <th>Producto</th>
                <th>Precio</th>
                <th>Cantidad</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Manzana</td>
                <td>$1.00</td>
                <td>50</td>
            </tr>
            <tr>
                <td>Plátano</td>
                <td>$0.50</td>
                <td>100</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

En este ejemplo:

- Se aplica alineación a la derecha (`right-align`) a las columnas de "Precio" y "Cantidad".
- Las columnas de precios y cantidades están coloreadas con fondos diferentes para mejorar la legibilidad.

**Conclusión**
Usar las etiquetas `<colgroup>` y `<col>` en tablas HTML permite aplicar estilos específicos a grupos de columnas, mejorando la presentación y la organización de los datos. Los ejemplos proporcionados demuestran cómo aplicar estilos y alineaciones específicas a columnas individuales o grupos de columnas, creando tablas claras y bien estructuradas.

## Reto Coding

---

Practicar la creación y el uso de tablas en HTML para organizar datos.

### Instrucciones:

1. **Crea un documento HTML** que contenga una tabla con los datos de tu elección.
2. **Utiliza las etiquetas principales** (`<table>`, `<thead>`, `<tbody>`, `<tfoot>`, `<caption>`) para estructurar la tabla.
3. **Aplica estilos** usando `<colgroup>` y `colspan` para combinar y agrupar celdas.
    
    ```html
    <style>
            table {
                width: 100%;
                border-collapse: collapse;
            }
            th, td {
                border: 1px solid black;
                padding: 8px;
                text-align: left;
            }
            thead {
                background-color: #f2f2f2;
            }
            tfoot {
                background-color: #f9f9f9;
            }
        </style>
    ```
    

**Solución Reto Coding**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Tabla</title>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid black;
            padding: 8px;
            text-align: left;
        }
        thead {
            background-color: #f2f2f2;
        }
        tfoot {
            background-color: #f9f9f9;
        }
    </style>
</head>
<body>
    <table>
        <caption>Listado de Productos</caption>
        <colgroup>
            <col style="background-color: lightgray;">
            <col style="background-color: lightgray;">
            <col style="background-color: lightblue;">
        </colgroup>
        <thead>
            <tr>
                <th>Producto</th>
                <th>Precio</th>
                <th>Cantidad</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Manzanas</td>
                <td>2€</td>
                <td>10</td>
            </tr>
            <tr>
                <td>Naranjas</td>
                <td>3€</td>
                <td>5</td>
            </tr>
            <tr>
                <td colspan="2">Total:</td>
                <td>15</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="3">Precios en Euros</td>
            </tr>
        </tfoot>
    </table>
</body>
</html>
```