# Interfaz de la aplicación


## Creación de la web
- Creamos un menú responsive con el menú siguiente:
    - Inicio
    - Sobre mi
    - Servicios
    - Contactar
- Utilizaremos el elemento de bootstrap *navbar* en su versión (clase) responsive.


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

- Aumentamos el tamaño de los iconos definiendo una clase nueva en el index.css:
```
.big {
    font-size: 60px;
}
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
- [Instalamos el paquete de node Weinre e inyectamos un código en nuestro index.html](http://docs.phonegap.com/phonegap-build/tools/weinre/#running-a-local-debug-server)
- Otra opción es utilizar *alert* en vez de *console.log*
## Añadir datos a la agenda de contactos
- En contactar añadiremos además del formulario un botón para guardar el contacto
- Guardaremos los siguientes datos:
- Nombre
- Apellido
- Teléfonos de contacto (más de uno)
- Email
- Debemos utilizar el plugin de contactos](https://cordova.apache.org/docs/en/latest/reference/cordova-plugin-contacts/index.html)
- Se instala mediante:
```
cordova plugin add cordova-plugin-contacts
```
- El código que podríamos añadir:

```
document.getElementById('btnContact').addEventListener('onClick', addContact, false);
function onSuccess(contact) {
    alert("Se ha guardado el contacto");
};
function onError(contactError) {
    alert("Error = " + contactError.code);
};
function addContact() {
    // create a new contact object
    var contact = navigator.contacts.create();
    contact.displayName = "Lionel Messi";
    contact.nickname = "Messi";
    // telefonos de contacto
    var phoneNumbers = [];
    phoneNumbers[0] = new ContactField('work', '768-555-1234', false);
    phoneNumbers[1] = new ContactField('mobile', '999-555-5432', true); // preferred number
    phoneNumbers[2] = new ContactField('home', '203-555-7890', false);
    contact.phoneNumbers = phoneNumbers;
    // emails
    var emails = [];
    emails[0] = new ContactField('Trabajo', 'asdf@adsf.com', false);
    emails[1] = new ContactField('Personal', 'asdfg@asdf.com', true); // preferred number
    contact.emails = emails;
    // Nombre del contacto
    var name = new ContactName();
    name.givenName = "Lionel";
    name.familyName = "Messi";
    contact.name = name;
    // guardamos
    contact.save(onSuccess,onError);
}
```