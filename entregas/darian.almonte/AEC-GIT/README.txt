AEC-GIT - Darian Almonte

INTRODUCCION
En esta actividad practiqué Git. Hice un fork, lo cloné, creé mis carpetas,
hice commits, trabajé en una rama y al final mando una pull request.
Pongo las capturas para demostrar que lo hice yo.

PASO 1: FORK Y CLONADO
Primero hice fork de un repositorio equivocado. Lo repetí con el que dijo
el profe: miguelancabezon/26-27-igps. Me quedó en mi cuenta darian2004.
Luego lo cloné con este comando:
git clone https://github.com/darian2004/26-27-igps.git
Entré a la carpeta con cd 26-27-igps y usé git status. Estaba en main y
sin cambios.

PASO 2: CARPETAS
La carpeta entregas ya existía. Dentro hice mi carpeta con este comando:
mkdir entregas\darian.almonte\AEC-GIT
Usé minúsculas y un punto como pidió el profe.

PASO 3: PRIMER COMMIT
Hice el archivo README.txt con este comando:
type nul > entregas\darian.almonte\AEC-GIT\README.txt
Al principio me dio "Acceso denegado". Me faltó poner el nombre del
archivo al final. Lo corregí y funcionó.
Después usé git add . y git status. El archivo salía en verde.
Hice el commit con el mensaje que pedía el profe:
git commit -m "docs: nuevo archivo"
Lo subí con git push origin main y lo vi en GitHub.

PASO 4: RAMA NUEVA
Hice la rama con este comando:
git checkout -b docs/modificaciones
Copié mis capturas a la carpeta AEC-GIT. Una vez escribí git add. sin
espacio y dio error. Lo repetí bien con git add .
Hice mi primer commit en la rama:
git commit -m "docs: anexo capturas del proceso"
Con git log --oneline vi que el commit aparecía arriba del anterior.
Este texto es mi segundo commit.

CAPTURAS
1.png: el formulario para crear el fork en GitHub
2.png: mi fork ya creado en mi cuenta darian2004
3.png: la URL para clonar mi fork
4.png: git clone, cd y git status
5.png: dir entregas y mkdir de mi carpeta
6.png: el Acceso denegado y la creación del README.txt
7.png: git add, git commit y git push a main
8.png: mi carpeta darian.almonte en GitHub con el commit
9.png: el push a main y la creación de la rama docs/modificaciones
10.png: git add de las capturas y el error de git add. sin espacio
11.png: el commit de las capturas y git log
12.png: este texto en el Bloc de notas
13.png: git status, git add y el commit de este texto
14.png: git log con los dos commits de la rama