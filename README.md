Ejercicio 3
===========

[ ] Ahora, envía todo el contenido de tu repositorio local a un repositorio en github.

[ ] A continuación, crea otro repositorio nuevo donde muestres los pasos que realizar para realizar un rebase. Tu nombre de repositorio en github se llamará "Ejercicio3-ejemplo-rebase".

```sh
mkdir programa1
cd programa1
touch datos1
git add datos1
git commit -m "datos1+master"
git checkout -b feature
touch cosanueva1
git add cosanueva1
git commit -m "cosa nueva en feature"
git checkout master
touch a2
git add a2
git commit -m "a2enmaster"
git checkout feature
touch cosanueva2
git add cosanueva2
git commit -m "cosanueva2 en feature"
git checkout master
touch a3
git add a3
git commit -m "a3enmaster"
git rebase master
git log --oneline --all --graph
```

[ ] Añade la carpeta y el fichero que necesitamos tener para indicarle que vamos a hacer uso de Github Actions. Primero crea la carpeta, luego el fichero y luego explica qué comandos van a ejecutarse dentro del fichero yml. 

Añadimos la carpeta .github/workflows donde meteremos nuestro fichero yml. Creamos dentro el fichero acciones.yml. 
Dentro meteremos nuestro codigo como ejemplo este:

```sh
name: GitHub Actions Demo
on: 
  push:
      branches: [ main ]
jobs:
  Explore-GitHub-Actions:
    runs-on: ubuntu-latest
    steps:
      - run: echo "🎉 The job was automatically triggered by a ${{ github.event_name }} event."
```

Que basicamente dice que en el branch main ejecute las acciones en el agente ubuntu-lastest los pasos que salen despues.
