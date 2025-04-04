# Javascript: cuestionario

## 1. ¿Cuáles son los diferentes tipos de datos que se pueden utilizar en JavaScript y cómo se diferencian entre sí?

En JavaScript, hay varios tipos de datos que puedes utilizar, y se dividen en **tipos primitivos** y **tipos no primitivos (objetos)**. A continuación se explican los más comunes y cómo se diferencian:

### I. Tipos Primitivos
Los tipos primitivos son **inmutables**, lo que significa que su valor no puede ser cambiado una vez creado. Estos son:

- **`String`**: Representa secuencias de caracteres.  
    Ejemplo:  
    ```javascript
    let nombre = "Juan";
    ```

- **`Number`**: Representa tanto números enteros como decimales..  
    Ejemplo:  
    ```javascript
    let edad = 25;
    let altura = 1.75;
    ```

-  **`BigInt`**: Representa números enteros grandes, más allá de los límites de `Number`.
    Ejemplo:
    ```javascript
    let bigNumber = 9007199254740991n;
    ```

- **`Boolean`**: Representa un valor de verdadero o falso.
    Ejemplo:
    ```javascript
    let esActivo = true;
    ```

- **`undefined`**: Representa una variable declarada pero no inicializada.
    Ejemplo:
    ```javascript
    let valor;
    console.log(valor); // undefined
    ```

- **`null`**: Representa la ausencia intencional de un valor.
    Ejemplo:
    ```javascript
    let objeto = null;
    ```

- **`Symbol`**: Valor único e inmutable que se usa para identificar propiedades de objetos de forma única.
    Ejemplo:
    ```javascript
    let simbolo = Symbol('descripcion');
    ```

### II. Tipos No Primitivos (Objetos)
Los tipos no primitivos son objetos, y a diferencia de los primitivos, son mutables, es decir, sus valores pueden cambiar después de haber sido creados.

- **`Object`**: Tipo más general para colecciones de datos y funcionalidades.
    Ejemplo:
    ```javascript
    let persona = {
    nombre: "Juan",
    edad: 25,
    ciudad: "Madrid"
    };
    ```

- **`Array`**: Lista ordenada de valores.
    Ejemplo:
    ```javascript
    let frutas = ["manzana", "plátano", "cereza"];
    ```

- **`Function`**: Las funciones son objetos especiales que pueden almacenarse en variables y ejecutarse.
    Ejemplo:
    ```javascript
    function saludar() {
    console.log("Hola");
    }
    ```

JavaScript distingue entre datos primitivos y no primitivos según su comportamiento. Los primitivos son simples, inmutables y se manejan como valores directos. Los no primitivos son estructuras complejas, mutables y se manejan por referencia. Esta distinción afecta cómo se copian, comparan y modifican los datos.  

Comprender estas diferencias mejora el control del flujo del programa.  
Y permite escribir código más claro, eficiente y libre de errores.

---

## 2. ¿Cuáles son los diferentes tipos de datos que se pueden utilizar en JavaScript y cómo se diferencian entre sí?

Las estructuras `if` y `else` permiten tomar decisiones dentro de un programa.  
Evalúan una condición: si es verdadera, se ejecuta un bloque de código.  
Con `else`, se define una acción alternativa si la condición es falsa.  
También se puede usar `else if` para manejar múltiples opciones.  

Estas estructuras hacen que el programa sea dinámico y responda a diferentes situaciones.  
Son esenciales para controlar el flujo lógico de cualquier aplicación.

---

## 3. ¿Cuáles son los diferentes tipos de operadores en JavaScript y cómo se utilizan los operadores aritméticos para realizar cálculos?

En JavaScript, los **operadores** son símbolos que permiten realizar operaciones sobre valores y variables. Se clasifican en varios tipos según su función.

### 🧮 I. Operadores Aritméticos

Se usan para realizar **cálculos matemáticos**:

| Operador | Descripción       | Ejemplo       | Resultado |
|----------|-------------------|---------------|-----------|
| `+`      | Suma              | `5 + 3`       | `8`       |
| `-`      | Resta             | `5 - 3`       | `2`       |
| `*`      | Multiplicación    | `5 * 3`       | `15`      |
| `/`      | División          | `10 / 2`      | `5`       |
| `%`      | Módulo (resto)    | `10 % 3`      | `1`       |
| `**`     | Exponente         | `2 ** 3`      | `8`       |
| `++`     | Incremento        | `x++`         | `x + 1`   |
| `--`     | Decremento        | `x--`         | `x - 1`   |

