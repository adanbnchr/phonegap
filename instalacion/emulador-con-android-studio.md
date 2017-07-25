## Instalación de Android Studio

* Seguimos las [instrucciones de instalación](https://developer.android.com/studio/install.html) seleccionando nuestro sistema operativo.

## Instalación de Java
```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

### Variables de Shell

* Fichero _$HOME/.zshrc_ para el **shell zsh**:

  ```
  export ANDROID_HOME='/home/usuario/Android/Sdk'
  path+=('/home/usuario/Android/Sdk/tools' '/home/usuario/Android/Sdk/platform-tools')
  ```

* Añado también el repositorio de los binarios de npm \(lo utiliza Sublime Text y al usar zsh hay que dárselo\). Fichero _$HOME/.zshenv:_

  ```
  path+=('/home/usuario/.nvm/versions/node/v5.0.0/bin/')
  ```

### Test de funcionamiento

* Cierra y vuelve a abrir el shell
* Ejecuta un comando como _android avd_

## 
```
phonegap platform add android
phonegap run android
```




