# Cards Ionic

## Configurar Android SDK no Linux

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

### Para Capacitor

- Execute  uma compilação Ionic

```
$ ionic build

```

- Gere um projeto nativo
```
$ ionic capacitor add android

```

## Defina o ID do pacote

### Para Capacitor

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
