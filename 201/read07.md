# 📚 Guía de Lectura y Debate 07

## 🧠 Conceptos 
🔹 **¿Qué es un objeto?**

Un **objeto** es como una caja que guarda cosas relacionadas: datos (propiedades) y funciones (métodos).

```js
let usuario = {
  nombre: "Ana",
  edad: 30,
  saludar: function () {
    console.log("Hola, soy Ana");
  }
};
```

🔹 **¿Qué es la Programación Orientada a Objetos?**

Es una forma de escribir código pensando en **entidades** del mundo real (como personas, autos, cuentas, etc.) y **dándole a cada entidad sus datos y acciones**.

🔹 **¿Qué es una función constructora?**

Es una **plantilla** para crear muchos objetos similares sin repetir el código. Se usa la palabra clave `function` y `new`.

```js
function Persona(nombre, edad) {
  this.nombre = nombre;
  this.edad = edad;
  this.saludar = function () {
    console.log("Hola, soy " + this.nombre);
  };
}

let persona1 = new Persona("Luis", 25);
let persona2 = new Persona("Lucía", 28);

persona1.saludar(); // Hola, soy Luis
persona2.saludar(); // Hola, soy Lucía
```
---
## 🔁 Refactor de Código: De estructura plana a función constructora
🟠 **Antes (estilo simple o plano)**

Este código usa solo arreglos con objetos sueltos:
```js
let movimientos = [
  { nombre: "Sueldo", monto: 1000, tipo: "ingreso" },
  { nombre: "Renta", monto: 500, tipo: "egreso" }
];

function mostrarIngresos(lista) {
  for (let i = 0; i < lista.length; i++) {
    if (lista[i].tipo === "ingreso") {
      console.log(lista[i].nombre.toUpperCase(), lista[i].monto);
    }
  }
}
```

- Es funcional, pero no reutilizable ni escalable fácilmente.
- Todo está separado: los datos por un lado, la lógica por otro.

---

🟢 **Después (con función constructora - POO)**

Ahora agrupamos **datos** + **lógica** dentro de objetos:
```js
// Creamos una "plantilla" de movimiento
function Movimiento(nombre, monto, tipo) {
  this.nombre = nombre;
  this.monto = monto;
  this.tipo = tipo;

  // Método para verificar si es ingreso
  this.esIngreso = function () {
    return this.tipo === "ingreso";
  };

  this.mostrar = function () {
    console.log(this.nombre.toUpperCase(), this.monto);
  };
}

// Creamos objetos usando new
let mov1 = new Movimiento("Sueldo", 1000, "ingreso");
let mov2 = new Movimiento("Renta", 500, "egreso");

// Usamos los métodos
if (mov1.esIngreso()) mov1.mostrar(); // SUELDO 1000
```

✅ Ventajas:

- Cada movimiento “sabe” cómo comportarse.
- Podemos agregar más lógica sin repetir código.
- Es más organizado y escalable.
---

## ✅ Verdadero o Falso con Explicaciones

| Enunciado | ¿Verdadero o Falso? | Explicación |
|-----------|----------------------|-------------|
| “Todos los lenguajes orientados a objetos soportan herencia múltiple por defecto.” | ❌ Mito | JavaScript solo permite herencia simple usando prototipos. Otros lenguajes como Java tampoco permiten herencia múltiple directa. |
| “La Programación Orientada a Objetos permite organizar el código en entidades con responsabilidad clara.” | ✅ Verdad | La POO permite crear objetos con tareas y datos propios, lo que mejora la organización del código. |
| “En JavaScript, usar funciones constructoras es obsoleto porque existen las clases desde ES6.” | ❌ Mito | Aunque ES6 introdujo `class`, las funciones constructoras siguen siendo válidas y son parte del núcleo del lenguaje. |
| “La abstracción implica eliminar cualquier detalle que no sea importante para la funcionalidad principal.” | ✅ Verdad | Abstraer es enfocarse en lo esencial y dejar fuera los detalles innecesarios, haciendo el código más claro y mantenible. |
| “Para crear objetos usando funciones constructoras, es obligatorio usar el prototipo explícitamente.” | ❌ Mito | No es obligatorio. Puedes definir métodos directamente dentro de la función constructora, aunque usar `prototype` puede mejorar la eficiencia. |
| “La POO promueve la escalabilidad al agrupar datos y comportamiento en entidades lógicas.” | ✅ Verdad | Al encapsular datos y lógica, es más fácil mantener, extender y escalar el código. |
| “La palabra clave this en las funciones constructoras apunta a un objeto global, sin importar si se usa new.” | ❌ Mito | Si no usas `new`, `this` puede apuntar al objeto global o ser `undefined` (modo estricto). Con `new`, `this` siempre apunta al nuevo objeto creado. |

## 🧾 Conclusión

La Programación Orientada a Objetos con funciones constructoras en JavaScript permite crear estructuras organizadas, reutilizables y escalables. Entender conceptos como abstracción, `this`, y `prototype` facilita escribir código más claro y mantenible. Aunque existen clases modernas, las funciones constructoras siguen siendo fundamentales para comprender cómo funciona JavaScript desde su base.
