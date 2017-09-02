# Aplicación móvil con Bootstrap


## Tecnologías
- Utilizaremos Twitter Bootstrap
- Se trata de un sitio web específico para dispositivos móviles
- Instalaremos un plugin en Visual Studio para que nos genere el código de Bootstrap con poco esfuerzo


## Configuración de Visual Studio

- Instalamos [Bootstrap 3 Snippets](https://marketplace.visualstudio.ocom/items?itemName=wcwhitehead.bootstrap-3-snippets)
- Comprobamos que nos funcione (tecleamos bs3-...) y debe disparar una lista de snippets para escoger el que nos interese.


## Nuevo proyecto
- Creamos nuevo proyecto mediante PhoneGap Desktop o mediante el CLI
- Nos basaremos en un proyecto vacío
- Consistirá en un portfolio de cada uno, una especie de CV
- Comprobamos que se lance bien el nuevo proyecto

## Primeros pasos
- Modificamos el fichero config.mxl (name, description y author)
- Añadimos las carpetas js, fonts y css
  - [Descargamos bootstrap](http://getbootstrap.com/docs/3.3/getting-started/#download) en dichas carpetas y el [plugin de jQuery](https://jquery.com/download/)
    - No usamos un CDN ya que queremos que funcione sin Internet
    - Podemos usar un css más "personalizado" usando https://bootswatch.com/
     ```
     
- Comprobamos que tengamos "estilo bootstrap" añadiendo algún snippet.
- Miramos en la consola que no haya ningún error.

## Plugins
- Nuestro JavaScript irá en el fichero *js/index.js*
   - Por el momento, responderemos al evento *deviceReady* 
   - Simplificaremos el código del template de helloWorld:
     ```
     document.addEventListener('deviceReady', onDeviceReady, false);
     
     function onDeviceReady () {
       console.log('Dispositivo listo!!!!')
     }

- Necesitamos algún plugin que gestione el evento *deviceReady*