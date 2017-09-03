# Introducción a PhoneGap



## Tipos de aplicaciones móviles

![](/assets/3apps-highlight.png)


## Descripción de aplicaciones móviles

- **Webapps** 
    
    Sitios web o aplicaciones web que se ejecutan en un navegador
    
- **Aplicaciones nativas**

    Típicas aplicaciones del teléfono. Se descargan del app store.   
    
- **Aplicaciones híbridas**

    Una mezcla de las anteriores


## Webapps

* Se construyen mediante HTML, CSS y JavaScript
* Se ejecutan a través de un navegador
* Se diseñan para verse bien en dispositivos móviles:
    - Diseño específico
    - Uso de [CSS Media Queries](https://developer.mozilla.org/es/docs/CSS/Media_queries)


## Ventajas de Webapps
* Más fáciles de generar (HTML, CSS y JavaScript)
* Una aplicación única para todos los dispositivos

     
## Desventajas webapps
* Más lentas
* Menos interactivas e intuitivas
* Sin icono (a través del navegador)
* No están en un app store 
* No pueden ejecutar funcionalidad nativa del teléfono (cámara, agenda contactos...)


## Aplicaciones Nativas

* Las aplicaciones habituales que se ejecutan en los teléfonos
* Se crean usando un lenguaje específico para cada plataforma
    * .net (Windows Phone)
    * java (Android)
    * swift (Apple)
    
* Pueden tener requerimientos para su compilación

* Se suelen descargar del store correspondiente
    * Play Store
    * App Store
    * Microsoft Store


## Ventajas aplicaciones nativas
* Muy rápidas
* Muy interactivas e intuitivas
* Se pueden encontrar en los app store
* Ejecutan cualquier funcionalidad nativa del teléfono


## Desventajas
* Un lenguaje de programación por cada plataforma
    * Más caras
    * Más dificiles de mantener


## Aplicaciones Híbridas
* Combinación de aplicaciones nativas y webapps
* Usan HTML, CSS y JavaScript
* Se ejecutan en un WebView (navegador sin marcos)
* Se nos proporciona API de acceso a la funcionalidad nativa.
    * La API es homogenea entre dispositivos
    * La API puede tener varias capas, una en código nativo


## Ventajas aplicaciones híbridas
* Un único desarrollo (multiplataforma)
    - Más rápido
    - Menor coste
* No necesita navegador
* Accede a funcionalidad nativa del dispositivo


## Desventajas aplicaciones híbridas
* Más lentas que las aplicaciones nativas
* Menos interactivas que las aplicaciones nativas
* Más caras que las webapps


## React-native
- Nueva generación de desarrollos para móviles
- Mediante HTML, CSS y JavaScript
- Compila a código nativo
- Todavía con pocos plugins disponibles
- Existen otras tecnologías (peores)
    - Xamarin: C# a código nativo
    - Titanium: HTML, CSS y JavaScript a código nativo

