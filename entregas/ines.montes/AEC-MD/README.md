# CAMBIO FÁCIL

**Cambio fácil** es una aplicación que calcula el cambio que se deberá  devolver en una compra.
El usuario **introduce la cantidad a pagar**, y posteriormente **cuanto dinero va a entregar**. La aplicación calcula automáticamente el cambio que debe de ser entregado con los billetes y monedas necesarias. 💵

## Objetivos

El objetivo de este proyecto es _solucionar los problemas_ que pueden surgir a la hora de calcular el cambio mentalmente, además de _optimizar el tiempo_ en tiendas, centros comerciales...💰

El objetivo de **Cambio Fácil** es:
- **Eliminar errores de cálculo** de forma definitiva al devolver el cambio. 
- **Agilizar** el cobro a los clientes.
- Mostrar **qué billetes y monedas deben entregarse**, no solo la cantidad total.

![Foto app](./fto%20doc.jpeg)

## Indice

1. [Presentación de "Cambio Fácil"](#cambio-fácil)
2. [Objetivos del proyecto](#objetivos-del-proyecto)
3. [Índice de contenidos](#índice-de-contenidos)
4. [Características principales](#características-principales)
5. [Instalación y configuración](#instalación-y-configuración)
6. [Tecnologías utilizadas](#tecnologías-utilizadas)
7.[Arquitectura y funcionamiento](#arquitectura-y-funcionamiento)
8.[Ejemplos de uso](#ejemplos-de-uso)
9. [Información adicional](#información-adicional)
    - [Contacto](#contacto)
10. [Elementos visuales y avanzados](#elementos-visuales-y-avanzados)

## Características principales

1. **Entrada de la cantidad de dinero a pagar.**
    - Acepta numeros decimales usando punto o coma.(```12,3``` o ```12.3```)
    - Rechaza valores numéricos negativos, o textos no numéricos.
2. **Entrada para indicar el dinero entregado.**
    - Comprueba que la cantidad ingresada sea suficiente para cubrir el importe a pagar.
    - Avisa de cuanto dinero falta en caso de que no alcance.
3. **Cálculo automático del cambio.**
    - Precisión exacta de céntimos.
    - Sin errores de redondeo.
4. **Desglose del número de billetes y monedas necesarias**
    - Usa el menor numero posible de monedas y billetes.
    - Adaptada al euro (billetes de 5 a 200€ y monedas de 2€ hasta 1 cent).
5. **Modo de realizar varias operaciones seguidas**
    - Permite encadenar varios cobros sin tener que reiniciar el programa.
6. **Historial de operaciones**
    - Guarda un registro de todos los cobros que se han ido haciendo.

**Estado de desarrollo**
- [x] Entrada del importe a pagar.
- [x] Entrada del dinero entregado
- [x] Cálculo del cambio.
- [x] Desglose en billetes y monedas.
- [ ] Modo de varias operaciones seguidas.
- [ ] Historial de operaciones.
- [ ] Exportar el historial a un archivo si es necesario. 


## Instalacion y comunicación

1. Comprueba que tienes instalado **Java 21** con ```java -version```, ```javac -version```.
2. Instala **Visual Studio Code**, y una extensión para poder depurar y ejecutar java. Por ejempplo _"Extension Pack for Java"_ .
3. **Clona el repositorio** usando el comando ```git clone```.

4. Abre la carpeta de Cambio Fácil en VS Code. ```cd (Ruta de carpetas hasta llegar a AEC-MD)```.

5. **Compila el código** desde la terminal con ```javac```.

6. **Ejecuta la aplicación** pulsando sobre el boton ```Run``` que aparece sobre el "main" en VS Code.

Por lo que deberia quedar:
``` bash 
java -version
javac -version

git clone https://github.com/inesmontesiras/26-27-igps.git

cd entregas/ines.montes/AEC-MD

javac -d out src/*.java
```
 


## Tecnologías utilizadas

- 


## Arquitectura y funcionamiento

- 

## Ejemplos de uso

- Usar el programa para que los niños aprendan a manejar los billetes y monedas. 
- Agilizar el pago en las tiendas.
- Método de prevención de estafas
- Ayuda para dar independencia a las personas mayores a la hora de comprar.
- Di

## Información adicional

🚨 Al usar esta app se debe de tener en cuenta que **no es una caja registradora oficial**, ya que no emite nungún ticket, ni sigue ninguna normativa. 🚨

### Contacto 📢
Si tienes algún problema con la app puedes contactarme en:
-  ✉️ **Gmail**: ines@cambiofacil.com
- 🐱 **GitHub**: <https://github.com/inesmontesiras>

## Elementos visuales avanzados
Para el desarrollo de este proyecto he utilizado.
- Emojis compatibles con GitHub de la siguiente web <https://gist.github.com/roachhd/1f029bd4b50b8a524f3c>
 :moneybag 

- Lineas horizontales para mejorar la organización.

----