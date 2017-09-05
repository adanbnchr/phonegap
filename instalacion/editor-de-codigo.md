# Editor de código


## Instalación
* Utilizaremos [Visual Code Editor](https://code.visualstudio.com/)
* Es un producto open source de Microsoft realizado mediante node.js (electron)
* Uso muy similar a Sublime Text (empezando con la paleta de comandos CTRL + ALT + P)
* Tiene un debugger para node.js muy bueno.


## Extensiones
* Se pueden ver desde el propio software o desde https://marketplace.visualstudio.com
* Emmet ya viene preinstalado
* Instalaremos por ej. live server
    - Hace falta recargar
    - Detecta cambios en vivo    
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
     - Si no utilizamos angular o ionic por ej, puede ser útil quitarlo del intellisense. Yo particularmente también uso dos espacios para la tabulación en vez de 4:

    ```
         {
    "html.suggest.angular1": false,
    "html.suggest.ionic": false,
    "editor.tabSize": 2
    }
    ```
     
     - Puede ser útil que nos de sugerendias respecto a clases de CSS que queremos utilizar:
         - [IntelliSense for CSS class names](https://marketplace.visualstudio.com/items?itemName=Zignd.html-css-class-completion)
         - [HTML CSS Support](https://marketplace.visualstudio.com/items?itemName=ecmel.vscode-html-css)
             - Instalaremos HTML CSS Support
             - Comprueba su funcionamiento, mira si al rellenar el atributo class de algún elemento el editor te da sugerencias (pulsando CTRL+espacio)
                 - Fichero css de prueba, por ejemplo *styles/main.css*:
                 ```
                 .rojo {
                    color: red;
                }
                .azul {
                    color: blue;
                }
                .importante {
                    font-weight: bold;
                }
                ```
                - Fichero html:
                
                    ```
                    <!DOCTYPE html>
                    <html lang="en">
                    <head>
                        <meta charset="UTF-8">
                        <meta name="viewport" content="width=device-width, initial-scale=1.0">
                        <meta http-equiv="X-UA-Compatible" content="ie=edge">
                        <title>Document</title>
                        <link rel="stylesheet" href="styles/main.css">
                    </head>
                    <body>
                        <p class="">Prueba</p>
                    </body>
                    </html>
                    ```
                
         
## Linter para css
- En principio Visual Code Editor ya lleva un linter por defecto :-)

## Linter para JavaScript
- Utilizaremos eslint (el más habitual)
- Instalaremos la extensión eslint dentro de Visual Code Editor
- Además de la extensión es necesario instalar un ejecutable en node:
    ```
    npm install -g eslint
    ```
- Utilizaremos eslint como dependencia de desarrollo dentro de nuestros proyectos
- Abriremos la paleta de comandos (CTRL + MAYS + P) y elegiremos *Create a .eslintrc.json file*













