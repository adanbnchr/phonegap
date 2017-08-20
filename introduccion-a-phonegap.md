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
- Necesidad intrínseca de aplicaciones multiplataforma. Ej: WhatsApp
- La experiencia de usuario en la aplicación debe ser consistente entre plataformas:
  - Un usuario puede migrar de SO incluso utilizar varios
  - La experiencia de usuario podría variar entre dispositivos en función de las características y capacidades de los dispositivos



## ¿Qué es PhoneGap?

* Framework para desarrollo de aplicaciones híbridas
* Nuestro código se realiza mediante HTML, CSS y JavaScript
* ¿¿¿Algún gráfico??

## PhoneGap UI

* Se utilizan frameworks de CSS específicos
  * Animaciones CSS "ligeras" para la CPU
  * Componentes específicos de móviles \(menú lateral tipo slide...\)
  * Aspecto similar a las plataformas de destino 

## API de PhoneGap

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
* Para IOS es necesaria una _**developer key**_

## ¿Qué es Cordova?

* Cordova es el núcleo o motor que utiliza PhoneGap
* PhoneGap es una distribución de Apache Cordova con funcionalidad adicional
* A la hora de desarrollar -sin más-, son la misma cosa.



