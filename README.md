# Nuevas características Angular 7

Las nuevas características que se incorporan en esta nueva versión y que nos indican en su changelog son:
  - **core**: add DoBootstrap interface.
  - **compiler**: add "original" placeholder value on extracted XMB
  - **compiler-cli**: add support to extend angularCompilerOptions
  - **bazel**: add additional parameters to ts_api_guardian_test def
  - **elements**: enable Shadow DOM v1 and slots
  - **platform-server**: update domino to v2.1.0
  - **router**: warn if navigation triggered outside Angular zone
  - **router**: add UrlSegment[] to CanLoad interface
 
Por otro lado, las versiones de las librerías más importantes que cambian son:
@angular/core now depends on
  - **TypeScript** 3.1
  - **RxJS** 6.3
 
@angular/platform-server now depends on 
  - **Domino** 2.1

Angular 7 es compatible con Node 10, sin embargo, se podrá seguir utilizando Node 8.
Varios bugs corrigen en esta versión. Dado que el listado es bastante amplio, os remitimos a su página oficial: https://github.com/angular/angular/blob/master/CHANGELOG.md

### Opciones para crear un proyecto Version 7:

##### 1.- Proyecto desde cero
(si ya teníamos instalado Angular CLI, deberemos desinstalarlo, vaciar el caché y luego instalar la última versión.
```sh
npm uninstall -g angular-cli
npm cache clean or npm cache verify (if npm > 5)
npm install -g @angular/cli@latest
``` 

Ya podríamos generar un proyecto con el comando 
```sh
ng new new-project
``` 
 
##### 2.- Hacer upgrade a versión Angular 7

Debemos partir de una versión de Angular 6. Ya que, si recordamos, en esta versión se introdujeron cambios en la estructura base del proyecto, así como en las dependencias. Entonces: 
```sh
ng update @angular/cli @angular/core
```

Además, como indican en su blog, sería interesante revisar en los polyfills si tenéis activado el reflect, y actualizar el angular.json para reducir el tamaño de los budgets:
```
"budgets":
[{
  "type": "initial",
  "maximumWarning": "2mb",
  "maximumError": "5mb"
}]
```
Otras mejoras son:
  - Mejora en el rendimiento de la aplicación.
  - Utilización de la nueva versión de Typescript y RxJS.
  - Uso de las nuevas versiones y funcionalidades de Angular y el CDK.
  - Mejora en la accesibilidad.
  - Angular Elements ahora permite la compatibilidad con los estándar custom elements.

### Nuevos componentes y utilidades de la comunidad
  * Nuevo Componente **Virtual Scrolling** 
  Una característica común en las aplicaciones web modernas es el desplazamiento de listas, no es sorprendente que el desplazamiento virtual sea una característica clave en esta versión.
  Las principales aplicaciones web del mundo están llenas de listas. El desplazamiento virtual es una técnica que maneja esto mostrando un número constante de elementos de la lista y cargando más a medida que el usuario se desplaza hacia abajo. Esto significa que el navegador puede hacer menos procesamiento de datos y proporcionar una experiencia de usuario más rápida.
  * Nuevo Componente de **Drag and Drop**
  De manera similar, el componente Drag and Drop permite arrastrar y soltar de una manera fácil para el desarrollador.
  El equipo de Angular declara en la [documentación oficial del componente](https://material.angular.io/cdk/drag-drop/overview):
  “El módulo @ angular / cdk / drag-drop le proporciona una manera de crear de forma fácil y declarativa interfaces de arrastrar y soltar, con soporte para arrastrar de forma gratuita, clasificar dentro de una lista, transferir elementos entre listas, animaciones, dispositivos táctiles, controles de arrastre personalizados, vistas previas y marcadores de posición, además de listas horizontales y bloqueo a lo largo de un eje."
  * **Default Performance Budgets** o Presupuestos de rendimiento predeterminados
  El presupuesto de rendimiento es la definición de restricciones de memoria en una aplicación, un presupuesto para la cantidad de memoria que se debe usar.
  Angular 7 permite el presupuesto de rendimiento por defecto, permitiendo a los desarrolladores cambiar sin esfuerzo, aumentando o reduciendo su presupuesto de memoria a través de la actualización del archivo angular.json, añadiendo esta funcionalidad según lo necesiten tal y como se muestra a continuación:
  * [Angular Console](https://angularconsole.com/): una **consola visual** que te permite arrancar y ejecutar proyectos Angular en la máquina local sin tener que acordarte de todos los parámetros que se usan en el CLI y automatizando algunas cosas por ti. Te facilitará el uso de Angular.
  * [Angular Fire 2](https://github.com/angular/angularfire2): la biblioteca oficial para usar **Firebase** desde Angular.
  * [NativeScript](https://docs.nativescript.org/code-sharing/intro): para crear aplicaciones nativas a partir de tu aplicación web.
  * [Stackblitz](https://stackblitz.com/fork/angular): el **editor online** específico para Angular que te permite programar y compartir las aplicaciones creadas directamente desde tu navegador, sin instalar nada en local.

#### Actualización de la documentación
La documentación en angular.io ahora incluye la [referéncia al material de Angular CLI](https://angular.io/cli).

