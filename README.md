KSM PARA WEBOS 3.x.x

Para el entorno de desarrollo es necesario descargarse el SDK de LG de la página developer.lge.com.
El usuario y la contraseña me los pueden pedir a mi o a Víctor.

Aquí se puede encontrar la informacíon necesaria para debuguear.
http://webossignage.developer.lge.com/develop/development-process/debugging-your-app/

Recomiendo usar el 'ares-setup-device' para agregar el dispositivo en el que se va a trabajar con el nombre de 'tv' y el emulador con el nombre de 'emu' para poder usar todos
los scripts de desarrollo creados en node. (Es necesario agregar ares como variable de entorno)

http://webossignage.developer.lge.com/sdk/tools/cli/?wos_flag=ares-setup-device#ares-setup-device

    npm run build (cambia todos los nombres necesarios de los archivos y corre las funciones de ares para crear el ipk de producción).
    
    npm run build-emulator(cambia los nombres, hace el ipk de dev, lo instala en el emulador y abre la ventana del navegador para debug).
    
Hay más scripts que pueden ver en el archivo package.json en el root del repo. Los tests no están activos.

El script.js del Player sirve como interfaz para llamar a los diferentes servicios de node que viven en Daemon. Toda la lógica de las funciones está separada en sus respectivos módulos
helper.js y mercury.js

En el case de Daemon es más o menos lo mismo, daemon.js es la interfaz a través de la cual se llama a los diferentes servicios que manejan las lógicas. helpers.js y mercury.js


La versión de SCAP que utilizamos para esta versión es 1.5:
http://webossignage.developer.lge.com/api/scap-api/scap15/