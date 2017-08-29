# JavaScript en servidor

![](assets/node.png)


## Qué es nodejs

- NodeJS es un intérprete de JavaScript que se ejecuta en servidor.
- Está basado en el motor de  JavaScript que utiliza Google Chrome (V8), escrito en C++


## Características principales
- Tener el mismo lenguaje en cliente y servidor
  - Permite a cualquier persona desarrollar en backend o en frontend
  - Permite reusar código o incluso mover código de cliente a servidor o al revés

- Está orientado a eventos y utiliza un modelo asíncrono (propio de JavaScript).


- Al contrario que en el navegador, encontramos muchas llamadas asíncronas: 
    - Llamadas a APIs
    - Lectura y escritura de ficheros
    - Ejecución de cálculos en el servidor
    - ....


- Llamadas síncronas en servidor serían fatales:
    - ¡Bloqueariamos las conexiones al servidor hasta que acabase la instrucción bloqueante!
    - Al ser asíncrono podremos tener muchas sesiones concurrentes


- Es monohilo
   - Utiliza un solo procesador
   - Si queremos usar toda la potencia de la CPU, tendremos que levantar varias instancias de node y utilizar un balanceador de carga ([por ejemplo con pm2](https://github.com/Unitech/pm2))

{% youtube src="https://www.youtube.com/watch?v=9nPdNyMbpSk" %}{% endyoutube %}

Ver la parte interesante del video: mínuto 14:47


## Desventajas
- Trabajar con código asíncrono hace que a veces el código no sea excesivamente legible
- Imagina que guardamos un registro de los accesos de los usuarios a nuestra app:

```
trackUser =  function(userId) {
  users.findOne({userId: userId}, function(err, user) {
    var logIn = {userName: user.name, when: new Date};
    logIns.insert(logIn, function(err, done) {
      console.log('wrote log-in!');
      });
  });
```

- Tenemos 3 funciones anidadas en una simple operación.
- Esto es lo que se conoce como [callback hell](https://strongloop.com/strongblog/node-js-callback-hell-promises-generators/)


## Evitar el callback en el navegador
- Mediante el [uso de promesas](https://www.promisejs.org/)
- Se trata de escribir código asíncrono con un estilo síncrono.
- Opciones más actuales:
    - Generators / Yields (ES6)
    - Async / Await (ES8)

- Ver [comparativa de métodos asíncronos](https://thomashunter.name/blog/the-long-road-to-asyncawait-in-javascript/)
- Ver [Async / Await](http://rossboucher.com/await/#/1)


## Compatiblidad node con ES6 y más allá

- [El soporte de ES6 en node es limitado](http://node.green/)
  - Se pude añadir el flag --harmony
  - Se puede utilizar un transpiler, que genere código compatible. El más habitual es [babel](https://babeljs.io/)
- En el navegador tenemos el mismo problema (mismo motor...): es práctica extendida el uso de transpilers.
  

## Hola Mundo en node
- Editamos un fichero en JavaScript, *holaMundo.js*:
  ```
  console.log ("Hola Mundo");
  
  ```
- Lo ejecutamos mediante *node holaMundo.js*
- Si escribimos *node* sin más, podemos acceder a la consola de node, un intérprete de JavaScript, igual que el que tenemos en el navegador


## npm
- Es el gestor de paquetes de node
- Propongo hacer dos prácticas para coger la dinámica del uso de npm y sus librerías y de trabajar con node: 
  - Crear una librería en node.js
  - Crear una api rest mediante node.js