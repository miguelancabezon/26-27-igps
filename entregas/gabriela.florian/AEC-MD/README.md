# 1. Presentación del proyecto
¿ Qué es Tres de raya con inteligencia artificial?
Tres en raya con inteligencia artificial es un proyecto que busca desarrollar una versión inteligente del clásico juego de tres en raya
tambén conocido como Tic-Tac Toe)

La propuesta consiste en combinar la visión artificial y la inteligencia artificial para permitir que el sistema reconozca
las fichas colocadas sobre un tablero físico mediante la cámara de un dispositivo móvil.

El objetivo es que el usuario pueda jugar contra un agente inteligente capaz de analizar el estado del tablero y seleccionar sus propias jugadas.
Objetivo Principal

Desarrollar un sistema interactivo que permita:
-Reconocer las fichas del tablero mediante una cámara
-Interpretar la situación actual de la partida.
-Utilizar un algoritmo de inteligencia artificial para decidir la siguiente jugada.
-Facilitar la interacción entre el jugador y el sistema.

El proyecto pretende explorar cómo pueden combinarse la visión artificial y los
algoritmos de decisión para crear un videojuego inteligente.

Imagen representativa
Ilustración representativa del juego Tres en Raya. El recurso gráfico se encuentra en la carpeta assets.

# 2. Índice de contenidos
   1. Presentación del proyecto
   2. Índice de contenidos
   3. Características principales
   4. Instalación y configuración
   5. Tecnologías utilizadas
   6. Arquitectura y funcionamiento
   7. Ejemplos de uso
   8. Información adicional
   9. Contacto

# Características principales
El sistema contempla las siguientes funcionalidades

# Funcionalidades previstas
1. Detección del tablero: utilización de una cámara para identificar la superficie del juego.
Imagen representativa



Ilustración representativa del juego Tres en Raya. El recurso gráfico se encuentra en la carpeta assets.

# 2. Índice de contenidos

Presentación del proyecto

Índice de contenidos

Características principales

Instalación y configuración

Tecnologías utilizadas

Arquitectura y funcionamiento

Ejemplos de uso

Información adicional

Contacto

# 3. Características principales

El sistema contempla las siguientes funcionalidades:

Funcionalidades previstas

Detección del tablero: utilización de una cámara para identificar la superficie de juego.

Reconocimiento de fichas: identificación de las fichas X y O mediante técnicas de visión artificial.

Interpretación del estado del juego: análisis de las posiciones ocupadas y libres del tablero.

Agente de inteligencia artificial: selección de movimientos mediante un algoritmo de decisión.

Detección del resultado: identificación de las condiciones de victoria, derrota o empate.

Interacción con el jugador: comunicación entre el usuario y el sistema durante la partida.

# Estado del desarrollo 
-Selección de la idea
-Identificación de las tecnologías principales
-Desarrollo del reconocimiento del tablero.
-Detección automática de las fichas.
-Implementación del algoritmo de inteligencia artificial.
-Integración de todos los componentes.
-Pruebas y evaluación del funcionamiento.

Paso 1. Acceder a Google Colab
Entrar en la siguiente dirección:https://colab.research.google.com/

Crear un cuaderno nuevo de Python.
Paso 2. Instalar las bibliotecas necesarias
Ejecutar el siguiente comando en una celda de código:

!pip install opencv-python numpy matplotlib

Paso 3. Importar las bibliotecas

import cv2
import numpy as np
import matplotlib.pyplot as plt

print("Entorno preparado correctamente")

Paso 4. Comprobar las versiones

import cv2
import numpy as np

print("Versión de OpenCV:", cv2.__version__)
print("Versión de NumPy:", np.__version__)

Una vez completados estos pasos, el entorno estará preparado para comenzar
a desarrollar y probar los diferentes componentes del proyecto.

# Tecnologías utilizadas
<div align="center">

# Herramientas y tecnologías del proyecto

