# Instalacion de PhoneGap




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




## PhoneGap Developer App

- Aplicación que podemos [descargar del App Store o del Play Store](http://docs.phonegap.com/getting-started/2-install-mobile-app/).
- Nos da acceso a un preview de nuestra aplicación:
  - No tenemos necesidad de instalar el SDK
  - Se compila utilizando los servicios de PhoneGap
  - El movil tiene que tener acceso al equipo de desarrollo (misma red wifi)
  

## Prueba 

- Creamos una aplicación de ejemplo:

```
$ phonegap create helloWorld
$ cd helloWorld
```
- Accede a la aplicación desde el navegador

```
$ phonegap serve
```

- Accede a la aplicación desde el navegador del PC
- Accede a la aplicación desde PhoneGap Developer

- Comprueba la diferencia entre ambas ejecuciones.
- En el segundo caso los plugins están "funcionando". Pare el caso del navegador se instala una *browser platform* que simula el comportamiento de los plugins.
  
## Compilación para Android
- Primero comprobamos que tenemos los requerimientos
  ```
  C:\Users\JuanDaniel\Desktop\project1>cordova requirements android
  
  Requirements check results for android:
  Java JDK: installed 1.8.0
  Android SDK: installed true
  Android target: installed android-25
  Gradle: installed C:\Program Files\Android\Android Studio\gradle\gradle-3.2\bin\gradle
  ```
* Si falta el JDK, se puede [descargar de Oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

- Luego compilamos
```
$ cordova build android
```
- El apk se genera en la ruta *platforms/android/build/generated/outputs/apk*

## Instalación en el teléfono 
- La forma más cómoda de instalarlo es usando la aplicación [Airdroid](https://web.airdroid.com/)
- Otra opción de instalación es utilizar alguna aplicación con el nombre del tipo *apk installer*
- Para poder instalarla es necesario tener dar acceso desde el menú en *Ajustes/Seguridad/Origenes Desconocidos*
- Observa que al instalarse pide los permisos correspondientes según el archivo *platforms/android/AndroidManifest.xml*

## Compilación en la nube de Adobe
- Subimos un zip con todo nuestro proyecto
  - La carpeta platform no, ¡es el favor que nos hacen!
- Si utilizamos git, podemos hacer un pull request

Opciones de compilación:
- Enable debuggin

- Enable hiratation

## Prueba en un emulador
- 

## Publicar en repositorios
- Si queremos monetizar nuestra aplicación es lo más conveniente
- Las distintas plataformas se llevarán un 30% en la venta y un 15% en las suscripciones
- Además necesitamos tener una cuenta de desarrollador para publicar apps
- Una vez envíada la aplicación debe ser aprobada

## Publicar en el Play Store
- Es el repositorio de aplicaciones para dispositivos Android
- Cuota de $25 una única vez
- [Publicar app](https://play.google.com/apps/publish/signup/)


## Enviar al app store
- Es el repositorio de aplicaciones para dispositivos IOS
- Cuota de $99 cada año
- [Publicar app](https://developer.apple.com/app-store/submissions/)

## Enviar al Windows Store
- Es el repositorio de aplicaciones para dispositivos Windows
- Cuta única de $12
- [Publicar app](https://developer.microsoft.com/es-es/store/publish-apps)