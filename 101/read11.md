# 🌟 **Read 11: El DOM y JavaScript** 🌟

## 📝 **Preguntas y Respuestas**

### 1. 🤔 **¿Qué es el DOM?**

El **Modelo de Objeto del Documento (DOM)** 🌐 es una representación estructurada que los navegadores crean para interpretar el contenido de una página web escrita en **HTML** o **XML**. El DOM transforma cada elemento de la página en un "nodo" dentro de una estructura jerárquica en forma de árbol 🌳, permitiendo que los desarrolladores accedan, manipulen y modifiquen dinámicamente estos elementos mediante lenguajes como **JavaScript**. Esta estructura organizada facilita la interacción programática con los componentes de la página, convirtiendo documentos estáticos en interfaces interactivas y dinámicas. En esencia, el DOM funciona como la interfaz crucial entre el código HTML estático y el comportamiento dinámico implementado a través de JavaScript.

---

### 2. 🔄 **Describe brevemente la relación entre el DOM y JavaScript**

El **DOM** y **JavaScript** mantienen una relación simbiótica fundamental para la web moderna. El DOM proporciona una representación estructurada y accesible de los documentos web 📄, mientras que JavaScript aporta las capacidades de programación necesarias para manipular esa estructura ⚙️. JavaScript utiliza el DOM como una API para acceder, modificar, añadir o eliminar elementos de la página en tiempo real. Esta interacción permite crear experiencias web dinámicas e interactivas sin necesidad de recargar la página. JavaScript puede escuchar eventos de usuario (como clics 🖱️ o pulsaciones de teclas ⌨️), responder a ellos y actualizar selectivamente el contenido de la página a través de la interfaz que proporciona el DOM, estableciendo así un ecosistema donde el contenido estático cobra vida gracias a la programación.

---

### 3. 🔍 **¿Qué método usarías para seleccionar un elemento del DOM por su ID y cómo se utiliza?**


```document.getElementById("table");```

**Explicación del código**: `document` hace referencia a toda la página. `getElementById("table")` busca el elemento con el ID "table".

---

### 4. 🎨 **¿Qué método utilizarías para cambiar el color de fondo de un elemento en el DOM y cómo se implementaría?**

**Explicación del código**: se está creando una variable llamada `variable` que busca el elemento ID `table` en el HTML. Luego, a esa variable se le cambia el color de fondo a celeste.

```javascript
let variable = document.getElementById("table");
variable.style.backgroundColor = "lightblue";