| Tecnología | Versión | Descripción | Uso en el proyecto |
|:---|:---:|:---|:---|
| **Python** | 3.x | Lenguaje de programación. | Desarrollo de la lógica del juego y algoritmos. |
| **OpenCV** | 4.x | Biblioteca de visión artificial. | Detección y reconocimiento de fichas. |
| **NumPy** | 2.x | Biblioteca de cálculo numérico. | Representación y procesamiento de matrices. |
| **Google Colab** | Actual | Entorno de programación en la nube. | Desarrollo y ejecución de experimentos. |
| **Git / GitHub** | 2.x / Web | Control de versiones. | Organización y documentación del proyecto. |

</div>

# 6. Arquitectura y funcionamiento

Funcionamiento general
Funcionamiento general

El proyecto se organiza en diferentes etapas que permiten transformar la información visual del tablero en una decisión del agente inteligente.

El funcionamiento previsto es el siguiente:

La cámara captura una imagen del tablero.

El módulo de visión artificial procesa la imagen.

El sistema identifica las fichas y sus posiciones.

Se representa el tablero mediante una matriz.

El agente de inteligencia artificial analiza las posibles jugadas.

Se selecciona un movimiento.

Se actualiza el estado de la partida y se comprueba el resultado.

Diagrama de flujo del sistema

flowchart TD
    A([Inicio de la partida]) --> B[Captura de imagen con cámara]
    B --> C[Procesamiento de imagen con OpenCV]
    C --> D[Reconocimiento de fichas]
    D --> E[Representación del tablero en una matriz]
    E --> F[Análisis del estado del juego]
    F --> G[Agente de Inteligencia Artificial]
    G --> H[Selección del siguiente movimiento]
    H --> I[Actualización del tablero]
    I --> J{¿Hay ganador o empate?}
    J -->|No| B
    J -->|Sí| K[Mostrar resultado]
    K --> L([Fin de la partida])


A continuación, se muestran algunas capturas del desarrollo y funcionamiento del proyecto:
# Capturas de pantalla del proyecto

# Primera prueba
![Primera prueba](./Captura%20de%20pantalla%202026-11-07%20135223.png)

# Detección del tablero
![Detección del tablero](./Captura%20de%20pantalla%202026-11-07%20135435.png)

# Reconocimiento de elementos
![Reconocimiento](./Captura%20de%20pantalla%202026-11-07%20143653.png)

# Pruebas del sistema
![Pruebas](./Captura%20de%20pantalla%202026-11-07%20145820.png)

# Resultado
![Resultado](./Captura%20de%20pantalla%202026-11-07%20155014.png)
# Organización por módulos

Módulo

Responsabilidad

Captura de imagen

Obtener imágenes del tablero.

Visión artificial

Detectar y reconocer las fichas.

Representación

Convertir el tablero en una matriz.

Inteligencia artificial

Analizar y seleccionar movimientos.

Gestión de partida

Comprobar victorias, derrotas y empates.

# 7. Ejemplos de uso

Ejemplo 1. Representación del tablero

Markdown utiliza determinados caracteres para aplicar formatos. Por ejemplo, los asteriscos permiten escribir texto en cursiva o negrita.

Para mostrar un asterisco como carácter normal sin aplicar formato, se utiliza una barra invertida:
* Este asterisco se muestra como un carácter normal.

El tablero puede representarse mediante una matriz de tres filas y tres columnas.

import numpy as np

tablero = np.array([
    ["X", "", "O"],
    ["", "X", ""],
    ["O", "", ""]
])

print(tablero)

Resultado esperado:

[['X' '' 'O']
 ['' 'X' '']
 ['O' '' '']]

Esta representación permite conocer las posiciones ocupadas y las casillas disponibles.

Ejemplo 2. Comprobación de una victoria

El siguiente ejemplo permite comprobar si un jugador ha conseguido completar una fila.

def comprobar_fila(tablero, jugador):
    for fila in tablero:
        if all(casilla == jugador for casilla in fila):
            return True

    return False


tablero = [
    ["X", "X", "X"],
    ["O", "", "O"],
    ["", "O", ""]
]

if comprobar_fila(tablero, "X"):
    print("¡El jugador X ha ganado!")
else:
    print("La partida continúa.")

Resultado esperado:
