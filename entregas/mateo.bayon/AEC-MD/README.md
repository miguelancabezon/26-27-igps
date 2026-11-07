# PetHome Initiative

Esta iniciativa tiene como objetivo principal darle un hogar a cientos de mascotas que actualmente se encuentran sin hogar a través del internet con la ayuda de la comunidad.

![Interfaz principal de PetHome](assets/petHomeInitiativeLogo.png)

## 1. Presentación del proyecto

**PetHome Initiative** es una plataforma colavorativa de web *full-stack* diseñada para servir de puente entre los protectores de animales y los posibles adoptantes.

El problema principal que aborda PetHome Initiative es tanto la falta de visibilidad como la saturación de los refugios y la desorganización de los procesos de adopción ya que muchas protectoras gestionan adopciones mediante varios canales distintos, nosotros proponemos varias soluciones a este problema, entre ellas:

- Un **catálogo unificado** de todas las mascotas disponibles para adopción, con información detallada y fotos de cada una.
- Un **sistema de gestión de adopciones** que permita a las protectoras organizar y hacer seguimiento de las solicitudes de adopción de manera eficiente.
- Una **campaña de marketing digital** para aumentar el interés y la visibilidad a nuestra plataforma y a las mascotas disponibles para adopción.

## 3. Características principales

A continuación, detallaremos las características principales de la plataforma y su proceso de desarrollo:

- [x] **Catálogo de mascotas**
    - Permite a los usuarios explorar y buscar mascotas disponibles para adopción, con filtros por especie, raza, edad, tamaño y ubicación.
    - Cada mascota tiene su propia página con información detallada, fotos y un formulario de contacto
- [x] **Sistema de pre-adopción digital**
    - Cuestionario de compatibilidad con los posibles adoptantes en los que se determina si la mascota es adecuada para su entorno y estilo de vida.
    - Adjuntación de documentos requiridos para poder completar el proceso de adopción.
- [ ] **Seguimiento de solicitudes de adopción a tiempo real**
    - Panel de control donde los refugios puedan dar de baja o de alta a los animales de forma sencilla implemantada en una base de datos unificada entre los refugios.
    - Notificaciones por correo electrónico a los adoptantes sobre el estado de su solicitud.
- [ ] **Campaña de marketing digital**
    - Contratar a un diseñador gráfico porque lo de nuestro logo es inexcusable. Está hecho en Microsoft Paint, ¿qué clase de compañía profesional hace su logo en Microsoft Paint?
    - Crear contenido visuak atractivo para redes sociales y anuncios en línea.

## 4. Instalación y configuración

Para poner en marcha la plataforma de **PetHome Initiative** y todos los cambios que hemos propuesto, se requiere realizar los siguientes pasos de instalación y configuración:

1. **Despliegue y configuración del entorno cloud**

    - Configurar el servidor principal de la plataforma en el entorno cloud de su elección (AWS, Azure, Google Cloud, etc.).
    - Inicializa las variables de entorno necesarias para la conexión a la base de datos y otros servicios externos.

    ```bash
    cp .env.example .env
    ```
    - Modificar el archivo `.env` con las credenciales y configuraciones específicas de su entorno.

2. **Alta y configuración de las protectoras asociadas**

    - Accede al panel de administración global mediante la ruta `/admin/setup`.
    - Registra las credenciales de los refugios piloto.

3. **Configuración de pasarelas y catálogos iniciales**

    - Conecta las pasarelas de pago externas (Revolut, PayPal, Stripe) para permitir donaciones y pagos de adopción.
    - Carga los catálogos de base de razas, tipos de animales, nombres, fotos, etc., para que los refugios puedan usarlos para registrar nuevas mascotas.
    ```bash
    npm run db:seed
    ```

## 5. Tecnologías utilizadas

A continuación, se detallan las distintas tecnologías utilizadas para la realización de esta iniciativa: 

| Tecnología | Versión | Descripción | Uso en el proyecto |
| :--- | :---: | :--- | :--- |
| **Node.js** | `v20.x` | Entorno de ejecución de JavaScript del lado del servidor, rápido y eficiente. | Motor principal para ejecutar el *backend* y la lógica de negocio de la API. |
| **PostgreSQL** | `v15.2` | Sistema de gestión de bases de datos relacional robusto y altamente escalable. | Almacenamiento seguro de datos de usuarios, refugios y el catálogo de animales. |
| **React** | `v18.2` | Biblioteca de JavaScript para la construcción de interfaces de usuario interactivas. | Desarrollo del panel de control web y la vista del catálogo unificado de adopción. |
| **Docker** | `v24.0` | Plataforma de contenedores de código abierto para automatizar el despliegue. | Estandarización del entorno de desarrollo y despliegue en producción de la iniciativa. |

## 6. Arquitectura y funcionamiento

El funcionamiento de **PetHome Initiative** se basa en un flujo automatizado que conecta de forma eficiente al potencial adoptante con los refujios y las mascotas disponibles en adopción.

El siguiente diagrama de flujo entra en detalle sobre cómo funciona la plataforma:

```mermaid
graph TD
    A[Inicio: Usuario accede al catálogo de mascotas] --> B{¿Usuario encuentra mascota?}
    B -- No --> C[Ajusta filtros de búsqueda]
    B -- Sí --> D[Rellena formulario de pre-adopción]
    D --> E[Envío de documentación y cuestionario de compatibilidad]
    E --> F[Revisión por la protectora de animales]
    F --> G{¿Es compatible?}
    G -- No --> H[Notificación de rechazo al usuario]
    G -- Sí --> I[Notificación de aceptación y visita concertada]
    I --> J[Aprobación final y adopción completada]

## 7. Ejemplos de uso

A continuación, se muestran dos ejemplos prácticos de como interactuar con el sistema de **PetHome Initiative**:

### Ejemplo 1: Consultar el catálogo de mascotas disponibles
Para obtener un listado filtrado de animales listos para la adopción, puedes envíar una petición `GET` al punto de enlace `/api/pets`:

```json
/api/v1/pets?species=dog&status=available
{
  "status": "success",
  "data": [
    {
      "id": "pet-001",
      "name": "Luna",
      "species": "Perro",
      "breed": "Mestizo",
      "age": "2 años",
      "shelter": "Refugio Esperanza",
      "status": "Disponible"
    }
  ]
}
```

### Ejemplo 2: Registrar una solicitud de pre-adopción
Un usuario o una protectora puede enviar una solicitud mediante una petición `POST` con los datos del formulario de pre-adopción:

```json
const response = await fetch('[https://api.pethome.org/v1/adoptions](https://api.pethome.org/v1/adoptions)', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer TU_TOKEN_JWT'
  },
  body: JSON.stringify({
    petId: 'pet-001',
    applicantName: 'María García',
    housingType: 'Piso con terraza',
    hasOtherPets: true
  })
});

const result = await response.json();
console.log('Solicitud creada con éxito:', result);
```