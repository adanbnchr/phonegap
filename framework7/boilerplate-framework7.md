# Boilerplate Framework7



## ¿Qué es Framework7?
- Es un framework para crear aplicaciones para Android y IOS
- Nos da una apariencia nativa de las aplicaciones
- Utiliza una librería específica (dom7) para acceso al DOM (en vez de jQuery)
- Utiliza un sistema de templates (template7) basado en [handlebars](http://handlebarsjs.com/).


# Estructura de la aplicación
- Un div general llamado **div.views**
    - Es el contenedor de las views específicas de cada página
    - Cada view se carga mediante AJAX
- Necesitamos los ficheros css y js del framework en nuestra aplicación
    - Los css son específicos de la plataforma (ios o android)
    - El html y css puede cambiar en función de la plataforma


## Crear boilerplate

- Descargamos framework7:

````
git clone https://github.com/framework7io/Framework7.git
```

- Creamos el proyecto:
```
cordova create phonegap-fw7-2
```

- Copiamos los ficheros del directorio dist del repositorio de Framework 7 a nuestro proyecto.

- Modifica el código de *form.html* para que los checkbox funcionen:
  - Observa que falta el icono
  - Modifica el código para que cada elemento tenga una estructura similar a la siguiente:
``` 
    <li>
      <label class="label-checkbox item-content">
        <input type="checkbox" name="my-checkbox" value="Movies">
        <div class="item-media">
          <i class="icon icon-form-checkbox"></i>
        </div>
        <div class="item-inner">
          <div class="item-title">Movies</div>
        </div>
      </label>
    </li>
```


## Cambiar el código de IOS a Android
- Seguir uno de los dos tutoriales siguientes:
  - [Migración de aplicación IOS a Android](http://framework7.io/tutorials/tips-to-migrate-ios-theme-app-to-material-theme.html)
  - [Mantener IOS y Android en una única aplicación](http://framework7.io/tutorials/maintain-both-ios-and-material-themes-in-single-app.html)

