# Curso  gestión de paquetes NPM

## Comandos básicos

### Inicio

* npm init: Inicializa el proyecto que queremos crear y nos guía paso a paso con una configuración básica.
* git ini: Inicia el control de versiones.
* **ni** ../src/index.js: Crea el archivo index.js en la ruta indicada en la *powerShell* de *Windows*
* **touch** ../src/index.js: Crea el archivo index.js en la ruta indicada en la *terminal* de *Linux*

### Instalación de paquetes

* npm  install package: Instala el paquete indicado.
 * npm install moment: Paquete para trabajar con fechas en JavaScript.
 * -S | -save: Instala la dependencia en el entorno de producción
 * -D | -save-date: Instala la dependencia en el entorno de desarollo
 * -g: Instala la dependencia de modo global, en caso de un proyecto de grupo que tenga una dependencia común para todos por ejemplo.
 * --dry-run: Simula la instalación para poder comprobar los paquetes a instalar.
 * -f: fuerza la instalación del paquete.
* npm install: instala todas las dependencias del package.json

### Actualizar y eliminar paquetes

* npm list: Muestra un lista de todos los paquetes instalados.
* npm outdate: Busca paquetes desactualizados.
* --dd: muestra el output más detallado de cualquier comando.
* npm update: Actualiza los paquetes.
 * npm install package@**latest**: indicamos que instale la última versión
* npm unistall package: Desintala el paquete seleccionado.
 * --no-save: Desinstala el paquete pero no lo elimina del package.json.

* npm cache clean --force: Elimina la cache de las dependencias
* npm cache verify: Nos muestra los datos de la cache

* Eliminar la carpeta node_modules elimina todos los paquetes.
* npm install -g rimraf: Instala un paquete de forma globar para poder elimiar después, esto se hace en caso de no poder eliminar node_modules
 * rimraf node_modules/: Elimina la carpeta

### Scripts

Se añaden la parte de scripts del packgae.json

```javascript
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "deploy": "npm run format && npm run build"
  },
  
```

### Auditar paquetes

* npm audit: Comprueba vulnerabilidades.
 * npm audit fix: Intenta solucionar todas las vulnerabilidades.

En caso de quedar algún paquete sin solucionar, hay que hacerlo de uno en uno con *npm update package*

### Subir paquetes a npm

* npm link: Instala los paquetes globales que hayamos creado en local.

Creamos una cuenta en npm:
* npm adduser: Seguimos los pasos para logearnos
* npm publish: Sube el paquete a tu "*repositorio*"

Los paquetes en npm necesitan un repositorio:
* git remote add origin *url_repositorio*
* npm init: para volver a iniciar todo el proyecto con el repositorio
* npm version: permite indicar el tipo de cambio
 * npm version patch
 * npm version minor
 * npm version mahjor






