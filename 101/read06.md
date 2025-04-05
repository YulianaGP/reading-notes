# 📝 Comandos en la Terminal de Linux/macOS

---

## 1️⃣ ¿Qué hacen los siguientes comandos?

- **`pwd`**: Muestra la ruta del directorio actual.  
- **`ls`**: Lista los archivos y carpetas del directorio actual.  
- **`cd`**: Cambia de directorio.  
- **`mkdir`**: Crea una nueva carpeta.  
- **`touch`**: Crea un archivo vacío.

---

## 2️⃣ ¿Qué sucede en el siguiente escenario si ingresas estos comandos y argumentos en la línea de comandos?

**Comandos:**

```bash
cd projects
mkdir new-project
touch new-project/newfile.md
cd ..
ls projects/new-project
```

Después de ejecutar estos comandos, habrás creado una carpeta llamada `new-project` dentro de `projects`, creado un archivo vacío `newfile.md` dentro de esa carpeta y luego listado el contenido de `new-project` que contiene `newfile.md`.

---

## 3️⃣ ¿Qué comando usarías en la terminal para listar todos los archivos, incluidos los archivos ocultos, en un directorio de Linux o macOS?

**Comando:**

```bash
ls -a
```

### Explicación de los parámetros

- **`ls`**: Lista los archivos y carpetas del directorio actual.
- **`-a`** (o `--all`): Muestra todos los archivos, incluidos los archivos ocultos (que comienzan con un punto, como `.git` o `.bashrc`).

Este comando te permite ver tanto los archivos normales como los ocultos en un directorio.
