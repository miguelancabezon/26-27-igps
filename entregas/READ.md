![Estado](https://img.shields.io/badge/Estado-En_Desarrollo-orange?style=flat-square)
![Versión](https://img.shields.io/badge/Versi%C3%B3n-1.0.0-blue?style=flat-square)

<!-- Hola profesor. Este es el comentario oculto que pidió en la rúbrica. No será visible en la renderización del Markdoown, pero demuestra el dominio de las etiquetas HTML. -->

# AniMatch API

**AniMatch API** Es un motor de recomendaciones de codigo abierto impulsado por metadatos. A diferencia de las plataformas tradicionales, no aloja contenido, sino que sirve como una base de datos relacional para descubrir animes.

**Objetivo principal y problema a resolver:**

El problema actual es que los motores de busqueda recomiendan series basándose únicamente en géneros genéricos (como *shonen* o *comedia*). El objetico de AniMatch es resolver esto permitiendo a los usuarios series basandose en la similitud visual, rastreando a los ilustradores, directores de arte y **estudios de animacion** específicos detrás de sus obras favoritas.

![AniMatch Header](https://images.unsplash.com/photo-1578632767115-351597cf2477?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80 "Imagen representativa de animación japonesa")

---

## 2. Índice de contenidos

- [1. Presentación del proyecto](#-animatch-api)
- [3. Características principales](#3-características-principales)
- [4. Instalación y configuración](#4-instalación-y-configuración)
- [5. Tecnologías utilizadas](#5-tecnologías-utilizadas)
- [6. Arquitectura y funcionamiento](#6-arquitectura-y-funcionamiento)
- [7. Ejemplos de uso](#7-ejemplos-de-uso)
- [8. Información adicional](#8-información-adicional)

---

## 3. Características principales

El sistema expone varias rutas de acceso para filtrarr la información con las siguientes funciones:
1. **Motor de Similitud Visual:** Algoritmo que agrupa series según el director de arte.
2. **Filtro de Continuidad de Estudio:**
    -Seguimiento de franquicias que cambian de el estudio de animación.
    -*Ejemplo:* La diferencia de animación del anime *shonen*: *AOT(Attack on Titan)*, creado por *[Hajime Isayama](https://shingeki-no-kyojin.fandom.com/es/wiki/Hajime_Isayama)*. Sus primera 3 temporadas fueron producidas por *[Wit Studio](https://shingeki-no-kyojin.fandom.com/es/wiki/Wit_Studio)* siendo caracterizado por su uso intensivo de líneas gruesas hechas a mano y también su secuencias de acción en *2D*. En cuanto su cierre, el proyecto se pasó a manos de *[MAPPA](https://shingeki-no-kyojin.fandom.com/es/wiki/MAPPA)*, que implementó un esilo *hiperrealista* y maduro del manga, introduciendo un uso constante de titanes modelados en *CGI(Computer-Generated Imgaery)* o *(3D)*.
3. **Emparejamiento de Autores(Author Matchmaking):** Mapeo de ilustradores para recomendar colaboraciones similares.
4. **Respuestas en formato JSON:** Estructura ligera y estanderizada para cualquier cliente *frontend*.
5. **Sistema de Caché:** Almacenamiento temporal para acelerar las peticiones más frecuentes.

**Estado actual de las funcionalidades:**
- [ ] Diseño de la base de datos relacional.
- [ ] Creación de endpoints para búsqueda por estudio.
- [ ] Implementación de la lógica de Inteligencia Artificial.
- [ ] Despliegue en servidor en la nube.

---

## 4. Instalación y configuración

Para levantar el entorno de desarrollo local y consumir la API, sigue este procedimiento:

1. Abre tu terminal (por ejemplo, Git Bash) y clona el repositorio:
2. Navega al directorio del proyecto 
3. Copia el archivo `.env.example` y renombralo a `.env` para confirgurar tus variables locales. 
4. Ejecuta el entorno utilizando Java: 

```bash
#Clonar y entrar al proyecto
git clone [htpps://github.com//angelmaldonado-neitzen/AniMatch-API.git](https://github.com/angelmaldonado-neitzen/AniMatch-API.git)
cd AniMatch-API

# Compilar y ejecutar la clase principal
javac src/ApiSever.java 
java src/ApiServer

## 5. Tecnologías utilizadas
| Tecnología | Versión | Descripción | Uso en el Proyecto |
| :--- | :---: | :--- | ---: |
| **Java** | `JDK 17` | Lenguaje de programación | Desarrollo del motor de búsqueda y lógica. |
| **Git** | `2.42` | Control de versiones | Gestión de ramas y *Pull Requests*. |
| **PostgreSQL** | `15.4` | Base de datos relacional | Almacenamiento de metadatos de estudios. |
| **Markdown** | `N/A | Lenguaje de marcado | Creación de la documentación técnica. |

:sparkles:## 6.  Arquitectura y funcionamiento

El propósito de *AniMatch API" es que, cuando termines de ver una *obra maestra* como *Attack on Titan* y te quedes con la boca abierta por su animación y historia; para que sigas con ese sentimiento de asombro. *AniMatch* te permite descubrir diferentes obras creado por el mismo autor, estudio de animación o por artistas con un estilo similar. Porque a veces, cuando terminamos de ver un anime excepcional, no solo buscas otra serie, sino una experiencia que sea igual o mejor a la que ya hayas pasado.


flowchart LR
    client["Frontend Client<br/>External component"]

    subgraph backend ["AniMatch API — Proposed Backend Architecture"]
        subgraph java ["Java API Server — Implementation unverified"]
            rest["REST API Endpoints — Planned<br/>Search by studio / Visual similarity<br/>HTTP requests and JSON responses"]

            subgraph engine ["Recommendation Engine — Planned"]
                dispatch["Request Processing<br/>Select requested workflow"]
                studio["Search by Studio<br/>Retrieve anime associated with a studio"]
                visual["Visual Similarity Algorithm<br/>Compare studio, art director<br/>and visual metadata"]
                continuity["Studio Continuity Filter<br/>Track studio changes across a franchise"]
                author["Author Matchmaking<br/>Find related illustrators and collaborations"]
            end
        end

        db["PostgreSQL Database — Planned<br/>Anime, studio and creator metadata<br/>Relational schema pending"]
        cache["Caching System — Planned<br/>Temporary storage of frequent results<br/>Technology unspecified"]
    end

    client -->|HTTP request with studio or favorite anime| rest
    rest -->|Dispatch request| dispatch
    dispatch -->|Studio selection| studio
    dispatch -->|Favorite anime selection| visual
    dispatch -.->|Planned additional capability| continuity
    dispatch -.->|Planned additional capability| author
    dispatch -->|Look up cached results| cache
    cache -->|Cached result or miss| dispatch
    studio -->|Query by studio| db
    db -->|Matching anime| studio
    visual -->|Query reference and candidate metadata| db
    db -->|Studio, art director and visual metadata| visual
    continuity -.->|Read franchise and studio metadata| db
    author -.->|Read illustrator and collaboration metadata| db
    studio -->|Search results| dispatch
    visual -->|Similar anime| dispatch
    dispatch -->|Store computed results| cache
    dispatch -->|Results| rest
    rest -->|JSON response| client

:sparkles:## 7. Ejemplos de uso:

A continuación, se mostraran ejemplos prácticos de cómo el *Frontend Client* interactúa con los *Rest API Endpoints* descritos en la arquitectura del sistema.

**Ejemplo 1: Petición al endpoint de Similitud Visual **(Frontend Client)**
En este caso, el cliente solicitará animes con similitud visual usando como referencia *Attack on Titan*, lo que dispara el flujo del `Visual Similarity Algorithm`:
```java
HttpClient client = HttpClient.newHttpClient();
HttpRequest request = HttpRequest.new Builder()
      .uri(URI. create("http://localhost:8080/api/v1/recommend/visual?reference=attackontitan"))
      .header("Accept", "application/json")
      .build();

      HttpResponse<String> response = client.send(request, BodyHandlers.ofString());
      System.out.println(response.body());
          
**Ejemplo 2: Respuesta JSON del Motor(Recommendation Engine)
{
    "status": 200,
    "reference": "Attack on Titan",
    "data": [
       {
        "anime_id": 40748,
        "title": "Jujutsu Kaisen",
        "studio": "MAPPA",
        "similarity_score": 0.96,
        "shared_attributes": ["Action", "Dark Fantasy", "CGI Integration"]
       },
       {
         "anime _id": 37521,
         "title": "Vinland Saga",
         "studio": "Wit Studio",
         "similarity_score": ["Action", "Gore", "2D Line Art"]
       }
    ]
}

 :sparkles:## 8. Información adicional

> **Advertencia sobre el límete de peticiones (Rare Limit):** Para evitar la sobrecarga del servidor en la versión de desarrollo, te recomendamos hacer un máximo de 60 peticiones por minuto. Si se supera este límete, la API delvolverá un error `429 Too Many Requests`.
<details>
<summary> <strong>Haz clic aquí para ver la Política de Contribución</strong></summary>
<p>¡Cualquier ayuda es bievenida! Si deseas agregar nuevos metadatos de estudios de animación (como MAPPA O Wit Studio) a nuestra base de datos, por favor haz un <em>fork</em> del repositorio, crea una rama (<code>branch</code>) con tu propuesta y envía un <em>Pull Request</em>. Recuerda verificar tu código antes de envviarlo.</p>
</details>

<br>

:sparkles: **Nota sobre sintaxis de Markdown:**
En Markdown utilizamos astericos para las cursivas y negritas. Si necesitasescribir un asterisco real en tu documentación sin tener que cambiar el texto, debes "escaparlo" usando una barra invertida. Por ejemplo: \*AniMatch API\* (el texto no se pondrá en cursiva).

:sparkles: <!-- Profesor: Aquí meto el comentario HTML oculto adiciona, como lo puso en la rúbrica sobre elementos invisibles en la renderización. -->

:sparkles: **Contacto y Soporte**
- Correo: angel.maldonado@alumnos.uneatlantico.es
- Perfil de Github: [angelmaldonado-neitzen](https://github.com/angelmaldonado-netizen/26-27-igps) 

:sparkles: **Apps o IAs utilizadas:**
-Gemini
-Mermaid
-Shield.io