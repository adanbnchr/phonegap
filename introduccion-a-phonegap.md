# Introducción a PhoneGap

## Un poco de historia
* Desarrollos para Linux/Unix, Windows y Mac
* Aparece Java
* Desarrollo Web para distintos navegadores: Explorer, Safari y Firefox
* Aparecen nuevos navegadores como Chrome y Opera provocando mayor fragmentación
* Aparecen frameworks como jquery, YUI o Google Web Toolkit
* Los navegadores empiezan a seguir las especificaciones de la W3C y últimamente casi todos se apoyan en WebKit (el último Opera).


## Situación actual
* Hay muchas plataformas distintas para smartphones en el mercado
  * Android, iPhone, BlackBerry, Nokia, Windows8 Phone, WebOS, Tizen, FirefoxOS...
  * Se extinguen otras como Bada y Meego
* La fragmentación es fuerte entre los distintos fabricantes ya que no se sigue ningún tipo de especificación o estándar común
*   Se aprecia cierta tendencia a sistemas operativos desarrollados mediante html5: Tizen, WebOS, FirefoxOS

## SO más vendidos en la actualidad

![](/assets/sistemas-operativos.png)


- A día de hoy y en cifras [(fuente Gartner)](http://www.gartner.com/newsroom/id/3725117)
![](/assets/Captura de pantalla 2017-08-20 a las 20.42.47.png)

- Evolución 
![](/assets/evolucion-moviles.png)

- Aunque depende de cada país (que la sombra de los árboles no te impida ver el bosque)
![](/assets/evolucion-moviles-usa.png)

## Tipos de dispositivos más usados

![](/assets/tipo_dispositivo.png)

## Fabricantes móviles
![](/assets/fabricantes.png)


## Requerimientos de usabilidad en móviles
- Necesidad intrínseca de aplicaciones multiplataforma. Ej: WhatsApp:
  - IOS
  - Android
  - Windows
  - Web
- La experiencia de usuario en la aplicación debe ser consistente entre plataformas:
  - Un usuario puede migrar de SO incluso utilizar varios
  - La experiencia de usuario podría variar entre dispositivos en función de las características y capacidades de los dispositivos


## Requerimientos de desarrollo

![](/assets/mobile_development_requirements.png)

## ¿Qué es Apache Cordova?

![](/assets/cordova_bot.png)

http://cordova.apache.org/

## ¿Qué es PhoneGap?

![](/assets/phonegap_logo.png)

http://phonegap.com/

## Diferencias

- Cordova es el proyecto Open Source que es la base de PhoneGap
- Normalmente se habla de PhoneGap y nos referimos a cualquiera de ellos indistintamente
- Apache Cordova es la base de PhoneGap, su motor. Lo mismo que WebKit es la base de Chrome o Safari.
- PhoneGap es una distribución de Apache Cordova con funcionalidad adicional
- A la hora de desarrollar -sin más-, son la misma cosa.


## Similitudes

* Son un framework (el mismo) para desarrollo de aplicaciones híbridas
* Nuestro código se realiza mediante HTML, CSS y JavaScript


## Solución única para las distintas plataformas móviles
- Se usan lenguajes de programación y estándares comunes a todas ellas: HTML, CSS y JavaScript
- Las aplicaciones nativas se muestran embebidas en un WebView
- Sigue estándares
- En un mundo ideal no sería necesario


## Librerías para acceso a la funcionalidad nativa del dispositivo
![](/assets/phonegap api.png)
- Liberías "comunes" mediante JavaScript: cordova.js y plugins.
- Librerías específicas para cada dispositivo en C#, Objective C, Java..



## PhoneGap UI (o Cordova)

* Se utilizan frameworks de CSS específicos
  * Animaciones CSS "ligeras" para la CPU
  * Componentes específicos de móviles \(menú lateral tipo slide...\)
  * Aspecto similar a las plataformas de destino 


## API de PhoneGap (o Cordova)

* Nos permite interaccionar con el dispositivo movil:
  * Contactos
  * Brújula
  * Geolocalización / GPS
  * Acelerómetro
  * Fotos / Video
  * Almacenamiento interno
  * Vibración
  * Estado de red / baterial
  * ...

## Desarrollo en PhoneGap y Testing

* PhoneGap Desktop Tool

  * Depuración mediante navegador
  * Movil conectado en red local

  * Entorno SDK de desarrollo
  * Entorno IOS XCode

## Empaquetado de aplicaciones

* **PhoneGap Build**: Servicio de compilación en la nube
- PhoneGap permite compilar en la nube y no depender de un hardware concreto
  - Proyectos Open Source ilimitados
  - Un proyecto privado sin coste
* Para IOS es necesaria una _**developer key**_

![](/assets/phonegap_flow.png)

## Arquitectura
![](/assets/arquitectura_phonegap.png)


## Uso de tecnologías Web
- Se basa en la parte común de todos los dispositivos móviles: el navegador
- Los nuevos navegadores se adhieren a estándares como HTML5/CSS3
- HTML5 nos da mucha funcionalidad: procesos en background mediante web workers, soporte offline, base de datos...
- CSS3 permite que nos despidamos de flash para realizar gradientes, bordes redondeados, páginas responsivas, vistas de impresión, etc.
- Todas las plataformas móviles excepto Windows 7 Phone utilizan un navegador basado en webkit


## Webviews
- Piensa en una aplicación PhoneGap como un navegador embebido (sin marco, "chromeless browser") dentro de la aplicación y que ejecuta HMTL5/CSS.
- Estos navegadores embebidos es lo que se conoce como webview
- Cada una de las pantallas de nuestra aplicación será un webview.
- Desde el webview ejecutaremos código JavaScript que comunicará con código nativo del dispositivo.
- Todos los dispositivos permiten al código en JavaScript hacer llamadas a código nativo en Java/C++/Objective C y al revés.

## Arquitectura Javascript

- Una aplicación mediante PhoneGap tendrá dos partes bien definidas:
  - JavaScript para la parte de negocio: Interfaz de usuario y funcionalidad
  - Javascript para acceder y controlar el dispositivo


## ¿Conviene usar PhoneGap?

- Uso de estándares
- Parece que hay cierta tendencia a la web, por ej: Firefox OS
- En aplicaciones multiplataforma:
  - Un desarrollador o equipo de desarrollo no tiene porque dominar varios lenguajes de programación
  - Varios equipos de desarrollo no siempre es la mejor opción, por las necesidades de coordinación inherentes
  
## Desventajas
- El look&feel de la aplicación no será nativo
- No presenta las últimas novedades
- El código debe estar optimizado para móviles: arquitectura SPA para evitar la latencia de las redes móviles

