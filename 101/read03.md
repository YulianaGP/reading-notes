# 🎨 CSS - Hojas de Estilo en Cascada

## 📌 Etimología
Cascading Style Sheets (Hojas de estilo en cascada)

## 🎯 Reglas Básicas
Las reglas en CSS siguen la estructura:
```css
propiedad: valor;
```
Ejemplo:
```css
color: blue; /* 🎨 Color del texto */
background-color: yellow; /* 🟨 Color del fondo */
text-decoration: underline; /* 🔽 Subrayado */
font-size: 80px; /* 🔠 Tamaño de la fuente */
font-weight: 800; /* 💪 Grosor (100 - 900) */
margin-bottom: 15px; /* 📏 Espacio inferior */
margin-top: 15px; /* 📏 Espacio superior */
```

## 🛠️ Uso
Se debe colocar dentro de la etiqueta `<style>` dentro del `<head>`:
```html
<head>
  <style>
    p {
      color: blue;
    }
  </style>
</head>
```

---

## 🔄 Normalización en CSS
Para quitar los estilos por defecto:
```css
* {
  margin: 0;
  padding: 0;
}
```

✅ `margin`: Espacio exterior entre elementos.
✅ `padding`: Espacio interior dentro de un elemento.

---

## 🎯 Cómo Centrar Elementos con Flexbox
Flexbox ayuda a centrar elementos de forma sencilla:
```css
display: flex;
align-items: center;
justify-content: center;
height: 100vh;
```
👉 Permite distribuir elementos en filas o columnas y alinearlos fácilmente.

---

## 🎭 Especificidad en CSS
Para diferenciar estilos entre etiquetas iguales, se pueden usar **ID** o **Clases**:

🔹 **Ejemplo con ID**
```html
<p id="subtitulo">Este es mi subtitulo</p>
```

🔹 **Ejemplo con Clase**
```html
<p class="nombre">Este es otro subtitulo</p>
```
📌 **Recomendaciones:**
- ✅ Usa **ID** (`#`) si el elemento es único.
- ✅ Usa **Clases** (`.`) si el estilo se repetirá.

---

## 🔤 Uso de Fuentes Externas (Google Fonts)
Pasos para cambiar la fuente:
1️⃣ Busca "Google Fonts" en el navegador.
2️⃣ Selecciona la fuente deseada (ej. Nunito).
3️⃣ Copia el código de `link` y agrégalo en `<head>`:
```html
<link href="https://fonts.googleapis.com/css2?family=Nunito&display=swap" rel="stylesheet">
```
4️⃣ Luego, aplica la fuente en CSS:
```css
h1 {
  font-family: "Nunito", sans-serif;
}
```

---

## 📌 Selectores en CSS
### 🔹 Tipos de Selectores
| Selector | Descripción | Ejemplo |
| --- | --- | --- |
| `*` | Universal (todos los elementos) | `* { margin: 0; }` |
| `p` | Todos los `<p>` | `p { color: red; }` |
| `#id` | Elemento con ID específico | `#nombre { color: green; }` |
| `.clase` | Elementos con clase específica | `.mi-clase { font-size: 20px; }` |
| `div p` | Todos los `<p>` dentro de `<div>` | `div p { color: blue; }` |
| `div > p` | Solo `<p>` hijos directos de `<div>` | `div > p { color: red; }` |
| `h1 + p` | `<p>` inmediatamente después de `<h1>` | `h1 + p { color: purple; }` |
| `h1 ~ p` | Todos los `<p>` después de `<h1>` | `h1 ~ p { color: orange; }` |
| `[atributo]` | Elementos con un atributo específico | `input[type="text"] { border: blue; }` |
| `:hover` | Efecto al pasar el mouse | `button:hover { background: yellow; }` |
| `:nth-child(2)` | Segundo hijo de un contenedor | `li:nth-child(2) { color: blue; }` |
| `::before` | Contenido antes de un elemento | `h1::before { content: "🔥"; }` |

---

## 📌 `<main>` en CSS
Solo puede haber un `<main>` por documento HTML.
Ejemplo de estilos para `<main>`:
```css
main {
  height: 250px; /* 📏 Altura */
  width: 100px; /* 📏 Ancho */
  border: 1px solid black; /* 🖍️ Borde */
  background-color: skyblue; /* 🎨 Color de fondo */
  border-radius: 25px; /* 🔵 Bordes redondeados */
}
```

---

## ✉️ Íconos en Correo y Ubicación
Para agregar íconos de correo y ubicación:

🔹 **HTML**
```html
<p><i class="fas fa-envelope"></i> <a href="mailto:yulianagiron326@gmail.com">yulianagiron326@gmail.com</a></p>
<p><i class="fas fa-map-marker-alt"></i> Villa el Salvador, Lima</p>
```

🔹 **Agrega este link en `<head>`** para habilitar FontAwesome:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
```

---

✅ **CSS es poderoso y versátil. ¡Experimenta con estos estilos!** 🚀