# localizame
Demo App Introducción a la programación de Apps con Phonegap 
Introducción a la programación de aplicaciones móviles con el framework Phonegap.

Fundamentos del taller:

El economista Frank Levy propone en su trabajo “How Technology Changes Demands for Human Skills”, y que ya había adelantado junto a otro economista, Richard Murnane, en su libro “The New Division of Labor: How Computers Are Creating the Next Job Market”, el siglo XXI requerirá trabajadores que no solo sean capaces de realizar labores rutinarias que demandan habilidades cognitivas, sino que además tendrán gran énfasis en desarrollar el pensamiento experto y ser capaz de realizar comunicaciones complejas. Todo esto impulsado en general por el desarrollo de sofisticadas tecnologías de la información y la comunicación, o dicho de otro modo, por el crecimiento explosivo de las tecnologías digitales, las cuales están impulsando nuevas dimensiones económicas, donde la tecnología digital y la innovación se transforman en valores agregados de todo los trabajadores.

Los objetivos son:

Conocer el concepto de aplicación móvil híbrida.
Identificar el framework para desarrollo móvil Phonegap/Cordova.
Conocer las herramientas para el desarrollo móvil JavaScript, HTML5 y CSS3.
Conocer el formato JSON para intercambio de datos.
Conocer el lenguaje php y MySql.
Conocer las APIs de Google Maps. 
Crear una App que me localice y carge lugares específicos cerca de mi posición.
Publicar una App en Google Play y Phonegap Build.
Valorar el potencial creativo y profesional de la programación de Apps con Phonegap/Cordova en el ámbito educativo y profesional.

Descripción de los módulos:

Clase 1: 

a) Introducción a la programación de Apps con Phonegap/Cordova, visión general.

Clase 2: 

a) Identificar el framework Phonegap/Cordova y sus componentes para windows.
b) Elementos del framework Phonegap/Cordova.
c) Instalar node.js, npm, apache-ant, android-sdk y phonegap.
d) Comandos básicos de Phonegap.

Clase 3:

a) Crear una base de datos con MySql en un hosting disponible para almacenar lugares con latitud y longitud.
b) Crear un script con php para convertir estos datos en un JSON.
c) Generar la Key de la API de Google Maps.

Clase 4:

a) Crear la app "Localízame" con Phonegap.
b) Incluir las librerías de JQuery y jQuery Mobile.
c) Poner los scripts que permiten localizar.
d) Configurar la localización y sus marcadores.
e) Instalar los plugins necesarios: Geolocation.

Clase 5:

a) Compilar y ejecutar la App.
b) Utilizar Ripple en Google Chrome para emular la App y depurar.
c) Utilizar Device con Android para probar la App.
d) Generar el Keystore y Firmar la App.
e) Subir la App a Phonegap Build o Google Play.
f) Distribuir nuestra App. 

Clase 6:

a) Compilar y ejecutar la App para iOS.
b) Utilizar safari y el emulador de iOS para depurar.
c) Utilizar Device con iOS para probar la App.
d) Generar el certificado iOS para publicarla en Apple Store.
f) Distribuir nuestra App.

Evaluación:

a) Publicación de la App.


Secuencia de actividades:

1. Descarga e instala Nodejs
2. Descarga e instala Android-SDK, es importante instalar la api 19, te pedira
3. Con npm desde línea de comando, instala Phonegap/Cordova:

node

4. Verifica instalación:

phonegap/cordova  -v

5. Creamos el proyecto:

phonegap/cordova create localizame --template jquery-mobile-starter --id com.tecnofran.localizameapp --name localizameapp && cd localizame

*Lo que hace este comando es crea la carpeta o directorio "localizame", luego descarga el template "jquery-mobile-starter", y le asignamos el id "com.tecnofran.localizameapp" y le damos el nombre "localizameapp". Finalmente, ingresamos al directorio "cd localizame".

Puedes listar los template con:

phonegap template list

6. Una vez creado debes agregar la plataforma de Android:

phonegap platform add android

*Puedes listar las plataformas con:
cordova platform remove platform-name

phonegap platform list

*Puedas quitarla con:


7. el plugin Geolocation, necesario para nuestro proyecto:

cordova plugin add cordova-plugin-geolocation

*Este plugin permitirá utilizar el GPS del Smartphone.

*Los plugins instalados pueden listarse:
cordova plugin list

*Para quitarlo:
cordova plugin remove plugin-name

8. Probamos nuestra app en el navegador, Chrome:

*Agregamos la plataforma:
cordova platform add browser

*Ejecutamos:
cordova run browser

9. Habilitamos las opciones de desarrollador en nuestro Smarthone con Android y activamos la opción Depuración de USB. No olvidemosconectar el Smartphone via cable al PC.

10. Habilitamos el Device con el comando:

adb devices

11. Ejecutamos el comando para que nuestra app se instale en el Smartphone.

cordova run android
