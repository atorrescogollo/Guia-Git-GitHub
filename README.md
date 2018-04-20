# Guía Git GitHub
Guía básica de uso de Git y GitHub

# Git
```    
git init            # Inicialización de un espacio de trabajo
```
## Trabajo con commits
```
git add <archivo>   # Añadir un archivo (al commit temporal)
git add -A          # Añadir todo
git status          # Estado actual del commit temporal
```
```
git commit          # Crear commit
    -m <nombre>       # Nombre del commit
    --branch          # Rama en la que se alojará el commit
    --amend           # Modificar el commit anterior
```
```
git log             # Ver todos los commits
```
```
git checkout <sha>  # Desplazarse a un commit (a partir del codigo SHA)
git checkout master # Desplazarse a la última versión
```
```
git reset HEAD~<posicion> # Borrar un commit
    --soft          # Solo borra el commit
    --hard          # Borra también el código añadido después del commit
```
## Trabajo con ramas
```
git branch              # Muestra todas las ramas
```
```
git branch <rama>       # Crea una rama
    -b                  # Con desplazamiento hacia la rama
```
```
git branch -D <rama>    # Borra una rama
```
```
git checkout <rama>     # Desplazarse a una rama
```
```
git merge <rama>        # Absorbe una rama (la almacena donde nos encontramos)
    --commit -m <nombre>    # Añade un commit con el resultado
    --no-commit             # No se crea ningún commit
```

# GitHub
```
git clone <url>               # Descargar un proyecto
```
```
git remote add origin <url>   # Crea relación local-remoto
git remote remove origin      # Quita relación local-remoto
```
```
git push origin <rama>        # Actualiza la rama en el repositorio
    --all                         # Todas las ramas
    -u                            # Tracking del proceso de subida
```

## Workflows
Pepe y Juan trabajan en el mismo proyecto:
```
# Pepe actualiza el repositorio con sus cambios
pepe@pc:~/proyecto$ git push origin master          # Pepe sube los cambios
```
```
# Juan quiere modificar su proyecto local. Primero, tiene que actualizar
juan@pc:~/proyecto$ git fetch origin                # Descarga de origin (GitHub)
juan@pc:~/proyecto$ git merge origin/master         # Absorción de la rama master de origin (Posibles conflictos!!)
```

### Forks
```
git fetch upstream            # Descargar última versión
git push origin master        # Sube los cambios (a nuestra cuenta)
```
En Github, **"new pull request"** > **"create"**
