
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


## Instalación en el teléfono

- Mediante alguna aplicación de tipo [AirDroid](https://play.google.com/store/apps/details?id=com.sand.airdroid) o mediante algún [apk installer](https://play.google.com/store/search?q=apk%20installer&c=apps) que permiten también compartir la aplicación con amigos.


