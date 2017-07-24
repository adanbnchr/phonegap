


* Necesitamos instalar nuestro cliente PhoneGap/Cordova
* El cliente está programado en [NodeJS](https://nodejs.org/)
* Los paquetes de NodeJS se instalan mediante su gestor de paquetes [NPM](https://www.npmjs.com/)

## Instalación de PhoneGap

* Podemos [instalar la aplicación gráfica](http://docs.phonegap.com/getting-started/1-install-phonegap/desktop/) en Windows o MacOS
* Podemos usar la linea de comandos:
  * Características adicionales
  * Presupone un conocimiento de la línea de comandos
  * Funciona en Windows, MacOS y Linux
  * Requisitos previos: instalación de node.js y git


* Podemos instalar dos versiones de comandos:**phonegap** o **cordova**. 
* ¿Cuál instalamos?

  * Phonegap hace lo mismo que cordova
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

## PhoneGap Developer

- Aplicación que podemos descargar del App Store o del Play Store.
- Nos da acceso a un preview de nuestra aplicación:
  - No tenemos necesidad de instalar el SDK
  - Se compila utilizando los servicios de PhoneGap
  - El movil tiene que tener acceso al equipo de desarrollo (misma red wifi)
  

## Prueba 

- Creamos una aplicación de ejemplo:

```
phonegap create helloWorld
cd helloWorld
phonegap serve
```

- Accede a la aplicación desde el navegador del PC
- Accede a la aplicación desde PhoneGap Developer

- Comprueba la diferencia entre ejecutarlo en un navegador y en el propio dispositivo 
  



