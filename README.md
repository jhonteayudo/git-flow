# Uso del gitflow 🚀

Ramas master y develop
El trabajo se organiza en dos ramas principales:

- Rama master: 
cualquier commit que pongamos en esta rama debe estar preparado para subir a producción
- Rama develop: 
rama en la que está el código que conformará la siguiente versión planificada del proyecto
Cada vez que se incorpora código a master, tenemos una nueva versión.

### Además de estas dos ramas, Se proponen las siguientes ramas auxiliares:

- Feature
- Release
- Bugfix
- Hotfix

Cada tipo de rama, tiene sus propias reglas, que resumimos a continuación. Cada rama tiene su respectivo label para ser asociado. Los issues tienen y las ramas asociadas tienen la siguiente prioridad:

1. Hotfix: Deben ser atentidas inmediatamente.
2. Bugfix: Una vez cerrado un issue, los bugfix son los siguientes a tratar. Si el bugfix tiene relacion con alguna rama feature en proceso tiene que cerrarse primero el bug.
3. Feature: Son atendidos en caso de no haber bugfix abiertos
4. Release: Como son lo branch para preparar para produccion no tienen una prioridad definida.

### Rama Feature
- Se originan a partir de la rama develop.
- Se incorporan siempre a la rama develop.
- Nombre: feature-*
Estas ramas se utilizan para desarrollar nuevas características de la aplicación que, una vez terminadas, se incorporan a la rama develop.

### Rama Release
- Se originan a partir de la rama develop
- Se incorporan a master y develop
- Nombre: release-*
Estas ramas se utilizan para preparar el siguiente código en producción. En estas ramas se hacen los últimos ajustes y se corrigen los últimos bugs antes de pasar el código a producción incorporándolo a la rama master.

### Rama Bugfix
- Se originan a partir de la rama develop.
- Se incorporan siempre a la rama develop.
- Nombre: bugfix-*
Estas ramas se utilizan para corregir errores y bugs en el código en desarrollo (develop).

### Rama Hotfix
- Se origina a partir de la rama master
- Se incorporan a la master y develop
- Nombre: hotfix-*
Estas ramas se utilizan para corregir errores y bugs en el código en producción (master). Funcionan de forma parecida a las Releases Branches, siendo la principal diferencia que los hotfixes no se planifican.

## Uso de los comandos
#### Crear una nueva feature (en el ejemplo my-feature):
```
$ git flow feature start my-feature
```
#### Finalizar la rama feature:
```
$ git flow feature finish my-feature
```
#### Publicar la rama feature en el repositorio remoto:
```
$ git flow feature publish my-feature
```
#### Obtener una rama feature del repositorio remoto:
```
$ git flow feature pull origin my-feature
```
#### Seguir de los cambios de la feature:
```
$ git flow feature track my-feature
```

