ENTREGA AEC-GIT - Jaime Apellido

1. FORK DEL REPOSITORIO
Hice fork del repositorio desde GitHub para tener una copia propia en mi cuenta.

[Captura: capturas/01-fork.png]


2. CLONADO EN LOCAL
-------------------------------------------
Cloné mi fork con:
    git clone https://github.com/TU_USUARIO/NOMBRE_REPO.git

[Captura: capturas/02-clone.png]


3. ESTRUCTURA DE CARPETAS
-------------------------------------------
Creé entregas/jaime.apellido/AEC-GIT con:
    mkdir -p entregas/jaime.apellido/AEC-GIT

[Captura: capturas/03-carpetas.png]


4. PRIMER COMMIT
-------------------------------------------
Creé informe.txt vacío, lo añadí y subí:
    git add .
    git commit -m "docs: nuevo archivo"
    git push origin main

[Captura: capturas/04-primer-commit.png]


5. RAMA DOCS/MODIFICACIONES
-------------------------------------------
Creé la rama de trabajo:
    git checkout -b docs/modificaciones

Fui añadiendo capturas y texto en varios commits
y subí la rama:
    git push origin docs/modificaciones

[Captura: capturas/05-rama.png]
[Captura: capturas/06-commits.png]


6. MERGE
-------------------------------------------
    git checkout main
    git merge docs/modificaciones
    git push origin main

[Captura: capturas/07-merge.png]


7. PULL REQUEST
-------------------------------------------
Creé la PR desde docs/modificaciones de mi fork
hacia main del repositorio original.

[Captura: capturas/08-pr.png]


CONCLUSIÓN
-------------------------------------------
(2-3 líneas sobre lo aprendido)