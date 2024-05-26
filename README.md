# Extractor de rutas con MONGODB

Objetivo:
Realizaremos 2 servicios orquestados:
1.  Crearemos una base de datos en Mongo DB que estará formada de 2 tablas: Una tabla con un diccionario y otra tabla que almacenará todos los resultados.

2. Por otra parte crearemos un servidor WEB con Python usando Flask. En este se le pedirá al usuario un input para que introduzca la URL de la web que desee. Una vez lo haga se hará un discovery de la misma buscando todas las rutas que tenga existentes usando el diccionario que tenemos en la tabla del primer servicio. Los resultados que se generen de esta busqueda se almacenarán en la tabla de resultados que también hemos creado previamente.

Nos harán falta los siguientes directorios y componentes:
**mongo**
 - **Dockerfile** para la creación de las bases de datos

**aplicacion_web**
 - Carpeta de **templates** el html del buscador
 - Carpeta de **wordlist** con nuestro diccionario de rutas
 - **App.py** este tendrá toda la lógica del servidor web y la extracción de rutas
 - **Dockerfile** para el servidor WEB

Por último utilizaremos Docker Compose para orquestar ambos servicios.
