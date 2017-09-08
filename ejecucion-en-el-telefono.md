# Ejecución en el teléfono


## Instalación mediante el .apk

- Necesitamos haber compilado la aplicación
- Se copia el apk al dispositivo y se ejecuta para que se instale
- La forma más cómoda de instalarlo es usando la aplicación [Airdroid](https://web.airdroid.com/)
- Otra opción de instalación es utilizar alguna aplicación con el nombre del tipo *apk installer*

## Configuración de permisos

- Para poder instalarla es necesario habilitar la opción en el movil de *Ajustes/Seguridad/Origenes Desconocidos*
- Al instalarse el apk, pide permisos según el archivo *platforms/android/AndroidManifest.xml*


## Instalación mediante PhoneGap Developer App

- Aplicación que podemos [descargar del App Store o del Play Store](http://docs.phonegap.com/getting-started/2-install-mobile-app/).
- Nos da acceso a un preview de nuestra aplicación:
  - No tenemos necesidad de instalar el SDK
  - Se compila utilizando los servicios de PhoneGap
- La aplicación es bastante exigente en requerimientos:
  - Puede ser que [no funcione en nuestro dispositivo](https://github.com/phonegap/phonegap-app-developer/issues/408)
- Levantamos un servidor mediante:

```
phonegap serve
```

- La IP que nos ofrece al levantar el servidor habrá que copiarla en PhoneGap Developer App para comunicar el móvil y el servidor
- Si el PC y el movil no están en la misma red, no habrá comunicación, por lo que habrá que arrancarla mediante un tunel:
```
phonegap serve --localtunnel
```
- **Si instalamos plugins fuera de los oficales, este método de desarrollo no nos sirve**


