# *Trámita* 📖 📌
![Estado](https://img.shields.io/badge/estado-en%20desarrollo-orange)
![Licencia](https://img.shields.io/badge/licencia-MIT-blue)

*Tu asistente para los trámites de extranjería.*

## Índice

- [Presentación del proyecto](#presentación-del-proyecto)
  - [El problema](#el-problema)
  - [La solución](#la-solución)
  - [Objetivo principal](#objetivo-principal)
- [Características principales](#características-principales)
- [Instalación y configuración](#instalación-y-configuración)
- [Tecnologías utilizadas](#tecnologías-utilizadas)
- [Arquitectura y funcionamiento](#arquitectura-y-funcionamiento)
- [Ejemplos de uso](#ejemplos-de-uso)
- [Información adicional](#información-adicional)
- [Contacto](#contacto)

## Características principales

- [x] **Itinerario personalizado** según el perfil del usuario
  - [x] Nacionalidad y tipo de visado
  - [x] Provincia de residencia
- [x] **Checklist de documentos** para cada trámite
- [ ] **Avisos de plazos** antes de que venzan
  - [ ] Notificaciones por correo
  - [ ] Notificaciones en el móvil
- [ ] **Formularios prerrellenados** (por ejemplo, `EX-17`)
- [ ] **Seguimiento del estado** de cada trámite
- [ ] **Paquete para EE. UU.** (planificado a futuro)

## Presentación del proyecto

**Trámita** es una aplicación web y móvil que guía a los *estudiantes extranjeros* paso a paso por los trámites administrativos necesarios para estudiar en España. Convierte un proceso confuso en una **lista de tareas clara, con plazos y avisos**.

### El problema

Un estudiante que llega a España con visado de estudios tiene que obtener su **TIE** (Tarjeta de Identidad de Extranjero) en un plazo de `30 días` desde su llegada. Para ello debe pedir cita, rellenar formularios, pagar una tasa y reunir documentos, y la información está **dispersa en webs distintas** y cambia según la provincia. Un error o un retraso puede dejarle en situación irregular.

### La solución

Trámita pregunta al usuario por su situación (nacionalidad, visado, fecha de llegada) y le genera un **itinerario personalizado** con:

- Los documentos que necesita, en forma de checklist.
- Los plazos calculados, con avisos antes de que venzan.
- El formulario preparado para revisar y presentar.

### Objetivo principal

Reducir el tiempo y la incertidumbre de la burocracia migratoria para que el estudiante se centre en lo importante: **estudiar y adaptarse a su nueva vida**.
