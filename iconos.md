# Creación de iconos

## Problemática de los iconos
- Se realiza en el fichero config.xml
- Una vez por cada plataforma
- [Mira ejemplos en la documentación](https://cordova.apache.org/docs/en/latest/config_ref/images.html)
- Para el browser no son necesarios
- Mira por ejemplo para Android:
```
    <platform name="android">
        <!--
            ldpi    : 36x36 px
            mdpi    : 48x48 px
            hdpi    : 72x72 px
            xhdpi   : 96x96 px
            xxhdpi  : 144x144 px
            xxxhdpi : 192x192 px
        -->
        <icon src="res/android/ldpi.png" density="ldpi" />
        <icon src="res/android/mdpi.png" density="mdpi" />
        <icon src="res/android/hdpi.png" density="hdpi" />
        <icon src="res/android/xhdpi.png" density="xhdpi" />
        <icon src="res/android/xxhdpi.png" density="xxhdpi" />
        <icon src="res/android/xxxhdpi.png" density="xxxhdpi" />
    </platform>
```
- No es posible utilizar imágenes vectoriales :-(

## Generación de iconos
- Utilizaremos el [módulo npm cordova-icon](https://www.npmjs.com/package/cordova-icon) para facilitarnos la tarea
    - Lo instalamos mediante *npm i -g cordova-icon*
    - Instalamos también image-magick (ver requerimientos del módulo anterior)
- Otra opción sería utilizar [app-icon](https://github.com/dwmkerr/app-icon), pero [en Windows tiene bugs](https://github.com/dwmkerr/app-icon/issues/37)

- Situamos nuestro icono *icon.png* con buena resolución en el raíz del proyecto
- Ejecutamos ```cordova-icon``` para que nos genere los iconos correspondientes.

- Si queremos hacerlo por plataforma basta con llamar los iconos como icon-[platform].png
- Se puede automatizar configurándolo como un *hook*
- Otra opción [usar algún servicio web](https://resizeappicon.com/)

