# GIT

Sistema de control de versiones

- Administra versiones de programas
- Open source
- Contribución con desarrolladores
- Guarda registros del código

Permite: 
- **Snaphots:** Fotos del código
- Decidir cambios
- Guardados en cualquier momento

### Estados

**Working Directory** --> Donde trabajo los archivos
<br>
                |<br>
                |<br>
                V<br>
            **git add**<br>
                |<br>
                |<br>
                V<br>
**Staging area** --> Versiones de guardado
                |<br>
                |<br>
                V<br>
            **git commit** <br>
                |<br>
                |<br>
                V<br>
**Repository** --> Versiones finales listas
               
## COMANDOS

```
git init: Proyecto nuevo
git add <file>: working dir -> staging area
git status: estados
git commit: Staging -> repository
git push: repositorio remoto
git pull: sincronizar cambios de otras personas
git clone: duplica, descarga del github url un proyecto
git config --global user.name /user.email
configurar nombre de usuario
git log: ver todos los commits que hemos creado 
git checkout name: revertir los cambios de los archivos y me cambia ese proyecto de rama
git diff: ver diferencias hechas en los archivos
```

## Crear Repo desde la terminal

``` 
    echo "# Mi-Biblioteca-U" >> README.md
    git init
    git add README.md
    git commit -m "first commit" -> mensaje
    git branch -M main
    git remote add origin https://github.com/Valeriacv918/Mi-Biblioteca-U.git
    git push -u origin main
```

## Push an existing repository from the command line
```
git remote add origin https://github.com/Valeriacv918/Mi-Biblioteca-U.git
git branch -M main
git push -u origin main
```

## Comandos de la terminal
```
ls  -> lista de dirctorios
cd  -> change Directory
pwd -> lugar donde estoy
:wq -> salir 
letra i para escribir en el commit

```