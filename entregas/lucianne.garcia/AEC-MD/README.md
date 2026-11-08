# BOONTA EVE CLASSIC   <img src="descarga.jpg" width="60" height="60">

[![Versión del Juego](https://shields.io)](https://github.com)
[![Estado del Proyecto](https://shields.io)](https://github.com/luciannegarcia-ship-it/26-27-igps)
[![Inspirado en](https://shields.io)](https://starwars.fandom.com/es/wiki/Star_Wars:_Episodio_I_La_Amenaza_Fantasma)
---

*   [1. Presentación del proyecto](#boonta-eve-classic)
*   [2. Objetivo principal](#objetivo-principal)
*   [3. Problema principal](#problema-principal)
*   [4. Caracteristicas Principales](#caracteristicas-principales)
*   [5. Instalacion y configuracion](#instalacion-y-configuracion)
*   [6. Tecnologías utilizadas](#tecnologías-utilizadas)
*   [7. Arquitectura o funcionamiento](#arquitectura-o-funcionamiento)
*   [8. Ejemplos prácticos](#ejemplos-practicos)
*   [9. Información adicional](#elementos-importantes)
*   [10. Contactos](#contactos)
*   [11. Contenido](#contenido)
---
<a name="boonta-eve-classic"></a>
<img src="BOONTA.jpg" align="right" width="600" style="margin-left: 15px; border-radius: 8px;">

**Bonta Eve Classic**  es  un videojuego de carreras de alta velocidad se realizara en un entorno bidimensional  
(2D), inspirado en las intrépidas carreras de Tatooine de la pelicula *La amenaza fantasma-Star Wars*,la carrera  
constara de tres vueltas con pods de carreras. 

<a name="obj-principal"></a>


## Objetivo principal
Objetivo principal del proyecto es desarrollar simulador de alta velocidad, un usuario podrá elegir el pods antigravedad, 
a través de un cañón estrecho que contara con obstáculos y conforme el usuario supere los niveles los obstáculos se pondrán  
mas complejos, desbloquearan nuevos vehículos antigravedad los cuales se podran obtener en la tienda.

## Problema principal
En el mercado actual la mayoría de videojuegos que se lanzan son de alta resolución y consumen bastantes recursos, 
haciendo que sean exclusivos para ordenadores de alta gama, BOONTA EVE CLASSIC  pretende resolver este problema  
ofreciendo así un titulo eficiente energéticamente.  
Gracias al uso nativo de C# y Godot Engine, el juego permite disfrutar de carreras fluidas a alta velocidad sin 
necesidad de un hardware costoso ni un consumo eléctrico elevado.



## Caracteristicas Principales
Funciones principales de  **Bonta Eve CLassic** diseñadas para simulacion de carreras:

<a name="boonta-eve-classic"></a>
<img src="tatooine.jpg" align="right" width="700" style="margin-left: 15px; border-radius: 8px;">

### Selleccion de vehiculo
1. Interfaz interactiva con el usuario para que elija su post antigravedad  
entre los que se tienen disponibles en el catalogo.
### Sistema de recompensa:
1. Acumulacion de **puntos** al finalizar la carrera, dependera de el  
puesto que se obtuvo en la carrera. 
2. Multiplicadores de puntuacion a los tres primeros lugares.
### Tienda Interactiva de consumo.
1. Espacio en el cual se podra gastar los puntos. 
2. Se podra adquirir nuevos vehiculos antigravedad bloqueados en 
el catalogo inicial.
3.  Adquisicion de mejora de los propulsores para mejorar la capacidad  
de arranque inicial. 
4.  Mejorar las turbinas para aumentar la velocidad en la carrera.
5.  Optimizacion de la evasion de obstaculos.
### Generador dinamico de obtaculos.
1. Aparicion aleatoria de rocas y trampas en el cañon de Tatooine.
2. Incremento de dificultad segun nivel.
### Sistema de vidas y gestion de daños.
1. Contador de vidas por partida. El usuario al inicio de cada carrera 
contara con tres vidas.
2. Destruccion inmediata del vehiculo e inicio en el punto de control  
tras impacto contra el cañon.
### Gestion para optimizar el codigo
1. Algoritmo ligero en el bucle del juego en C# para optimizar el consumo 
de CPU.
2. optimizacion en Godot Engine para asegurar un consumo energetico bajo.
### Estado de desarrollo de las funcionalidades
- [x] Base de datos para el catalogo de pods.
- [x] Sistema matematico de calculo de puntos segun puesto obtenido.
- [x] Logica de control del vehiculo y aceleracion basica.
- [x] Control de vida (3 a 0) y destruccion en caso de perdida de vidas.
- [ ] Interfaz de la tienda y controles de compra. (En desarrollo)
- [ ] Pantalla visual Game star,  Game over y reinicio de escenario.
- [ ] Optimizacion del los pods.

<a name="caracteristicas"></a>

## Instalacion y configuracion

### Pasos necesarios para instalar
1. Descargue el proyecto clonando el repositorio desde su terminal de Git:
```bash
git clone https://github.com
```
2. Ingrese a la carpeta descargada mediante el comando `cd`:
```bash
cd boonta-eve-classic
```
3. Abra el ejecutable de **Godot Engine**, importe el archivo `project.godot` y pulse la tecla `F5` para iniciar la carrera.
### bloque de codigo

#### Calculo de puntos
Asignacion de puntos segun puesto obtenido en la carrera.
```csharp
public int CalcularPuntos(int posicion) 
{
    if (posicion == 1) return 500; // Primer puesto
    if (posicion == 2) return 300; // Segundo puesto
    if (posicion == 3) return 150; // Tercer puesto
    return 50;                     // Otros puestos
}
```
### Elementos importantes
> ⚠️ \*ATENCION\*No altere la variable `puntos`.Podria dañar el sistema
<details>
<summary><b>Optimización</b></summary>

El juego usa el comando `LimpiarRAM()` para ahorrar energía en el PC.
</details>

<!-- Sistema de optimizacion -->

## Tecnologias utilizadas

| **TECNOLOGIAS** | **VERSION** | **DESCRIPCION**     | **USO DEL PROYECTO**|
|:-----------------|:-------------|:---------------------|:---------------------|
| Lenguaje C# |`v12.`| Lenguaje orientado a objetos | Programacion de la logica de los pods, calculos de puntuacion y tienda de mejoras|
| Godot Engine| `v4.3`| Motor de videojuegos multiplataforma| Gestion de entorno *2d*, control de la carrera|
|Git /GitHub| `v2.4x`| Sistema de control de versiones y mejoras|Control de codigo fuente e historial de cambios|
|Aseprite|`v1.3`| Especializada en dibujo de *pixel art* y animacion| Diseño de los cañon, pods antigravedad y los obstaculos|

## Arquitectura o funcionamiento
Boonta Eve Classic funciona de forma continua el cual se logra por Godot Engine. El sistema se encarga de leer contantemente los comandos del  
teclado del usuario, se calcula los movimientos del pod con C#, comprueba si existe colisiones con las rocas del cañon antes de que 
se dibuje el siguiente fotograma en pantalla.
---

```mermaid 
graph TD;
A[Inicio de la carrera]-->B[Inicializador Pod tres vidas]
B-->C[Bucle principal del juego]
C-->D[Leer comandos de teclado, aceleracion, evasion]
D-->E[Calculos de los movimientos]
E-->F{¿Choco el Pod?}
F--> Si -->G[ Resta 1 vida]
F--> No -->H[Continuea Bucle]
G --> I{¿Vidas == 0?}
I -- Sí --> J[Pantalla de Game Over]
I -- No --> H
H --> K{¿Completó las 3 vueltas?}
K -- Sí --> L[Calcular puntos obtenidos según puesto]
K -- No --> C
L --> M[Guardar puntos en la Tienda]
M --> N[Fin de la Carrera]
```
---

## Ejemplos Practicos
### Calcular puntos de la carrera
```csharp
public int CalcularPuntos(int posicion) 
{
    // Si queda primero, suma quinientos puntos
    if (posicion == 1) return 500; 
    // ...
}
```
### Mejora de velocidad 
```csharp
public int MejorarVelocidad(int velocidadBase, int puntosMejora)
{
    return velocidadBase + puntosMejora;
}
```
Para mas detalles sobre la optimizacion del motor y la programacion del juego,  [Documentación de Godot C#](https://godotengine.org).

## Contactos
Si experimenta alguna complicacion en el juego, o tiene dudas sobre la optimizacion del codigo, se puede contactar mediante:
[Github](https://github.com/luciannegarcia-ship-it),
[Gmail](lucianne.garcia@alumnos.uneatlantico.es)

## Contenido
[![Mapa de ¿l circuito oficial de Tatooine](https://shields.io)](https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/a7e43642-8f48-424a-a8ff-cc7791a0cb22/dj2cgmw-97d6e1d2-cccc-4cca-8f7d-f9c8ca0bae0a.jpg/v1/fill/w_1084,h_737,q_70,strp/boonta_eve_classic_race_track_by_minzamondblume_dj2cgmw-pre.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9ODcwIiwicGF0aCI6Ii9mL2E3ZTQzNjQyLThmNDgtNDI0YS1hOGZmLWNjNzc5MWEwY2IyMi9kajJjZ213LTk3ZDZlMWQyLWNjY2MtNGNjYS04ZjdkLWY5YzhjYTBiYWUwYS5qcGciLCJ3aWR0aCI6Ijw9MTI4MCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.145Of0uC2iYKi61SRjjTDaseRoHPk969kbcG_ESwuVk)

[Informacion extendida historia de la carrera Boonta Eve Classic](https://starwars.fandom.com/wiki/Boonta_Eve_Classic)





















