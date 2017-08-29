# Instalación y configuración del editor de código

## Instalación
* Utilizaremos [Visual Code Editor](https://code.visualstudio.com/)
* Es un producto open source de Microsoft realizado mediante node.js (electron)
* Uso muy similar a Sublime Text (empezando con la paleta de comandos CTRL + ALT + P)
* Tiene un excepcional debugger para node.js

## Extensiones
* Se pueden ver desde el propio software o desde https://marketplace.visualstudio.com
* Emmet ya viene preinstalado
* Para hacer un preview en el browser por ejemplo instalaremos **open in browser**
    - Hace falta recargar
    - Mediante CTRL+K D se realiza un preview en el navegador por defecto
    - Mediante CTRL+ALT+O se elige
    - Las instrucciones de uso aparecen en Visual Code Editor una vez instalado el plugin
* Para autocompletar ficheros utilizaremos **path autocomplete**
    - Mediante CONTROL + ESPACIO podemos lanzarlo
    - Prueba con un fichero css (para insertar el fichero utiliza la abreviatura de emmet link)


## html
* El código **seleccionado** se formatea mediante CTRL+ K y CTRL + F
* Cambiar la configuración por defecto
    * Mediante los settings (específicos por lenguaje)
    * User Settings para nuestras modificaciones
* Linter para html con la extensión HTMLHint
    * Necesitamos instalar el [paquete de node.js HTMLHint](https://www.npmjs.com/package/htmlhint)
* Intellisense:
     - Por defecto nos da sugerencias (ej. teclea < y pulsa CTRL + espacio)
     - Puede ser útil que nos de sugerendias respecto a clases de CSS que queremos utilizar:
         - [IntelliSense for CSS class names](https://marketplace.visualstudio.com/items?itemName=Zignd.html-css-class-completion)
         - [HTML CSS Support](https://marketplace.visualstudio.com/items?itemName=ecmel.vscode-html-css)
         
         
## Linter para JavaScript
- Utilizaremos eslint (el más habitual)
- Instalaremos la extensión eslint dentro de Visual Code Editor
- Utilizaremos eslint como dependencia de desarrollo dentro de nuestros proyectos













