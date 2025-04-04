# 🚀 Conceptos Básicos de JavaScript 🚀

## 1. 🔄 ¿Qué es **"Control Flow"** (Control de Flujo)?

El **control de flujo** en programación se refiere a la manera en que se ejecutan las instrucciones dentro de un programa, determinando el orden en que se ejecutan. Utiliza estructuras como:

- Condicionales (`if`, `else`) ⚙️
- Bucles (`for`, `while`) 🔄
- Selección múltiple (`switch`) 🔀

Estas estructuras permiten tomar decisiones y repetir acciones según condiciones específicas. También se pueden usar instrucciones como `break` y `continue` para modificar la ejecución de los bucles.

```javascript
// Ejemplo de control de flujo con condicional
let hora = 14;

if (hora < 12) {
    console.log("¡Buenos días! ☀️");
} else if (hora < 18) {
    console.log("¡Buenas tardes! 🌤️");
} else {
    console.log("¡Buenas noches! 🌙");
}

// Ejemplo de bucle for
for (let i = 1; i <= 3; i++) {
    console.log(`Iteración ${i} 🔁`);
}
```

En resumen, el control de flujo permite que un programa sea dinámico y responda a diferentes situaciones o entradas de manera flexible y eficiente.

---

## 2. 📋 ¿Qué es una "function" (Función) de JavaScript?

Una función en JavaScript es un bloque de código reutilizable diseñado para realizar una tarea específica. Las funciones permiten:

- Organizar el código de manera más eficiente ✅
- Crear componentes reutilizables 🔄
- Recibir entradas a través de parámetros 📥
- Proporcionar un resultado o valor de retorno 📤

Las funciones se crean con la palabra clave `function`, seguida de un nombre, los parámetros entre paréntesis y un bloque de código entre llaves.

```javascript
// Declaración de función básica
function saludar(nombre) {
    console.log("Hola, " + nombre + " 👋");
}
 
saludar("Juan");  // Imprime "Hola, Juan 👋"

// Función con valor de retorno
function sumar(a, b) {
    return a + b;  // Devuelve la suma de los dos números
}

let resultado = sumar(5, 3);
console.log(`El resultado es ${resultado} 🧮`);  // Imprime "El resultado es 8 🧮"
```

Las funciones mejoran la estructura, organización y mantenibilidad del código al dividirlo en piezas más pequeñas y manejables.

---

## 3. 🔁 ¿Cuántas veces se ejecutará un bucle "while"?

Un bucle `while` en JavaScript se ejecutará mientras la condición especificada sea verdadera. La cantidad de repeticiones depende completamente de cuándo esa condición se vuelva falsa.

- Si la condición inicial es falsa, el bucle no se ejecutará ni una sola vez ❌
- Si la condición nunca cambia a falsa, el bucle continuará de manera indefinida (bucle infinito) ⚠️
- Si la condición eventualmente se vuelve falsa, el bucle se detendrá ✋

```javascript
// Ejemplo de bucle while que se ejecuta 5 veces
let i = 0;
while (i < 5) {
    console.log(`Iteración ${i} 🔄`);
    i++;  // Incrementa i en cada iteración
}

// Ejemplo con condición que depende de entrada externa
let intentos = 0;
let contraseñaCorrecta = false;

while (!contraseñaCorrecta && intentos < 3) {
    // Simular verificación de contraseña
    let intento = prompt("Introduce tu contraseña 🔑");
    
    if (intento === "secreto") {
        contraseñaCorrecta = true;
        console.log("¡Acceso concedido! ✅");
    } else {
        intentos++;
        console.log(`Contraseña incorrecta. Intentos restantes: ${3 - intentos} ⚠️`);
    }
}
```

En el primer ejemplo, el bucle se ejecutará exactamente 5 veces, ya que la condición `i < 5` se vuelve falsa cuando `i` llega a 5.

---

## 4. 📚 ¿Qué método usarías para agregar un elemento al final de un array y cómo se utiliza?

El método `push()` se utiliza para agregar uno o más elementos al final de un array. Este método modifica el array original y devuelve la nueva longitud del array.

```javascript
// Ejemplo de bucle while que se ejecuta 5 veces
let i = 0;
while (i < 5) {
    console.log(`Iteración ${i} 🔄`);
    i++;  // Incrementa i en cada iteración
}

// Ejemplo con condición que depende de entrada externa
let intentos = 0;
let contraseñaCorrecta = false;

while (!contraseñaCorrecta && intentos < 3) {
    // Simular verificación de contraseña
    let intento = prompt("Introduce tu contraseña 🔑");
    
    if (intento === "secreto") {
        contraseñaCorrecta = true;
        console.log("¡Acceso concedido! ✅");
    } else {
        intentos++;
        console.log(`Contraseña incorrecta. Intentos restantes: ${3 - intentos} ⚠️`);
    }
}
```

El método `push()` es muy útil para la gestión dinámica de colecciones de datos, permitiendo añadir nuevos elementos de forma sencilla y eficiente.