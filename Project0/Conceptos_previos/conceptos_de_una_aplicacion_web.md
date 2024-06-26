<div style="text-align: center;">
  <img src="https://github.com/Hack-io-Data/Imagenes/blob/main/01-LogosHackio/logo_celeste@4x.png?raw=true" alt="logo hack(io)" />
</div>

# Conceptos base de una aplicación web

Vamos a ver cómo funciona todo el proceso detrás de una aplicación web usando un ejemplo sencillo: una app para pedir pizzas. Imagina que quieres pedir una pizza desde tu computadora o tu teléfono. Vamos a desglosar cómo cada parte trabaja para que puedas hacer tu pedido sin problemas.

## **Navegadores (Frontend)**

---

**Qué es:** El navegador es el programa que usas para navegar por Internet, como Chrome, Firefox, o Safari.

**Qué hace:** Muestra las páginas web y permite interactuar con ellas. Básicamente, es la parte de la aplicación que ves y con la que interactúas.

Imagina que abres el navegador y ves una página web donde puedes seleccionar el tipo de pizza que quieres, la cantidad, y hacer clic en un botón para pedirla.

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Pide tu Pizza</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <header>
      <h1>Pide tu Pizza</h1>
      <nav>
        <ul>
          <li><a href="#menu">Menú</a></li>
          <li><a href="#pedido">Hacer Pedido</a></li>
        </ul>
      </nav>
    </header>
    <main>
      <section id="menu">
        <h2>Menú</h2>
        <ul id="lista-pizzas"></ul>
      </section>
      <section id="pedido">
        <h2>Hacer Pedido</h2>
        <form id="form-pedido">
          <label for="pizza">Elige tu pizza:</label>
          <select id="pizza" name="pizza"></select>
          <label for="cantidad">Cantidad:</label>
          <input type="number" id="cantidad" name="cantidad" min="1" required />
          <input type="submit" value="Pedir" />
        </form>
      </section>
    </main>
    <footer>
      <p>&copy; 2023 Pizzería. Todos los derechos reservados.</p>
    </footer>
    <script src="scripts.js"></script>
  </body>
</html>
```

## **Servidor (Backend)**

---

**Qué es:** El servidor es como el cerebro detrás de tu sitio web. Es donde se maneja la lógica, los cálculos y se procesan las solicitudes.

**Qué hace:** Responde a las solicitudes que le haces desde el navegador. Por ejemplo, cuando haces clic en "Pedir", el servidor recibe esa solicitud, procesa la información y te devuelve una respuesta.

Cuando haces tu pedido de pizza, el servidor recibe la información de qué pizza quieres y cuántas unidades, y entonces inicia el proceso para preparar tu pedido.

## **Base de Datos**

---

**Qué es:** La base de datos es como una gran libreta donde se guarda toda la información necesaria para la aplicación, como los tipos de pizza disponibles, los pedidos realizados, etc.

**Qué hace:** Almacena y gestiona todos los datos que la aplicación necesita. Permite guardar la información de manera organizada para que el servidor pueda acceder a ella cuando sea necesario.

Cuando pides una pizza, la información de tu pedido se guarda en la base de datos para que el restaurante pueda prepararla y también para llevar un registro de todos los pedidos.

## **API (Interfaz de Programación de Aplicaciones)**

---

**Qué es:** La API es como un mensajero que lleva y trae información entre el frontend (navegador) y el backend (servidor).

**Qué hace:** Permite que el frontend y el backend se comuniquen de manera efectiva. Cuando el navegador necesita alguna información o enviar un pedido, lo hace a través de la API.

Cuando seleccionas una pizza y haces clic en "Pedir", el navegador envía esa información a la API, que luego se la pasa al servidor. El servidor procesa el pedido y usa la API para enviar una respuesta de vuelta al navegador, confirmando que el pedido se ha realizado.

```js
document.addEventListener("DOMContentLoaded", function () {
  fetch("/api/pizzas")
    .then((response) => response.json())
    .then((data) => {
      const listaPizzas = document.getElementById("lista-pizzas");
      data.forEach((pizza) => {
        const li = document.createElement("li");
        li.textContent = pizza.name;
        listaPizzas.appendChild(li);
      });

      const selectPizza = document.getElementById("pizza");
      data.forEach((pizza) => {
        const option = document.createElement("option");
        option.value = pizza.id;
        option.textContent = pizza.name;
        selectPizza.appendChild(option);
      });
    });

  document
    .getElementById("form-pedido")
    .addEventListener("submit", function (e) {
      e.preventDefault();
      const pizzaId = document.getElementById("pizza").value;
      const cantidad = document.getElementById("cantidad").value;

      fetch("/api/pedidos", {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
        },
        body: JSON.stringify({ pizzaId, cantidad }),
      })
        .then((response) => response.json())
        .then((data) => {
          alert("Pedido realizado con éxito: " + data.message);
        });
    });
});
```

**Resumiendo**

- **Navegador:** Es donde ves e interactúas con la página web. Muestra la información y permite hacer acciones como pedir una pizza.
- **Servidor:** Procesa las solicitudes y maneja la lógica de la aplicación. Es el cerebro detrás de escena.
- **Base de Datos:** Guarda toda la información que la aplicación necesita, como los tipos de pizza y los pedidos.
- **API:** Actúa como un mensajero entre el navegador y el servidor, permitiendo la comunicación y el intercambio de datos.

¡Y así es como puedes pedir una pizza online usando una aplicación web!

## Contenido asociado
---
- [Video: API](https://vimeo.com/840027895/af09d0f6ee)
