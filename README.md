# proyecto-flipper

Repositorio para aprender a desarrollar con Flutter. La app (`bill_manager`) vive en la carpeta [`bill_manager/`](bill_manager).

## Requisitos

- [Flutter SDK](https://docs.flutter.dev/get-started/install) (canal stable). Dart SDK `^3.13.4`, incluido con Flutter.
- VS Code con las extensiones **Flutter** y **Dart** (`Dart-Code.flutter`).
- Chrome, para correr la app en web sin configurar nada más.

Para correr en móvil además necesitas:

- **Android:** Android Studio (SDK y un emulador) y `flutter doctor --android-licenses`.
- **iOS (solo macOS):** Xcode completo y CocoaPods (`brew install cocoapods`).

Verifica tu entorno con:

```bash
flutter doctor
```

## Cómo levantar el proyecto

Todos los comandos se ejecutan dentro de `bill_manager/`.

```bash
git clone https://github.com/MaxRetana/proyecto-flipper.git
cd proyecto-flipper/bill_manager

flutter pub get          # instala las dependencias
flutter devices          # lista los dispositivos disponibles
flutter run -d chrome    # corre la app en el navegador
```

Para correr en otra plataforma cambia el dispositivo: `flutter run -d macos`, o el id de un emulador o dispositivo que aparezca en `flutter devices`.

Desde VS Code: abre la carpeta `bill_manager`, elige el dispositivo en la barra inferior y pulsa `F5`.

### Hot reload

Con la app corriendo en la terminal:

- `r`: hot reload (aplica los cambios sin perder el estado).
- `R`: hot restart.
- `q`: salir.

## Calidad del código

```bash
flutter analyze   # análisis estático
flutter test      # pruebas
```

## Flujo de trabajo

- Los cambios se hacen en una rama creada desde `develop` (por ejemplo `6-task-levantar-el-proyecto-de-flutter`) y se integran con un Pull Request hacia `develop`.
- Los issues y PR usan las plantillas de `.github/`.
- Los mensajes de commit se escriben en español, con formato `tipo(ámbito): descripción`.
