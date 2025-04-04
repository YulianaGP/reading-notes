# Read 11: El DOM y JavaScript

## Preguntas y Respuestas

### 1. ¿Qué es el DOM?

El Modelo de Objeto del Documento (DOM) es una forma en la que los navegadores organizan y entienden el contenido de una página web escrita en HTML o XML. Gracias al DOM, los programadores pueden ver la página como una estructura formada por "bloques" o elementos, como títulos, párrafos, imágenes, etc. Esta estructura permite que los lenguajes de programación, como JavaScript, puedan acceder a esos elementos para cambiarlos, moverlos o darles estilo. En resumen, el DOM es el puente que conecta una página web con el código que la hace interactiva.

---

### 2. Describe brevemente la relación entre el DOM y JavaScript

El DOM y JavaScript trabajan juntos para hacer que las páginas web sean interactivas. El DOM organiza el contenido de la página como una estructura que JavaScript puede entender. Gracias a eso, JavaScript puede buscar, leer y cambiar elementos de la página, como textos, imágenes o botones. Aunque son tecnologías diferentes, se complementan: el DOM guarda la información de la página, y JavaScript se encarga de manipular esa información.

---

### 3. ¿Qué método usarías para seleccionar un elemento del DOM por su ID y cómo se utiliza?

```javascript
document.getElementById("table");

**Explicación del código**: `document` hace referencia a toda la página. `getElementById("table")` busca el elemento que tenga ese ID.

---

### 4. ¿Qué método utilizarías para cambiar el color de fondo de un elemento en el DOM y cómo se implementaría?

```javascript
let variable = document.getElementById("table");
variable.style.backgroundColor = "lightblue";

**Explicación**: se está creando una variable llamada `variable` y está buscando el nombre de un elemento `table` que está en el html. Luego, a la variable ya creada se le va a aplicar un color de fondo celeste.
