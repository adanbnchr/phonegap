# Compilación 

## Plataformas para compilación
- IOS:
    - Requiere una firma y pagar la licencia de desarrollo
    - Uso de equipos MAC
- Windows Phone:
    - Está poco extendido
    - Requiere equipos Windows
- Android
    - Compilación desde Windows, Mac o Linux
    - Android permite instalar los apk, sin necesidad de pasar por el Play Store
    - Muy extendido, en especial en España
    
## Nuestra elección
- El proceso de montar un entorno de programación para cualquier dispositivo móvil es costoso
- La lógica es muy similar en otros entornos
- Utilizaremos Android por ser el más versátil
    

## Requerimientos compilación para Android en Windows

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


## Requerimientos compilación para Android en Linux

```
$ cordova requirements android
```
- En mi caso he tenido que:
- Instalar Java:
```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```
- Instalar Graddle:

```
sudo apt-get update
sudo apt-get install gradle
```

- Configurar variables de shell (en mi caso con zsh), fichero _$HOME/.zshrc_ para el **shell zsh**:

```
export ANDROID_HOME='/home/usuario/Android/Sdk'
path+=('/home/usuario/Android/Sdk/tools' '/home/usuario/Android/Sdk/platform-tools')
```


## Compilación

- Mediante el comando:
```
$ phonegap build android
```
- El apk se genera en la ruta *platforms/android/build/generated/outputs/apk*


## Instalación en el teléfono

- La forma más cómoda de instalarlo es usando la aplicación [Airdroid](https://web.airdroid.com/)
- Otra opción de instalación es utilizar alguna aplicación con el nombre del tipo *apk installer*
- Para poder instalarla es necesario tener dar acceso desde el menú en *Ajustes/Seguridad/Origenes Desconocidos*
- Observa que al instalarse pide los permisos correspondientes según el archivo *platforms/android/AndroidManifest.xml*

## Compilación en la nube de Adobe

* Nos ahorramos mantener varios SDK
* [Planes de PhoneGap](https://build.phonegap.com/plans)
  * Una aplicación privada gratuita
  * Infinitas aplicaciones libres
  * [Hay restricciones en el tamaño de nuestras aplicaciones](https://build.phonegap.com/plans)
* [Haz login](https://build.phonegap.com/people/sign_in)

## ¿Qué ficheros subo?

* Se sigue la especificación de la [W3C Widget Packaging](https://www.w3.org/TR/widgets/)
* Habrá que comprimir \(.zip\) el fichero config.xml y la carpeta www.
* Si tenemos ficheros específicos de una plataforma, también el directorio merge:

  ![](/cli_project.png)


Opciones de compilación:
- Enable debugging
    - Desde el navegador se puede debuggear el código que se está ejecutando en el dispositivo movil

- Enable hidratation
    - Nuestra aplicación corre en un contenedor que se engarga de verificar si hay actualizaciones (sin usar app store o similar).

