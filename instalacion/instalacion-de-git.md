# Git



## ¿Qué es git?
- Es un sistema de control de versiones distribuido
- El control de versiones más utilizado
- Lo utiliza PhoneGap/Cordova para la instalación de sus plugins
- Te recomiendo que leas su [documentación](https://git-scm.com/book/es/v1)


## Instalación de git en Linux

* Instalación de git:

  ```
  sudo apt-get update
  sudo apt-get install git
  ```


## Instalación de git en Windows

- [Descargamos el paquete](https://git-scm.com/download/win) y lo instalamos
- En la instalación se configura de modo que se pueda ejecutar vía git-bash y vía la consola normal de Windows.


### Configuración de git

* Configuración necesaria para cada commit que haga:

  ```
  git config --global user.name "Your Name"
  git config --global user.email "youremail@domain.com"
  ```
* Opcionalmente el editor \(si no me gusta el que hay por defecto\):

  ```
  git config --global core.editor vi
  ```


* Git tiene 3 niveles de configuración, cada nivel sobreescribe el anterior:

  * Para todos los usuarios: _/etc/gitconfig_
  * Para un usuario: _~/.gitconfig_  \(opción --global\)
  * Para un repositorio: _.git/config_ 


* Para ver los parámetros configurados:

```
git config --list
```

* Viene bien tener una [chuleta de comandos de Git](https://services.github.com/kit/downloads/github-git-cheat-sheet.pdf)



### Configuración de GitHub
* En principio lo siguiente está indicado para Linux o Mac. En Windows es más cómodo conectar por https y [utilizar algún caché de credenciales](https://help.github.com/articles/caching-your-github-password-in-git/#platform-windows)
* Nos registramos en [Github](https://github.com/) 


* Accedemos a nuestra cuenta
* Vamos a los settings y asociamos una ssh-key

  * Evitaremos introducir usuario/contraseña en cada _git push_

* Como creamos nuestra ssh-key:

  ```
  ssh-keygen
  ```

* Copiaremos el contenido de _~/.ssh/id\_rsa.pub_ a una nueva clave ssh en GitHub

