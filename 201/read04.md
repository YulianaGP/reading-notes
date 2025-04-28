# 📚 Tarea de Desarrollo Web

## 🎨 ¿Cómo difieren las **Component Classes** y **Utility Classes** en su uso diario?

- <span style="color:#4CAF50">**Component Classes**</span> agrupan varios estilos en una sola clase para un componente completo (ej. `card`, `button`, `navbar`).
- <span style="color:#2196F3">**Utility Classes**</span> aplican estilos muy específicos y pequeños (ej. `mt-4`, `text-center`, `bg-red-500`).

🔎 **En uso diario**:
- **Component Classes** permiten **reutilizar** componentes completos de forma rápida.
- **Utility Classes** brindan **flexibilidad** para crear diseños únicos sin escribir CSS extra.

---

## 🚀 ¿Cuándo es más eficiente utilizar **Component Classes** en lugar de **Utility Classes**?

- Cuando necesitas **consistencia visual** en todo el proyecto.
- Al desarrollar **sistemas de diseño** o **componentes estándar** (botones, formularios, tarjetas).
- Ideal para equipos grandes donde se requiere un diseño **unificado**.

---

## 👀 ¿Cómo afecta el uso de **Utility Classes** a la legibilidad del código?

- 🔥 **Pros**: Cada clase describe claramente qué estilo aplica.
- ⚡ **Contras**: Puede hacer que los archivos HTML se vean **sobrecargados** o difíciles de leer si no se organizan bien.
  
👉 Una buena práctica es **combinar** clases relacionadas o usar componentes pequeños para mantener la claridad.

---

## 🛠️ ¿En qué tipos de proyectos prefieres usar **Bootstrap**? ¿Por qué?

Prefiero usar Bootstrap en:
- 🏢 **Proyectos corporativos** donde la prioridad es la rapidez de desarrollo.
- 🛒 **E-commerce** y **dashboards** donde ya existen patrones UI prediseñados.
- 🌐 **Páginas institucionales** donde no se requiere un diseño altamente personalizado.

✨ ¿Por qué? Porque Bootstrap ofrece una **base sólida** y **responsiva** de inmediato.

---

## 🌟 ¿Cuáles son las ventajas principales de **Tailwind CSS** frente a otros frameworks?

- 🎯 **Flexibilidad total** para personalizar estilos.
- ⚡ **Rendimiento optimizado** (solo cargas lo que usas).
- 🧩 **Componentización sencilla** compatible con frameworks modernos (React, Vue, etc).
- 🛠️ Facilita la creación de **diseños únicos** sin sobreescribir estilos predefinidos.

---

## ⏱️ ¿Cómo impacta la elección del framework en el tiempo de desarrollo?

- Un framework bien elegido puede **acelerar** el proyecto hasta en un **50%** 🚀.
- Frameworks como Bootstrap **reducen el tiempo inicial**, pero pueden **limitar la personalización** después.
- Tailwind **requiere configuración inicial**, pero **acelera el diseño** en fases avanzadas.

👉 **Conclusión**: La elección depende de las **necesidades** y **prioridades** del proyecto.

---

## 🌳 ¿Por qué es esencial usar ramas en **Git** al trabajar en equipos?

- 🧹 Mantiene el **código principal limpio** y **estable**.
- 🎯 Permite trabajar en **múltiples features** o **correcciones** simultáneamente.
- 👥 Facilita la **colaboración** y el **control de versiones** de cada funcionalidad nueva.

---

## 🧩 ¿Cómo ayuda el uso de ramas a mantener la estabilidad del código principal?

- Todas las nuevas características y cambios se prueban en ramas **aparte** antes de fusionarse.
- Se puede aplicar un **control de calidad** (tests, revisiones de código) antes de integrar cambios a `main`.
- Evita errores en producción 🚫🐛.

---

## 🧠 ¿Qué desafíos has enfrentado al fusionar ramas y cómo los resolviste?

### 🔥 Desafíos:
- **Conflictos de merge**: dos ramas modificaron la misma línea de código.
- **Desincronización**: ramas que no se actualizaron frecuentemente con `main`.

### 🛠️ Soluciones:
- Hacer `pull` regularmente del `main` a la rama en desarrollo.
- Resolver conflictos usando **herramientas de comparación visual** (ej. VSCode, GitKraken).
- Revisar cuidadosamente los **archivos conflictivos** antes de confirmar (`commit`) la
