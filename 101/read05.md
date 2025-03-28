# DevTools

Las herramientas de desarrollo más adecuadas para nuestro trabajo son los **IDE** (*Integrated Development Environment*).

## 🔧 ¿Qué es un IDE?
Un **IDE** es un software que proporciona un conjunto de herramientas para facilitar la programación y el desarrollo de software en un solo lugar. Permite organizar archivos y gestionar cambios en el código con herramientas como **Git**.

## 💻 IDEs populares

| IDE                  | Lenguaje principal          | Gratuito |
|----------------------|----------------------------|----------|
| **Visual Studio Code**  | Múltiples lenguajes        | Sí       |
| PyCharm             | Python                     | Versión gratuita y de pago |
| Eclipse            | Java                        | Sí       |
| IntelliJ IDEA      | Java y otros lenguajes     | Versión gratuita y de pago |
| Android Studio     | Desarrollo móvil (Android) | Sí       |
| WebStorm           | JavaScript/TypeScript      | No       |

---

# 🔨 Visual Studio Code

Para mejorar la experiencia en **VS Code**, se recomienda instalar las siguientes extensiones:

| Extensión              | Propósito |
|------------------------|-----------|
| SynthWave ‘84         | Tema visual |
| Material Icon Theme   | Mejora los íconos |
| Live Server           | Permite ver el avance de la página en tiempo real |

### ⚠️ Nota:
Para activar el **autoguardado**, haz click en *File* > *Auto Save*.

---

# 🎮 Node.js

Es un entorno de ejecución para JavaScript en el servidor.

### 🚨 Problemas en la instalación
Para verificar si Node.js está instalado correctamente:
```bash
node --version
```
Si no funciona, intenta:
1. Abrir la terminal (**Windows CMD** o **Git Bash**).
2. Escribir el comando anterior y presionar *Enter*.

---

# 🔄 Git - Control de versiones

**Git** permite gestionar diferentes versiones de un proyecto.

### ⚙️ Configuración de Git Bash con GitHub

Ejecuta los siguientes comandos en **Git Bash**:
```bash
git config --global user.name 'TU NOMBRE COMPLETO'
git config --global user.email 'TU CORREO ELECTRÓNICO'
git config --global core.editor "code --wait"
git config --global init.defaultbranch main
```

### 🛠️ Asociar Git con GitHub

1. Crea un repositorio en **GitHub**.
2. Copia la URL del repositorio.
3. En Git Bash, dentro del proyecto, ejecuta:
```bash
git init
git remote add origin URL_DEL_REPOSITORIO
touch README.md
git add .
git commit -m "Primer commit"
git push -u origin main
```
4. Verifica que los archivos aparezcan en GitHub.

---

# 📝 Comandos esenciales de Git Bash

| Comando                 | Descripción |
|-------------------------|-------------|
| `mkdir carpeta`         | Crea una nueva carpeta |
| `cd carpeta`           | Entra a la carpeta |
| `cd ..`                | Retrocede un nivel |
| `touch archivo.txt`     | Crea un archivo vacío |
| `ls`                   | Lista los archivos de la carpeta |
| `pwd`                  | Muestra la ruta actual |
| `start .`              | Abre la carpeta en el explorador |
| `rm -r carpeta`        | Elimina una carpeta |
| `code .`               | Abre VS Code en la carpeta actual |

---

# 🔍 Conclusión
Para verificar que todos los programas y configuraciones están correctos, ejecuta:
```bash
curl -s https://raw.githubusercontent.com/entertechschool/setup-guide/main/configs/verify.sh | bash
```
Esto verificará que tienes **VS Code**, **Git**, **Node.js** y **npm** correctamente instalados.
