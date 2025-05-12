# 📚 Lectura y Debate 06: Programación Funcional en JavaScript

## 🎯 Objetivos
- Comprender el paradigma funcional y cómo se diferencia del paradigma imperativo.
- Aplicar funciones puras para resolver problemas sin efectos secundarios.
- Utilizar funciones de orden superior (`map()`, `filter()`, `find()`) para transformar datos de forma declarativa.

---

## 🔑 Conceptos Clave

| Concepto                  | Definición                                                                 |
|--------------------------|---------------------------------------------------------------------------|
| **Programación Funcional** | Paradigma basado en funciones puras, inmutabilidad y sin efectos secundarios. |
| **Funciones Puras**        | Dependen solo de sus argumentos y no modifican el estado externo.         |
| **Funciones de Orden Superior** | Reciben o retornan funciones (por ejemplo: `map()`, `filter()`, `find()`).    |
| **Declarativo vs Imperativo** | Declarativo: describe *qué* se quiere hacer. Imperativo: detalla *cómo* hacerlo. |
| **Principio DRY**          | “Don't Repeat Yourself”: evita la duplicación de lógica mediante funciones reutilizables. |

---

## 🧠 Reflexiones

### 🔹 Diferencias entre paradigma imperativo y funcional

| Aspecto             | Imperativo                                          | Funcional                                             |
|---------------------|-----------------------------------------------------|-------------------------------------------------------|
| Estilo              | Paso a paso (cómo se hace)                          | Declarativo (qué se quiere hacer)                    |
| Mutabilidad         | Mutación de datos frecuente                         | Inmutabilidad preferida                              |
| Estado compartido   | Puede depender del contexto o variables externas    | Sin dependencias externas                            |
| Ejemplo de código   | `for`, `while`, variables temporales                | `map()`, `filter()`, funciones puras                 |

**Ejemplo imperativo**:
```js
let result = [];
for (let i = 0; i < numbers.length; i++) {
  if (numbers[i] > 10) {
    result.push(numbers[i]);
  }
}
```

**Ejemplo funcional**:
```js
let result = numbers.filter(n => n > 10);
```

## 🔹 ¿Cuándo es ventajoso usar funciones puras?
✅ Sí conviene:
- Cuando se necesita código predecible y fácil de probar.
- Para reutilización lógica en diferentes partes del sistema.
- En transformaciones de datos.

🚫 Menos útil:
- Cuando se interactúa con el DOM o se hacen llamadas a APIs.
- En tareas que dependen del tiempo o estado global.

## 🔹 Rol de `map()`, `filter()`, `find()` en la calidad del código
- Mejoran la legibilidad al expresar intenciones directamente.
- Reducen la complejidad al evitar bucles complejos.
- Fomentan un estilo declarativo y conciso.
- Facilitan el encadenamiento de operaciones.

🔹 Ejemplo con map() y filter():
```js
let precios = [10, 20, 30];
let conIVA = precios.map(p => p * 1.19);
let mayoresA25 = conIVA.filter(p => p > 25);
```

## 🔹 Por qué facilita testing y debugging
- Las funciones puras siempre devuelven el mismo resultado si se les dan los mismos datos.
- Se pueden probar de forma aislada, sin necesidad de contexto.
- Elimina los efectos secundarios, lo que hace más predecible el flujo del programa.

## 🔹 Cómo integrar el enfoque funcional en proyectos imperativos
- Comienza por identificar funciones repetidas y convertirlas en funciones puras.
- Usa métodos como map(), filter(), reduce() para transformar listas.
- Separa la lógica pura de la lógica con efectos secundarios (como actualizaciones del DOM).
- Refactoriza funciones para que solo dependan de sus argumentos.

## Ejemplo

✅ PRIMERO: Código con **enfoque imperativo**

Supongamos que tienes un sistema que calcula el total de egresos y muestra los nombres de los gastos mayores a $100. Todo se hace paso a paso con bucles y mutación de variables:

```js
// Lista original de movimientos
let movimientos = [
  { nombre: "Sueldo", monto: 1200, tipo: "ingreso" },
  { nombre: "Renta", monto: 600, tipo: "egreso" },
  { nombre: "Luz", monto: 80, tipo: "egreso" },
  { nombre: "Internet", monto: 150, tipo: "egreso" },
];

// Cálculo del total de egresos
let totalEgresos = 0;
for (let i = 0; i < movimientos.length; i++) {
  if (movimientos[i].tipo === "egreso") {
    totalEgresos += movimientos[i].monto;
  }
}
console.log("Total egresos:", totalEgresos);

// Obtener nombres de gastos mayores a 100
let gastosGrandes = [];
for (let i = 0; i < movimientos.length; i++) {
  if (movimientos[i].tipo === "egreso" && movimientos[i].monto > 100) {
    gastosGrandes.push(movimientos[i].nombre);
  }
}
console.log("Gastos mayores a 100:", gastosGrandes);
```

✅ SEGUNDO: El mismo ejemplo con **integración funcional progresiva**

Ahora vamos a refactorizar el código anterior integrando programación funcional, paso a paso, sin romper la lógica. Usamos funciones puras, métodos de orden superior y evitamos efectos secundarios.

```js
// Lista original de movimientos (sin cambios en los datos)
const movimientos = [
  { nombre: "Sueldo", monto: 1200, tipo: "ingreso" },
  { nombre: "Renta", monto: 600, tipo: "egreso" },
  { nombre: "Luz", monto: 80, tipo: "egreso" },
  { nombre: "Internet", monto: 150, tipo: "egreso" },
];

/* ---------- FUNCIONES PURAS ---------- */

// Verifica si un movimiento es egreso
const esEgreso = mov => mov.tipo === "egreso";

// Acumula montos
const sumarMontos = (total, mov) => total + mov.monto;

// Verifica si el monto es mayor a 100
const esMayorA100 = mov => mov.monto > 100;

// Extrae solo el nombre del movimiento
const obtenerNombre = mov => mov.nombre;

/* ---------- LÓGICA DECLARATIVA Y FUNCIONAL ---------- */

// Total de egresos (sin usar bucles, sin mutar variables)
const totalEgresos = movimientos
  .filter(esEgreso)        // Filtramos solo egresos
  .reduce(sumarMontos, 0); // Sumamos montos

console.log("Total egresos:", totalEgresos);

// Nombres de egresos mayores a 100
const gastosGrandes = movimientos
  .filter(esEgreso)        // Filtramos solo egresos
  .filter(esMayorA100)     // De esos, los mayores a 100
  .map(obtenerNombre);     // Extraemos solo el nombre

console.log("Gastos mayores a 100:", gastosGrandes);
```

✅ Beneficios concretos del cambio:

- Eliminamos los bucles manuales (for), usando .filter(), .map() y .reduce().
- Encapsulamos la lógica en funciones puras, reutilizables y testeables.
- Evitamos mutar variables (let) en la lógica de negocio.
- Hacemos el código más legible, expresivo y mantenible.