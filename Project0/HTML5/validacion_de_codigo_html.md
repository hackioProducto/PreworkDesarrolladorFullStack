<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Validación de código HTML

Los navegadores web, por defecto, utilizan un método intuitivo que les permite continuar con la carga de un documento HTML, incluso si encuentran errores en el código. Sin embargo, esta capacidad de "autocorrección" puede ocultar problemas que afecten la accesibilidad, el rendimiento y la compatibilidad de nuestras páginas web. Para evitar estos problemas, es esencial utilizar un **validador HTML**.

## ¿Qué es un validador HTML?

---

Un validador HTML es una herramienta que analiza el código HTML y señala los errores presentes, proporcionando una breve descripción de cada error. Esto es especialmente útil para asegurar que nuestro código cumpla con los estándares web y que sea accesible y compatible con diferentes navegadores y dispositivos.

## Uso del validador Nu HTML Checker

---

El [Nu HTML Checker](https://validator.w3.org/) es una herramienta proporcionada por el W3C (World Wide Web Consortium) que valida el código HTML. Es una de las herramientas más confiables para asegurar que tu código siga las mejores prácticas y estándares web.

Métodos para Validar tu Código

1. **Address**: Introduce la URL de la página que quieres validar.
2. **File Upload**: Sube directamente el archivo HTML que quieres validar.
3. **Text Input**: Copia y pega tu código HTML directamente en el validador.

Opciones Avanzadas, al hacer clic en "More Options", puedes acceder a configuraciones adicionales:

- **Show source**: Muestra tu código HTML con los errores destacados, línea por línea.
- **Outline**: Proporciona una vista en forma de árbol de la estructura de tu documento HTML.
- **Image report**: Genera un informe con las imágenes presentes en tu página web, detallando información relevante sobre ellas.

## Reto Coding

---

Supongamos que tienes el siguiente código HTML y quieres asegurarte de que esté libre de errores

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ejemplo de Validación</title>
</head>
<body>
    <h1>Hola Mundo</h1>
    <p>Este es un párrafo de ejemplo.</p>
    <img src="imagen.jpg" alt="Descripción de la imagen">
</body>
</html>
```

### Instrucciones:

1. **Copia el código** y pégalo en la opción **Text Input** del Nu HTML Checker.
2. Haz clic en **Check** para validar el código.
3. Revisa los resultados proporcionados por el validador. Si hay errores, el validador te mostrará una descripción y la línea donde se encuentra cada error.

**Solución Reto Coding**

```vbnet
Error: Element “img” is missing required attribute “alt”.
From line 10, column 5; to line 10, column 43
```

Este mensaje indica que el elemento `<img>` está perdiendo el atributo `alt`, que es obligatorio para describir la imagen.

Consejos Finales

1. **Valida tu código regularmente**: Hacerlo durante el desarrollo te ayuda a identificar y corregir errores tempranamente.
2. **Utiliza las opciones avanzadas**: Estas opciones pueden darte una visión más clara y detallada de los problemas en tu código.
3. **Consulta la documentación**: La [documentación de MDN](https://developer.mozilla.org/es/docs/Web/HTML/Reference) es un excelente recurso para aprender más sobre HTML y asegurarte de que estás siguiendo las mejores prácticas.
