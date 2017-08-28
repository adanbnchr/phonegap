# Entorno de desarrollo para Android

## Android Studio

- Necesitamos [descargar Android Studio](https://developer.android.com/studio/index.html)
- Instalamos todos los componentes:
    - Android Studio
    - Android SDK
    - Android Virtual Device
- Android Studio necesita DK, pero desde la versión 2.2 viene ya el último openJDK embebido.
- Dependiendo de la plataforma podemos necesitar alguna configuración adicional relativa a los PATH principalmente.j
- Las instrucciones precisas están en la [página de descarga de Android Studio](https://developer.android.com/studio/install.html)

## Configuración
- Al arrancar Android Studio debemos ir a Configure->SDK Manager
    - Instalamos las imagenes que nos hagan falta
    - Elegimos 64 bits (depende de nuestra arquitectura)
- Dentro de Android Studio podemos acceder al Adnroid Virtual Device Manager
    - Definimos nuestro dispositivo para pruebas
