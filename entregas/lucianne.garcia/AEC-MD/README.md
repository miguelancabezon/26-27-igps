# BOONTA EVE CLASSIC   <img src="descarga.jpg" width="60" height="60">

*   [1. Presentación del proyecto](#boonta-eve-classic)
*   [2. Objetivo principal](#objetivo-principal)
*   [3. Problema principal](#problema-principal)
*   [4. Caracteristicas Principales](#caracteristicas-principales)

**Bonta Eve Classic** es  un videojuego de carreras de alta velocidad se   
realizara en un entorno bidimencional (2D), inspirado en las intrépidas   
carreras de Tattoine de la pelicula *La amenaza fantasma-Star Wars*,   
la carrera constara de tres vueltas con pods de carreras.   

## **Objetivo principal**  
Objetivo principal del proyecto es desarrollar simulador de alta velocidad,  
un usuario podrá elegir el pods antigravedad,  a través de un cañón  
estrecho que contara con obstáculos y conforme el usuario supere los 
niveles los obstáculos se pondrán mas complejos, desbloquearan nuevos vehículos antigravedad los cuales se podran obtener en la tienda.

## **Problema principal**
En el mercado actual la mayoría de videojuegos que se lanzan son de alta  
resolución y consumen bastantes recursos, haciendo que sean exclusivos  
para ordenadores de alta gama, BOONTA EVE CLASSIC  pretende resolver  
este problema ofreciendo así un titulo eficiente energéticamente.  
Gracias al uso nativo de C# y Godot Engine, el juego permite disfrutar  
de carreras fluidas a alta velocidad sin necesidad de un hardware costoso  
ni un consumo eléctrico elevado.

## **Caracteristicas Principales** 
Funciones principales de  **Bonta Eve CLassic** diseñadas para simulacion  
de carreras:

### **Selleccion de vehiculo**
1. Interfaz interactiva con el usuario para que elija su post antigravedad  
entre los que se tienen disponibles en el catalogo.
### **Sistema de recompesa:**
1. Acumulacionn de **puntos** al finalizar la carrera, dependera de el  
puesto que se obtuvo en la carrera. 
2. Multiplicadores de puntuacion a los tres primeros lugares.
### **Tienda Interactiva de consumo.**
1. Estacio en el cual se podra gastar los puntos. 
2. Se podra adquirir nuevos vehiculos antigravedad bloqueados en 
el catalogo inicial.
3.  Adquisicion de mejora de los propulsores para mejorar la capacidad  
de arranque inicial. 
4.  Mejorar las turbunas para aumentar la velocidad en la carrera.
5.  Obtimizacion de la evasion de obtaculos.
### **Generador dinamico de obtaculos.**
1. Aparicion aleatoria de rocas y trampas en el cañon de Tatooine.
2. Incremnto de dificulatad segun nivel.
### **Sistema de vidas y gestion de daños.**
1. Contador de vidas por partida. El usuario al inicio de cada carrera 
 contara con tres vidas.
2. Destruccion inmediata del vehiculo e inicio en el punto de control  
tras impacto contra el cañon.
### **Gestion para optimizar el codigo**
1. Algoritmo ligero en el bugle del juego en C# para optimizar el consumo 
de CPU.
2. optimizacion en Godot Engine para asegurar un consumo energetico bajo.
### **Estado de desarrollo de las funcionalidades**
- [x] Base de datos para el catalogo de pods.
- [x] Sistema matematico de calculo de puntos segun puesto obtenido.
- [x] Logica de control del vehiculo y aceleracion basica.
- [x] Control de vida (3 a 0) y destruccion en caso de perdida de vidas.
- [ ] Interfaz de la tienda y controles de compra. (En desarrollo)
- [ ] Pantalla visual Game star,  Game over y reinicio de escenario.
- [ ] Optimizacion del los pods.

## **Intalacion y configuracion**
1. Descargue el proyecto clonando el repositorio desde su terminal de Git:
```bash
git clone https://github.com
```
2. Ingrese a la carpeta descargada mediante el comando `cd`:
```bash
cd boonta-eve-classic
```
3. Abra el ejecutable de **Godot Engine**, importe el archivo `project.godot` y pulse la tecla `F5` para iniciar la carrera.

## **Tecnologias utilizadas**

| **TECNOLOGIAS** | **VERSION** | **DESCRIPCION**     | **USO DEL PROYECTO**|
|:-----------------|:-------------|:---------------------|:---------------------|
| Lenguaje C# |`v12.`| Lenguaje orientado a objetos | Programacion de la logica de los pods, calculos de puntuacion y tienda de mejoras|
| Godot Engine| `v4.3`| Motor de videojuegos multiplataforma| Gestion de entorno *2d*, control de la carrera|
|Git /GitHub| `v2.4x`| Sistema de control de versiones y mejoras|Control de codigo fuente e historial de cambios|
|Aseprite|`v1.3`| Especializada en dibuelo de *pixel art* y animacion| Diseño de los cañon, pods antigravedad y los obstaculos|

## **Arquitectura o funcionamientonto**



















