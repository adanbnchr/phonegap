## Ejecución desde el PC
- Ejecutamos el siguiente comando:
```
phonegap run android
```
- En primer lugar la aplicación se compila
- La aplicación se intentará instalar y ejecutará en:
    - El dispositivo físico si está conectado
    - Un emulador que haya corriendo

```
....
BUILD SUCCESSFUL

Total time: 2.392 secs
Built the following apk(s):
        C:/Users/JuanDaniel/Desktop/demo1/platforms/android/build/outputs/apk/android-debug.apk
ANDROID_HOME=C:\Users\JuanDaniel\AppData\Local\Android\sdk
JAVA_HOME=C:\Program Files\java\jdk1.8.0_144
No target specified and no devices found, deploying to emulator
Error: No emulator images (avds) found.
1. Download desired System Image by running: "C:\Users\JuanDaniel\AppData\Local\Android\sdk\tools\android.bat" sdk
2. Create an AVD by running: "C:\Users\JuanDaniel\AppData\Local\Android\sdk\tools\android.bat" avd
HINT: For a faster emulator, use an Intel System Image and install the HAXM device driver

```



## Creación de dispositivo

* Necesitamos un AVD \(Android Virtual Device\) disponible con [API no superior a 25](https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html#requirements-and-support)

* Para añadir el dispositivo se puede hacer desde Android Studio - Tools

* Posteriormente ejecutamos nuestro proyecto.

```
phonegap run android
```







