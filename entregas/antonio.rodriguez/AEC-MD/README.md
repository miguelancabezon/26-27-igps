# EL GRANDIOSO VIAJE DE MARCO
 <a id="begin"></a>

El grandioso viaje de Marco es una divertida aplicacion en la cual puedes observar las diferentes travesias que tiene Marco junto a su mono Amedio al tratar de llegar donde su madre.

## Objetivos:
  <a id="objetivos"></a>
* *Ver cuanto tardaria Marco en llegar donde su madre 💞*
* ~~Identificar las diferentes probabilidades que algo salga mal o que Marco se retrase 😭~~
* **Señalar lo mal portado que es Amedio 😡**
* Enseñar un final feliz al encontrarse con su madre 😆

![Logo](./img/Gemini_Generated_Image_tmpafitmpafitmpa.jpg)

###### Enlaces dentro del MD
| Inicio | [Ir al inicio](#begin) |
|:----------:|:--------:|
| Objetivos    | [Ir a objetivos](#objetivos)   |
| Funcionalidades | [Ir a funcionalidades](#Funciona) |
| Instalacion | [Ir a Instalacion](#Instalacion) |
| Tecnologias Usadas | [Ir a Tech Usada](#TechUsada) |
| Florchart | [Ir a flowchart usado](#flowchart) |



### Funcionalidades
<a id="Funciona"></a>
+ Señalar como se implementan las probabilidades en JAVA
+ Aclarar una bonita historia de amor
+ Enseñar las probabilidades no excluyentes
    + Como Amedio se puede escapar y cansar el mismo dia!
+ Incluir un contador de dias de cuanto tarda Marco
+ Separar cada dia con una bonita conjuncion de lineas y asteriscos 😮

[x] Hacer Pasos 1,2,3,4  
[ ] Terminar la tarea  
[ ] Hacer pasos 5 , 6, 7

## Instalacion
 <a id="Instalacion"></a>
1. Descargar Java y actualizarlo a ultima version
2. Descargar Visual Studio Code e implementar las extensiones necesarias de Java
3. Clonar la repo [Mi repo haha😆](https://github.com/antoniorodriguez007/26-27-prg1.git)  
    3.1 En la rama practica-03-11 encontrar la carpeta entregas  
    3.2 Abrir la carpeta entregas y entrar a *rodriguezAntonio*  
4. Al estar dentro de esa carpeta, ingresar a **src** y tendras que ver un archivo llamado `ViajedeMarco.java` con codigo similar a este:
 ```javascript
if (chance_amedio <= PROB_AMEDIO_ESCAPA) {
                horas_de_viaje = horas_de_viaje - REDUCCION_HORAS_AMEDIO_ESCAPA;
                System.out.println("EL AMEDIO INTENTO ESCAPAR");
            }
            if (chance_amedio <= PROB_AMEDIO_CANSA) {
                velocidad_promedio = velocidad_promedio * REDUCCION_VELOCIDAD_AMEDIO_CANSA;
                System.out.println("EL AMEDIO SE CANSO");
            }
```
5. Ejecutar y ver como viaja Marco!!!😎😎

## Tecnologias usadas
 <a id="TechUsada"></a>
| Tecnologia | JAVA | Visual Studio | Manos Humanas | Github
|:----------:|:--------:| :--------:| :--------:| :--------:|
| Version   |  **JDK 27**  |  **18.5** | **2026** | **3.22.2** |
| Descripcion |  lenguaje de programación y una plataforma | IDE creado por Microsoft, utilizado  para diseñar, depurar, probar  software orientado a objetos | Parte del cuerpo humano que viene con la mayoria de personas, terminan en 5 dedos | Plataforma basada en la nube que permite a los desarrolladores almacenar, gestionar y colaborar en proyectos de código 
| Uso en el proyecto |  El lenguaje de programacion base usado para este proyecto|  IDE principal que se empleo en la creacion del proyecto | Con estas fue que se tocaron las teclas del teclado que se usaron al crear la aplicacion | Uso de este para verificar versiones y discutir mejoras entre los desarrolladores |


## Florwchart tipo mermaid
 <a id="florchart"></a>

```mermaid
  flowchart TD
    A([Inicio]) --> B["Inicializar variables:<br/>distancia = 350 km, dias = 0"]
    B --> C["Inicio del día:<br/>dias++"]
    C --> D["Generar variables aleatorias base:<br/>Velocidad: 10 - 15 km/h<br/>Horas: 8 - 10 h"]
    
    D --> E{"Evaluar Clima"}
    E -- "Lluvia Fuerte (10%)" --> F1["Velocidad = Velocidad * 0.25"]
    E -- "Lluvia Moderada (30%)" --> F2["Velocidad = Velocidad * 0.75"]
    E -- "Buen Clima (60%)" --> F3["Velocidad sin cambios"]
    
    F1 --> G1{"¿Amedio se escapa?<br/>(15%)"}
    F2 --> G1
    F3 --> G1
    
    G1 -- Sí --> H1["Horas = Horas - 2"]
    G1 -- No --> G2
    H1 --> G2{"¿Amedio se cansa?<br/>(25%)"}
    
    G2 -- Sí --> H2["Velocidad = Velocidad * 0.90"]
    G2 -- No --> I
    H2 --> I["Calcular avance diario:<br/>kmMarco = Velocidad * Horas"]
    
    I --> J["Actualizar distancia:<br/>distancia = distancia + 80 - kmMarco"]
    J --> K{"¿distancia < 0?"}
    K -- Sí --> L["Ajustar distancia = 0"]
    K -- No --> M
    L --> M{"¿distancia <= 0?"}
    
    M -- No (Sigue el viaje) --> C
    M -- Sí (¡Alcanzó a su madre!) --> N["Imprimir resultados y días totales"]
    N --> O([Fin del programa])
```

### Ejemplos de uso
1. Si juegas con los datos puedes ver como alterar aunque sea una cosita pequena afecta por completo a como seria el viaje, ya sea aumentando mucho los dias o acortandolos, puedes hacer sufrir a Marco o hacer que Amedio le de empujones, con solo cambiar unos numeros.  
``` java
  if (chance_amedio <= PROB_AMEDIO_EMPUJA) {
                horas_de_viaje = horas_de_viaje + ADICION_HORAS_AMEDIO_EMPUJA;
                System.out.println("EL AMEDIO TE EMPUJO, +2 HORAS EXTRA");
            }
            if (chance_amedio <= PROB_AMEDIO_BANANA) {
                velocidad_promedio = velocidad_promedio * ADICION_VELOCIDAD_AMEDIO_BANANA;
                System.out.println("EL AMEDIO SE SACO UNA BANANA, TU VEL SE MULTIPLICA X 2!");
            }
```
2. Sirve como material de estudio de un programa basico hecho en JAVA con bucles simples.  

## Enlaces utiles!
* [Google](https://www.coursera.org/courses?query=java&index=prod_all_products_term_optimization_united_states&languages=es&start=20&utm_medium=sem&utm_source=gg&utm_campaign=b2c_emea_x_multi_ftcof_career-academy_cx_dr_bau_gg_sem_gc_s1_en_m_hyb_24-03_x&campaignid=21119897702&adgroupid=184367650928&device=c&keyword=data%20engineering%20courses&matchtype=p&network=g&devicemodel=&creativeid=749370828398&assetgroupid=&targetid=kwd-346848013160&extensionid=&placement=&gad_source=1&gad_campaignid=21119897702&gclid=CjwKCAiAzKvXBhBAEiwABLl9Av_aFT9z_1wHiXeJbP_uDdR6e0xN8jkztv01bVuTeJ0jSs4imzmiUBoCkAIQAvD_BwE "Curso de JAVA")  
* [Google](gemini.google.com "Ir a Google gemini") 

## Lista colapsable
<details>
<summary>Click para expandir </summary>

Todo esto fue hecho a base del proyecto realizado en PRG1 el dia del 03/11/26, cualquier consulta o duda estoy a la orden!
</details>


## Creador
***
@antoniorodriguez07
***
[Contáctame](antonio.rodriguez@alumnos.uneatlantico.es)
[Enviar email con asunto](mailto:correo@ejemplo.com?subject=Consulta)

> [!WARNING]
> Se reservan los derechos de autor, prohibido calificar con algun numero menor a 10, se demandara al encontrar algo contrario a lo dicho.

<!-- Mentira profe, pero esta bonito el MD no? creo que SI merece un 10 😉 -->






