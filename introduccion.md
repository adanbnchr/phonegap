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
- Creamos nuevo proyecto mediante el CLI de Cordova
```
cordova create curriculum
```

- Comprobamos que se lance bien el proyecto
  - Tenemos que estar situados dentro del proyecto
  - Con Cordova es necesario añadir la plataforma browser (en PhoneGap se hace automático)
```
cordova platform add browser
cordova serve
```

  
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
- Añadimos algún snippet de bootstrap y comprobamos que tengamos "estilo bootstrap" añadiendo algún snippet.
- Miramos en la consola del navegador que no haya ningún error.
