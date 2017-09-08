# Hello World


## Hello World mediante template desde Phonegap

- Creamos una aplicación de ejemplo:
    - Por defecto usa el template de helloWorld
    - Ejecutar comando *phonegap template list*

    ```
    $ phonegap create helloWorld
    $ cd helloWorld
    ```
    - Accede a la aplicación desde el navegador
    - Ahora "sirve" la aplicación mediante el CLI de Phonegap:

    ```
    $ phonegap serve
    ```

        - Accede a la aplicación desde el navegador del PC
        - Accede a la aplicación desde PhoneGap Developer
        - Si el teléfono y el PC no están en la misma red se puede añadir el parámetro *--localtunnel*

    - Comprueba la diferencia entre ambas ejecuciones.
    - En el segundo caso los plugins están "funcionando". Pare el caso del navegador se instala una *browser platform* que simula el comportamiento de los plugins.
    
## Hello Word desde PhoneGap Desktop

- Se pulsa en el botón + para añadir un nuevo proyecto 
- Se elige el template
- Se lanza o se para desde la ventana gráfica

## Hello Word utilizando Cordova
- Similar al CLI para Phonegap
- No instala los plugins que sí instala Cordova y no son necesarios (mejor)
- No instala la plataforma browser por defecto (hay que hacerlo a mano)
- Si accedemos desde el navegador, habrá que poner la ruta
- No funcionará con PhoneGap Developer

