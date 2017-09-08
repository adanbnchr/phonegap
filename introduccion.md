# Aplicación móvil con Bootstrap


## Tecnologías
- Realizaremos una webapp que empaquetaremos con Phonegap
- Utilizaremos Twitter Bootstrap
- Posteriormente podremos añadir funcionalidad nativa:
  - Añadir los datos del contacto a la agenda
  - ...

## Configuración de Visual Studio

- Instalamos plugin para visual code editor [Bootstrap 3 Snippets](httpts://marketplace.visualstudio.ocom/items?itemName=wcwhitehead.bootstrap-3-snippets)
  - Nos generá los snippets de de Bootstrap
- Comprobamos que nos funcione:
  - Tecleamos bs3-...
  - Debe disparar una lista de snippets para escoger.


## Nuevo proyecto
- Nos basaremos en un proyecto vacío
- Consistirá en un curriculum/portfolio de una empresa o un individuo
- Seguiremos las pautas que aquí se detallan personalizándolo para nuestras necesidades.
- Comprobamos que se lance bien el nuevo proyecto
- Creamos nuevo proyecto mediante el CLI de Cordova
```
cordova create curriculum
```

- Comprobamos que se lance bien el proyecto
```
cordova platform add browser
cordova serve
```
  - Tenemos que estar situados dentro del proyecto
  - Con Cordova es necesario añadir la plataforma browser (en PhoneGap se hace automático)
  

## Primeros pasos
- Modificamos el fichero config.mxl (name, description y author)
- Añadimos las carpetas js, fonts y css
  - [Descargamos bootstrap](http://getbootstrap.com/docs/3.3/getting-started/#download) y lo llevamos a las carpetas correspondientes
  - Descargamos también el [plugin de jQuery](https://jquery.com/download/)
    - No usamos un CDN ya que queremos que funcione sin Internet
    - Podemos usar un css más "personalizado" usando https://bootswatch.com/
    - Bootstrap necesita jQuery, ¡ojo con el orden!
    - Y recuerda.... el css en el *head* de la página, los js al final del body.
 
## Comprobamos que funcione nuestro boilerplate
- Eliminamos el contenido de ejemplo del *index.html*
```
        <div class="app">
            <h1>Apache Cordova</h1>
            <div id="deviceready" class="blink">
                <p class="event listening">Connecting to Device</p>
                <p class="event received">Device is Ready</p>
            </div>
        </div>
```
- Comprobamos que tengamos "estilo bootstrap" añadiendo algún snippet.
- Miramos en la consola que no haya ningún error.


## Creación de la web
- Creamos un navbar responsive con el menú siguiente:
  - Inicio
  - Sobre mi
  - Servicios
  - Contactar



## Iconos
- Utilizaremos los iconos de [font awesome](http://fontawesome.io/icons/)
  - Más cantidad que los que vienen con Bootstrap
  - Open Source
- Otras opciones:
  - https://material.io/icons/
  - https://thenounproject.com/
  - ...

- Descargamos la librería de iconos y copiamos las carpetas *css* y *fonts* a nuestro proyecto
- Añadimos la hoja de estilos a nuestro html:
```
    <link rel="stylesheet" href="css/font-awesome.min.css">
```


## Funcionalidad nativa
- Para llamar a la funcionalidad nativa del teléfono lo haremos comunicándonos con la librería *cordova.js*
- No podremos llamar a la funcionalidad nativa del teléfono hasta que la libería de cordova esté cargada 
- La libería de cordova dispara el evento *deviceReady* una vez está cargada

- Configuraremos un aviso en consola de momento para ver cuando se carga
  - Se utiliza la función addEventListener que recibe el nombre del evento y la función que manejará el evento
- Nuestro JavaScript irá en el fichero *js/index.js*
     ```
     document.addEventListener('deviceReady', onDeviceReady, false);
     
     function onDeviceReady () {
       console.log('Dispositivo listo!!!!')
     }
    ```


## Ejercicio
* Ejercicio: Prueba a sacar por consola un mensaje cuando el usuario baje o suba el volumen de su teléfono. 
  * Los eventos son *volumedownbutton* y *volumeupbutton*
  
## Solución ejercicio

- El código sería similar al siguiente:

```
document.addEventListener('volumedownbutton', bajarVolumen, false);
document.addEventListener('volumeupbutton', subirVolumen, false);

function bajarVolumen() {
  console.log ('He bajado el volumen');
}

function subirVolumen(){
  console.log('He subido el volumen');
}
```

- Pero... ¿como lo comprobamos?
  - Necesitamos hacer debug del código 


## Debug
- *console.log*, *console.error*, *console.warn* nos sirve solo si:
  - Miramos las trazas de log del emulador o del dispositivo remoto mediante 
  *adb* (android device bridge)
  - Conectamos nuestro navegador del PC al webview mediante chrome://inspect (en principio necesitamos conectar el movil mediante USB)
  - [Instalamos el paquete de node Weinre e inyectamos un código en nuestro index.html](http://docs.phonegap.com/phonegap-build/tools/weinre/)
  
- Otra opción es utilizar *alert* en vez de *console.log*
  
  