### 💡 Ejemplo práctico

```javascript
    
    let a = 10;
    let b = 3;

    console.log(a + b);  // 13
    console.log(a - b);  // 7
    console.log(a * b);  // 30
    console.log(a / b);  // 3.333...
    console.log(a % b);  // 1
    console.log(a ** b); // 1000
```

### 🧩 II. Operadores de Asignación

Asignan valores a variables.

| Operador | Ejemplo   | Equivale a     |
|----------|-----------|----------------|
| `=`      | `x = 5`   | Asigna 5 a x   |
| `+=`     | `x += 2`  | `x = x + 2`    |
| `-=`     | `x -= 2`  | `x = x - 2`    |
| `*=`     | `x *= 2`  | `x = x * 2`    |
| `/=`     | `x /= 2`  | `x = x / 2`    |
| `%=`     | `x %= 2`  | `x = x % 2`    |

---

### 🔁 III. Operadores de Comparación

Comparan valores y devuelven `true` o `false`.

| Operador | Descripción       | Ejemplo                          |
|----------|-------------------|----------------------------------|
| `==`     | Igual             | `5 == '5'` → `true` (compara valor) |
| `===`    | Igual estricto    | `5 === '5'` → `false` (valor y tipo) |
| `!=`     | Distinto          | `5 != '5'` → `false`             |
| `!==`    | Distinto estricto | `5 !== '5'` → `true`             |
| `>`      | Mayor que         | `5 > 3`                          |
| `<`      | Menor que         | `5 < 3`                          |
| `>=`     | Mayor o igual     | `5 >= 5`                         |
| `<=`     | Menor o igual     | `3 <= 5`                         |

---

### 🔀 IV. Operadores Lógicos

Se usan para combinar condiciones.

| Operador | Nombre | Ejemplo                |
|----------|--------|------------------------|
| `&&`     | AND    | `true && false` → `false` |
| `||`     | OR     | `true || false` → `true`  |
| `!`      | NOT    | `!true` → `false`         |


### 🧠 ¿Cómo usar operadores aritméticos en un cálculo?

Por ejemplo, para calcular el área de un rectángulo:

```javascript
let base = 10;
let altura = 5;
let area = base * altura;

console.log("El área es:", area); // El área es: 50
```

---

## 4. ¿Cómo se declara una variable en JavaScript y cuáles son las diferencias entre var, let y const en cuanto a su alcance y mutabilidad?

# 🧠 Declaración de Variables en JavaScript

En JavaScript, las variables se pueden declarar utilizando tres palabras clave: `var`, `let` y `const`. La forma general de declarar una variable es:

```javascript
let nombre = "Juan";
```

### 🔹 Diferencias entre `var`, `let` y `const`

| Palabra clave | Alcance (`scope`) | Reasignable | Redeclarable | Uso recomendado         |
|---------------|-------------------|-------------|---------------|--------------------------|
| `var`         | Función           | ✅ Sí        | ✅ Sí          | ❌ Desaconsejado         |
| `let`         | Bloque (`{}`)     | ✅ Sí        | ❌ No          | ✅ Sí                    |
| `const`       | Bloque (`{}`)     | ❌ No        | ❌ No          | ✅ Sí (valor fijo)       |

---

### 📌 Detalles importantes

- **`var`**: Tiene alcance de función (*function scope*), lo que puede causar comportamientos inesperados en estructuras como bucles o condicionales. Además, permite redeclarar la misma variable, lo que puede sobrescribir valores sin intención.

- **`let`**: Tiene alcance de bloque (*block scope*) y no se puede redeclarar dentro del mismo bloque. Es ideal para variables que cambian su valor a lo largo del programa.

- **`const`**: También tiene alcance de bloque, pero no se puede reasignar su valor. Sin embargo, si se declara un objeto o arreglo con `const`, **sí se pueden modificar sus propiedades internas**.

---

### 💡 Ejemplo práctico

```javascript
function ejemplo() {
  if (true) {
    var x = 1;
    let y = 2;
    const z = 3;
  }

  console.log(x); // ✅ Funciona (var tiene alcance de función)
  // console.log(y); // ❌ Error (let tiene alcance de bloque)
  // console.log(z); // ❌ Error (const tiene alcance de bloque)
}
```

## ✅ Conclusión

Para escribir código moderno y seguro, se recomienda usar `let` para variables que cambian y `const` para valores fijos. El uso de `var` está obsoleto en la mayoría de los casos y puede provocar errores difíciles de detectar.