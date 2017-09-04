# Instalación y configuración de node.js



## Gestor de versiones

* Es habitual utilizar varias versiones de node en nuestra máquina de desarrollo o por cada usuario.
* Esto nos permitirá:

  * Poder cambiar de versión de node de forma transparente
  * Evitar tener que hacer sudo cuando instalemos paquetes de forma global
    * Los paquetes globales se instalan para un único usuario y version de node
    * Los paquetes globales sirven para cualquier proyecto



* Los gestores de versiones más habituales son:

  * [nvm](https://github.com/creationix/nvm) para Linux/Mac
  * [nvm-windows](https://github.com/coreybutler/nvm-windows) para Windows


## Instalación de nvm en Linux

* Instalaremos y utilizaremos node vía nvm \(node virtual manager\)

  ```
  curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.1/install.sh | bash
  ```

  * Instalar una versión de node:

    ```
    nvm install 6
    ```

  * Ver las versiones que hay instaladas:

    ```
    nvm ls
    ```

  * Usar una versión en particular:

    ```
    nvm use 6
    ```

  * Usar una versión en particular siempre que abrimos un shell:

    ```
    nvm alias default 6
    ```


## Instalación de node

* Si hemos utilizado un gestor de versiones de node, ya habremos instalado node.
* Instalación en Linux: 

```
sudo curl -sL https://deb.nodesource.com/setup_6.x | bash -
sudo apt-get install -y nodejs
sudo apt-get install build-essential
```


* En Windows [descargando el paquete msi](https://nodejs.org/es/)

* Comprobamos que esté instalado:
  * Desde Windows tendremos que sacar la consola mediante el comando cmd
  * Posteriormente en Windows utilizaremos la propia consola del editor de código

```
npm -v
node -v
```


## Actualización de npm
- La versión de npm que viene con el propio node no es la excesivamente actual y da problemas con algunos plugins de PhoneGap
- Se recomienda actualizar mediante el comando:
  ```
  npm install -g npm
  ```







