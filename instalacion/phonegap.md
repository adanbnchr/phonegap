# Instalacion de PhoneGap

## Modos de instalación

* Podemos [instalar la aplicación gráfica](http://docs.phonegap.com/getting-started/1-install-phonegap/desktop/)
  - Funciona solo en Windows y MacOS
  
* Podemos usar la linea de comandos:
  * Características adicionales
  * Presupone un conocimiento de la línea de comandos
  * Funciona en Windows, MacOS y Linux


## Instalación de Phonegap Desktop
* Interfaz gráfica para ejecutar proyectos de Phonegap
* Mediante la  [descarga del paquete de instalación](http://docs.phonegap.com/getting-started/1-install-phonegap/desktop/)


## Intalación de la aplicación de línea de comandos
* Necesitamos [instalar nuestro cliente PhoneGap/Cordova](http://docs.phonegap.com/getting-started/1-install-phonegap/cli/)
* El cliente está programado en [NodeJS](https://nodejs.org/)
* Los paquetes de NodeJS se instalan mediante su gestor de paquetes [NPM](https://www.npmjs.com/)
* Requisitos previos: instalación de node.js y git


## ¿PhoneGap o Cordova?


* Podemos instalar dos versiones de comandos:**phonegap** o **cordova**. 
* ¿Cuál instalamos?

  * Phonegap hace lo mismo que Cordova
  * Phongap además accede a servicios y aplicaciones creadas por Adobe
  * Algunos servicios de Adobe son gratuitos

* Por lo anterior, instalamos mejor phonegap:

  ```
    $ npm install -g phonegap
  ```

* Si quisieramos instalar cordova:

  ```
    $ npm install -g cordova
  ```


## PhoneGap Developer App

- Aplicación que podemos [descargar del App Store o del Play Store](http://docs.phonegap.com/getting-started/2-install-mobile-app/).
- Nos da acceso a un preview de nuestra aplicación:
  - No tenemos necesidad de instalar el SDK
  - Se compila utilizando los servicios de PhoneGap
  - El movil tiene que tener acceso al equipo de desarrollo (misma red wifi)
  
