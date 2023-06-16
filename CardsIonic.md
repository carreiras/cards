# Cards Ionic

## Instalar o Ionic
 - Após instalar o Node.js
```
$ npm i -g @ionic/cli
```


## Configurar Android SDK
```
$ export ANDROID_SDK_ROOT=$HOME/Android/sdk
$ export PATH=$PATH:$ANDROID_SDK_ROOT/tools/bin
$ export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools
$ export PATH=$PATH:$ANDROID_SDK_ROOT/emulator
$ export PATH=$PATH:$ANDROID_SDK_ROOT/build-tools/30.0.3
```

## Criar um novo projeto ionic
```
$ ionic start

Every great app needs a name! 😍

Please enter the full name of your app. You can change this at any time.
To bypass this prompt next time, supply name,
the first argument to ionic start.

? Project name: █
```

## Configurar o projeto para o Android
- Adicione o caminho de instalação do Android Studio no arquivo .bashrc
```
export CAPACITOR_ANDROID_STUDIO_PATH="/home/{nome-user}/android-studio/bin/studio.sh"
```

- Execute  uma compilação Ionic
```
$ ionic build
```

- Gere um projeto nativo
```
$ ionic capacitor add android
```

## Definir o ID do pacote
- Abra o arquivo capacitor.config.ts e altere a propriedade appId

```
import { CapacitorConfig } from '@capacitor/cli';

const config: CapacitorConfig = {
  appId: 'com.firstApp',
  appName: 'First App',
  webDir: 'www',
  server: {
    androidScheme: 'https'
  }
};

export default config;
```

## Executar o projeto no Android Studio
- Desenvolva o aplicativo Ionic e sincronize-o com o projeto nativo.

```
$ ionic capacitor copy android
```

- Execute o aplicativo em um simulador ou dispositivo.
```
$ ionic capacitor open android
```

## Inspecionar projeto sendo excutado no Android Studio
- Abra Google Chrome e digite a url
```
chrome://inspect/#devices
```

## Executar projeto no Android Studio com Live Reload
```
$ ionic capacitor run android -l --hot=YOUR_IP_ADDRESS
```

