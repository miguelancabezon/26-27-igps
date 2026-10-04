\- AEC-GIT - daniel.celis



\- Introducción

Esta práctica era para aprender a usar Git y la verdad que me he liado bastante al principio. No sabía muy bien la diferencia entre add, commit y push y me salían errores todo el rato.

\- Paso 2

he ejecutado git clone del repo y creé la estructura entregas/daniel.celis/AEC-GIT con mkdir y corregí el error de crear una carpeta en vez de un archivo con mkdir README.txt.


\- Paso 3

Quería crear el README pero lo llamé informe.md para poder meter las capturas mejor en .md
luego cree informe.md (antes me salía como <DIR> por usar mkdir). 
lo solucione con rmdir y type nul > informe.md
luego hice el git add -f por .gitignore, commit "docs: nuevo archivo" y push origin main. Ahí ya me salió en verde new file: informe.md y pude hacer el commit que pedían con el mensaje exacto

Y luego el push:
git push origin main


\- Paso 4
Este paso me costó menos porque ya sabía lo del -f
después hice la rama con git checkout -b docs/modificaciones y git branch para comprobar si estaba en verde. Después creé la carpeta capturas/ dentro de AEC-GIT y fui copiando a mano todos los pantallazos que había hecho desde el Explorador de Windows de Imágenes\Capturas de pantalla a entregas\daniel.celis\AEC-GIT\capturas.

\- Paso 5 - pendiente

Lo haré después del push de esta rama y el merge a main pendiente de hacer.

Para terminar he vuelto a main y he fusionado todo con los siguientes comando:

git checkout main
git merge docs/modificaciones
git push origin main

Conclusión:

Al principio no entendía nada de por qué no me dejaba hacer commit y era porque estaba creando carpetas en vez de archivos y porque la carpeta entregas estaba en el .gitignore(lo tuve que buscar porque no entendía nada de lo que me pasaba). Una vez que entendí lo del git add -f ya fue todo más fácil. He aprendido a usar git status para ver si estoy en verde y a hacer commits con mensajes claros.
