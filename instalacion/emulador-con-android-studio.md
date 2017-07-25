## Instalación de Android Studio

* Seguimos las [instrucciones de instalación](https://developer.android.com/studio/install.html) seleccionando nuestro sistema operativo.

## Instalación de Java
```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

## Instalación de Graddle

```
sudo apt-get update
sudo apt-get install gradle
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

##  Añadir plataforma

- Después de la @ (opcional) va la versión. Con la 6.1.2 (por defecto) da un error.
```
phonegap platform add android@latest # 6.3.1 with default... error!
```

### Test de funcionamiento
- Necesitamos un AVD (Android Virtual Device) disponible con [API no superior a 25](https://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html#requirements-and-support)

- Para añadir el dispositivo se puede hacer desde Android Studio - Tools

- Posteriormente ejecutamos nuestro proyecto.
  ```
  phonegap run android
  ```
  

## Compilación

- Generar el apk por nuestra cuenta
```
phongap build android
```

- Mediante la nube de Adobe

