# ¿Cómo funciona la web?

La web es un sistema de información global que permite a los usuarios acceder y compartir contenido a través de internet. Funciona mediante la comunicación entre *clientes* (como navegadores web) y *servidores* (donde se almacenan los sitios web). Esta comunicación se basa en protocolos como *HTTP* y *HTTPS*.

Cuando un usuario ingresa una URL en su navegador, ocurre lo siguiente:

1. *El navegador envía una solicitud HTTP* al servidor web.
2. *El servidor procesa la solicitud* y envía los archivos del sitio web (HTML, CSS, JavaScript).
3. *El navegador interpreta y muestra la página web* en la pantalla del usuario.

---

# Partes esenciales de la web

## 1. Cliente (Navegador Web)
Es la aplicación que permite a los usuarios acceder a sitios web. Ejemplos: *Google Chrome, Firefox, Safari*.

## 2. Servidor Web
Es el equipo que almacena y entrega las páginas web. Ejemplos: *Apache, Nginx*.

## 3. Protocolo HTTP/HTTPS
Es el sistema de comunicación que permite la transferencia de datos entre cliente y servidor.

## 4. DNS (Sistema de Nombres de Dominio)
Convierte nombres de dominio (ej. www.ejemplo.com) en direcciones IP.

## 5. Lenguajes de Programación Web
Las páginas web están construidas con tecnologías como *HTML, CSS y JavaScript*.

---

# Ejemplo de una solicitud HTTP

Cuando visitas una página web, tu navegador realiza una solicitud HTTP como esta:

```http
GET /index.html HTTP/1.1
Host: www.ejemplo.com
User-Agent: Mozilla/5.0