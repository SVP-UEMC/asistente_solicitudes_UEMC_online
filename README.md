# Chat Tramitación Solicitudes UEMC

Aplicación web que integra el agente tipo chatbot guiado **Tramitación de Solicitudes UEMC**, desarrollado en Copilot Studio y publicado como canal web mediante GitHub Pages.

La aplicación proporciona una interfaz web propia, replicando la experiencia visual del asistente guiado por opciones, mientras mantiene un comportamiento conversacional basado en normativa universitaria.

---

## Descripción general

Este proyecto no contiene lógica de negocio ni normativa universitaria.

Toda la inteligencia conversacional, validación de trámites, control de respuestas y uso del conocimiento se gestiona exclusivamente en **Copilot Studio**.

La aplicación web se encarga únicamente de:
- Presentar la interfaz de usuario.
- Conectar con el agente mediante Bot Framework Web Chat.
- Mostrar la conversación al usuario final.

---

## Arquitectura

GitHub Pages (HTML / CSS / JavaScript)  
↓  
Bot Framework Web Chat  
↓  
Copilot Studio (Agente conversacional)

La web no toma decisiones.  
El agente no renderiza interfaz.  
Cualquier cambio funcional debe realizarse en Copilot Studio.

---

## Estructura del proyecto

/
├─ index.html      Estructura de la interfaz  
├─ styles.css      Estilos visuales (colores, tipografía, layout)  
├─ app.js          Inicialización de Web Chat y conexión con el agente  
└─ README.md

---

## Configuración

La conexión con el agente se realiza mediante **Direct Line**.

Los identificadores y tokens necesarios se configuran en el archivo `app.js`.

Importante:  
No se deben incluir secretos directamente en el repositorio en entornos productivos.  
Para producción se recomienda generar tokens dinámicamente desde un backend intermedio.

---

## Despliegue

La aplicación se publica utilizando **GitHub Pages**:

- Repositorio público.
- Rama `main`.
- Publicación desde la raíz del proyecto.

La URL final es proporcionada por GitHub Pages.

---

## Buenas prácticas

- No duplicar lógica del agente en JavaScript.
- No introducir validaciones de trámites en la web.
- No modificar el comportamiento conversacional desde este proyecto.
- Mantener los estilos visuales desacoplados del contenido.

---

## Mantenimiento

Cambios de contenido, normativa o comportamiento → Copilot Studio  
Cambios visuales o de experiencia de usuario → styles.css / index.html  
Cambios de integración técnica → app.js

---

## Estado del proyecto

Agente conversacional validado.  
Conocimiento normativo centralizado.  
Interfaz web desacoplada y controlada.  
Listo para uso en entorno real.
