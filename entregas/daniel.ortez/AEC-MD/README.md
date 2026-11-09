# Bot de Administración y Moderación para Telegram

Este proyecto es un bot automatizado para administrar grupos y comunidades de Telegram, desarrollado con Node.js y TypeScript.

La idea de este proyecto surge para solucionar la gestión manual del spam en grupos grandes, la bienvenida de nuevos integrantes y el control de comandos de moderación. El bot permite filtrar mensajes no deseados con reglas personalizadas, aplicar sanciones como advertencias o silenciar usuarios, y responder a eventos mediante webhooks.

![Captura del Bot](https://via.placeholder.com/800x400.png?text=Vista+Previa+del+Bot)

---

## Indice de contenidos

- [Funcionalidades principales](#funcionalidades-principales)
- [Pasos de instalacion y configuracion](#pasos-de-instalacion-y-configuracion)
- [Tecnologias utilizadas](#tecnologias-utilizadas)
- [Arquitectura del sistema](#arquitectura-del-sistema)
- [Ejemplos de codigo y uso](#ejemplos-de-codigo-y-uso)
- [Notas y datos adicionales](#notas-y-datos-adicionales)
- [Contacto y soporte](#contacto-y-soporte)

---

## Funcionalidades principales

* **Sistema de filtrado anti-spam:**
  * Revisa enlaces sospechosos y mensajes reenviados de forma masiva.
  * Aplica un silenciado temporal o expulsión directa según la regla configurada.
* **Control de acceso y bienvenida:**
  * Envía un mensaje automático de bienvenida a quienes entran al grupo.
  * Muestra un botón de verificación simple para comprobar que el usuario no es una cuenta automatizada.
* **Estado de las tareas del proyecto:**
  - [x] Estructura base del proyecto conectada a la API de Telegram con Telegraf.
  - [x] Implementación de comandos básicos de moderación (`/ban`, `/mute`, `/warn`).
  - [ ] Integración con base de datos PostgreSQL para almacenar el historial de sanciones.
  - [ ] Creación de una pequeña interfaz web para ver métricas del grupo.

---

## Pasos de instalacion y configuracion

Para probar o desplegar el proyecto en un entorno local, sigue estos pasos:

1. Clona el repositorio en tu equipo:
   ```bash
   git clone [https://github.com/usuario/telegram-automod-bot.git](https://github.com/usuario/telegram-automod-bot.git)
   cd telegram-automod-bot
