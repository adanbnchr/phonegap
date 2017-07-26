## Instalación de Android Studio

* Seguimos las [instrucciones de instalación](https://developer.android.com/studio/install.html) seleccionando nuestro sistema operativo.

## Instalación de Java

```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

## Instalación de Graddle

```
sudo apt-get update
sudo apt-get install gradle
```

### Variables de Shell

* Fichero _$HOME/.zshrc_ para el **shell zsh**:

  ```
  export ANDROID_HOME='/home/usuario/Android/Sdk'
  path+=('/home/usuario/Android/Sdk/tools' '/home/usuario/Android/Sdk/platform-tools')
  ```

* Añado también el repositorio de los binarios de npm \(lo utiliza Sublime Text y al usar zsh hay que dárselo\). Fichero _$HOME/.zshenv:_

  ```
  path+=('/home/usuario/.nvm/versions/node/v5.0.0/bin/')
  ```

## Añadir plataforma

* Después de la @ \(opcional\) va la versión. Con la 6.1.2 \(por defecto\) da un error.
  ```
  phonegap platform add android@latest # 6.3.1 with default... error!
  ```

### Test de funcionamiento

* Necesitamos un AVD \(Android Virtual Device\) disponible con [API no superior a 25](https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html#requirements-and-support)

* Para añadir el dispositivo se puede hacer desde Android Studio - Tools

* Posteriormente ejecutamos nuestro proyecto.

  ```
  phonegap run android
  ```

## Escenarios de compilación

* Ver [que niveles soporta nuestra aplicación](https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html)

* [Dipositivos soportados](https://developer.android.com/about/dashboards/index.html)

* Compilación en local

  * Necesitamos los sdk

* Compilación en la nube de Adobe

## Targets para compilación
- IOS requiere una firma y pagar la licencia de desarrollo
- Windows Phone está poco extendido
- Android permite instalar los apk, sin necesidad de pasar por el Play Store
- Utilizaremos Android

## Compilación en local

* Generar el apk por nuestra cuenta
  ```
  phongap build android
  ```

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

## Instalación en el teléfono

- Mediante alguna aplicación de tipo [AirDroid](https://play.google.com/store/apps/details?id=com.sand.airdroid) o mediante algún [apk installer](https://play.google.com/store/search?q=apk%20installer&c=apps)

