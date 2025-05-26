## ☑️ Lista de Mitos y Verdades Analizada

---

### ❌ Mito  
**Usar `querySelector()` siempre devuelve una colección de nodos, incluso si selecciona uno solo.**

**Justificación:**  
`querySelector()` devuelve un único nodo (el primero que coincida con el selector). Si se desea una colección, se debe usar `querySelectorAll()`.

---

### ✅ Verdad  
**El DOM permite manipular estilos CSS directamente desde JavaScript usando propiedades específicas como `.style` y `.classList`.**

**Justificación:**  
Puedes cambiar estilos en línea con `.style` (`element.style.color = 'red'`) o modificar clases con `.classList` (`element.classList.add('activo')`).

---

### ❌ Mito  
**Una expresión regular (Regex) siempre devolverá el mismo resultado sin importar el contexto o idioma del texto que analice.**

**Justificación:**  
El comportamiento de Regex puede cambiar dependiendo de:
- Modificadores usados (`i`, `g`, `u`)
- Codificación del texto (UTF-8, ASCII)
- Idioma si hay uso de propiedades Unicode como `\p{L}` con la bandera `u`

---

### ✅ Verdad  
**Utilizar `querySelectorAll()` es menos eficiente que `getElementById` cuando se busca un único elemento por su ID.**

**Justificación:**  
`getElementById()` está optimizado para búsquedas por ID. `querySelectorAll()` debe interpretar un selector CSS completo, lo cual consume más recursos.

---

### ❌ Mito  
**Todos los métodos del DOM devuelven elementos del mismo tipo, no existen diferencias entre ellos.**

**Justificación:**  
- `getElementById()` devuelve un único elemento o `null`.  
- `getElementsByClassName()` devuelve una HTMLCollection viva.  
- `querySelectorAll()` devuelve una NodeList estática.  
- `querySelector()` devuelve un solo nodo.

Cada uno tiene distinto tipo de retorno y comportamiento.

---

### ✅ Verdad  
**`querySelectorAll()` permite seleccionar múltiples elementos y devuelve una lista estática (no viva) de nodos.**

**Justificación:**  
Una NodeList estática no se actualiza si el DOM cambia después de ejecutarla. A diferencia de colecciones vivas, como las de `getElementsByClassName()`.

---

### ✅ Verdad  
**Las expresiones regulares (Regex) se pueden utilizar para transformar contenido de texto (Markdown a HTML, por ejemplo) sin necesidad de librerías externas.**

**Justificación:**  
Es posible crear transformaciones básicas de Markdown a HTML (como convertir `**texto**` en `<strong>texto</strong>`) utilizando Regex. Aunque para conversiones complejas es recomendable usar librerías.

---

### ❌ Mito  
**Los cambios realizados en los nodos del DOM usando JavaScript son permanentes incluso después de refrescar la página.**

**Justificación:**  
Los cambios hechos con JavaScript en el DOM son temporales. Al recargar la página, el DOM se reconstruye desde el HTML original. Para persistencia, se requiere localStorage, cookies o bases de datos.

---

## ✅ Conclusión

Este análisis demuestra que:

- No todos los métodos del DOM son iguales, ni devuelven el mismo tipo de dato.
- Regex es una herramienta poderosa, pero su comportamiento depende del contexto y configuración.
- Las manipulaciones en el DOM son efímeras a menos que se combinen con almacenamiento persistente.
- Elegir correctamente la API adecuada influye en el rendimiento, la legibilidad y la escalabilidad del código.

Comprender estas diferencias permite escribir código más robusto, claro y eficiente en aplicaciones frontend modernas.
