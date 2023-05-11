# Conexión a MongoDB
Conexión a MongoDB desde NodeJS con Mongoose.

1- Crear una carpeta (ejemplo: backend_mongodb) en el directorio de su preferencia.

2- Abrir la terminal de Visual Studio Code y ejecutar estando posicionado dentro de la carpeta (backend_mongodb) el comando npm init --yes, al haber previamente instalado en la computadora el entorno Node.js. Una vez ejecutado este comando se genera en la carpeta el archivo package.json.

3- Instalar la dependencia dotenv al ejecutar el comando npm install dotenv, para poder utilizar las variables de entorno. Una vez instalado vamos a tener dentro de la carpeta en la que estamos posicionados el archivo package-lock.json y la carpeta node_modules.

4- Procedemos ahora a instalar el framework express escribiendo en la terminal de Visual Studio Code npm install express. Express provee toda la funcionalidad que se necesita para hacer aplicaciones web, proporcionando mecanismos para escritura de manejadores de peticiones con diferentes verbos HTTP en diferentes caminos URL (rutas), integración con motores de renderización de “vistas” para generar respuestas mediante la introducción de datos en plantillas, establecer ajustes de aplicaciones web como qué puerto usar para conectar, la localización de las plantillas que se utilizan para renderizar la respuesta y añadir procesamiento de peticiones “middleware” adicional en cualquier punto dentro de la tubería de manejo de la petición.

5- Instalamos mongoose (dependencia que nos permitirá conectarnos con mongodb). Mongoose es una librería para Node.js que nos permite escribir consultas para una base de datos de MongooDB, con características como validaciones, construcción de queries, middlewares, conversión de tipos y algunas otras, que enriquecen la funcionalidad de la base de datos.

6- Creamos un nuevo archivo app.js (ver el código especificado dentro del mismo). En él importamos las dependencias que vamos a utilizar y nos conectamos a MongoDB utilizando la variable de entorno MONGO_URI_TEST.

7- Abrimos en el navegador la pagina de MongoDB, iniciamos sesión o nos registramos en caso de no tener una cuenta.

8- En la página de MongoDB creamos una implementacion de base de datos (Database Deployments) siguiendo todos los pasos que se muestran en la pestaña del navegador y una vez configurada le damos al botón "Finish and Close". 

9- Seleccionamos el botón "Connect" del cluster que previamente creamos y escogemos la primera opción (Drivers). Seleccionamos el driver (Node.js) y la versión (4.1 or later). Si la versión del driver no nos permite conectarnos seleccionamos una versión previa. 

10- Copiamos el string de conexión al código de nuestra aplicación, creando un archivo .env en la carpeta en donde estamos posicionados en Visual Studio Code e igualando el nombre MONGO_URI_TEST al string previamente copiado, reemplazando '<password>' por la contraseña que habíamos definido para nuestro usuario.
  
11- Importamos los modulos en otro archivo, para ello creamos en la carpeta actual el archivo index.js con las líneas de código especificadas.
  
12- En la terminal de Visual Studio Code ejecutamos el comando npm install nodemon para que cada vez que el usuario quiera guardar algo en la base de datos esta se actualice automáticamente.
  
13- En el archivo package.json en el objeto "scripts" agregamos el atributo "start":"nodemon index.js".
  
14- Corremos el servidor en la terminal de Visual Studio Code con el comando npm run start y verificamos en la página web de MongoDB que nos hayamos conectado a la base de datos.
