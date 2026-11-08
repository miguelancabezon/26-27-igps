# Evidencias de la entrega AEC-MD — PIVOT IA

## Documento y captura

- [README del proyecto](README.md).
- [Captura auténtica del README renderizado en GitHub](capturas/README-preview.png).
- [Enunciado vigente de la actividad](https://github.com/miguelancabezon/26-27-igps/blob/d3673fee7bbc9f018063ca112c67322fb0f55c18/actividades/eval-continua/md-aec.md).
- [Versión exacta del README capturado](https://github.com/nniheba/26-27-igps/blob/ef4f7b48b749349bc945fc9e8dc9f9f163975611/entregas/nicolas.herrera/AEC-MD/README.md).

La captura se obtuvo el 8 de noviembre de 2026 en la vista **Preview** de GitHub, con Brave. Muestra la cabecera, los tres badges, el logotipo y la presentación del documento final. Se convirtió el formato de imagen recibido a PNG, conservando sus dimensiones de 1905 × 961 píxeles; no se reconstruyó la interfaz ni se generó la imagen con IA. El quinto commit añade esta evidencia sin cambiar el README capturado.

SHA-256 de la captura PNG: `2dad3876ab772dbb799853c5920beda8b318a0fb6bcf7397f887aa2c13ebd394`.

## Cinco etapas de desarrollo

| Etapa | Aportación | Verificación |
| :---: | :--- | :--- |
| 1 | Presentación y logotipo | [4dfed2c](https://github.com/nniheba/26-27-igps/commit/4dfed2c7a13066b0f8b5e455d76c2ac07ec3d76c) |
| 2 | Índice, funcionalidades y lista de tareas | [d4bda37](https://github.com/nniheba/26-27-igps/commit/d4bda373c81daf9288a4914fba04ccc2a4479d6d) |
| 3 | Instalación, configuración y tabla de tecnologías | [e087d45](https://github.com/nniheba/26-27-igps/commit/e087d45e2af99baed184a04e52bb0bd55cf46fb1) |
| 4 | Arquitectura Mermaid, dos ejemplos de API y elementos avanzados | [ef4f7b4](https://github.com/nniheba/26-27-igps/commit/ef4f7b48b749349bc945fc9e8dc9f9f163975611) |
| 5 | Captura auténtica y este registro de evidencias | Último commit de la rama `docs/aec-md-pivot-ia` |

## Comprobaciones

- Comparación con `main` del profesor en `d3673fee7bbc9f018063ca112c67322fb0f55c18`.
- Cambios limitados a `entregas/nicolas.herrera/AEC-MD/`.
- Ocho enlaces del índice resuelven a encabezados del README.
- Logotipo local y tres badges visibles en GitHub.
- Tabla de seis tecnologías y bloques de código con lenguaje.
- Mermaid renderizado por GitHub, con las ramas de aprobación y revisión.
- Bloque HTML colapsable, comentario HTML, cita y caracteres escapados presentes.
- README final idéntico al documento local de origen; entrega preparada en un repositorio aislado.

Para reproducir la revisión desde una copia de la rama:

```bash
git log --reverse --oneline d3673fee7bbc9f018063ca112c67322fb0f55c18..HEAD
git diff --check d3673fee7bbc9f018063ca112c67322fb0f55c18 HEAD
git diff --name-status d3673fee7bbc9f018063ca112c67322fb0f55c18 HEAD
shasum -a 256 entregas/nicolas.herrera/AEC-MD/capturas/README-preview.png
```
