Misión: Realizar un "Rebranding" completo de RustDesk a Ultron Desk e inyectar datos de conexión persistentes.

1. Cambio de Identidad Visual (Iconos y Logos)
"Antigravity, localiza y reemplaza los siguientes archivos de imagen por mis logos de Ultron Desk. Mantén las dimensiones originales para evitar errores de compilación:

hay una opcion que es Acerca de 
quiero que remplaces el sitio web por:

https://ultrondesk.com/

Windows: Reemplaza todos los archivos .ico y .png en la carpeta res/ (especialmente logo.ico).

Android: En flutter/android/app/src/main/res/, busca las carpetas mipmap-* y reemplaza ic_launcher.png con mi logo.

Interfaz (UI): Busca en la carpeta flutter/assets/ los archivos logo.svg o logo.png y sustitúyelos."

2. Cambio de Textos Visibles
"Busca en todo el proyecto la cadena de texto 'RustDesk' (sensible a mayúsculas) y reemplázala por 'UltronDesk' en los siguientes archivos críticos:

Cargo.toml (Name y Description).

flutter/pubspec.yaml (Name).

flutter/lib/common.dart o archivos de traducción .arb / .json en flutter/assets/l10n/."



3. Preconfiguración de Servidor y Key (Hardcoded)
"Para que el cliente apunte a mi servidor de Ultron automáticamente tras la instalación, modifica las constantes en src/common.rs (o el archivo equivalente de configuración de red):

IDs_server: 209.46.127.76

relay_server: 209.46.127.76

key: 8EV6xMXSpa5r1klj2jKkqysICIJwFYHMhafTaA0G5qo=

Propiedad: Asegúrate de que estas opciones queden bloqueadas o como predeterminadas para que el usuario no tenga que escribirlas."

4. Preparación para Compilación en GitHub Actions
"Configura o modifica el archivo .github/workflows/build.yml para que:

Utilice los runners de Windows-latest y Ubuntu-latest (para Android).

El nombre del artefacto de salida sea UltronDesk_Windows.exe y UltronDesk_Android.apk.

Ejecuta el Push al repositorio para que GitHub Actions inicie la compilación de inmediato."

las imagenes y logos las deje en el proyecto como branding puedes utilizarlas para los dos clientes el de windows y android