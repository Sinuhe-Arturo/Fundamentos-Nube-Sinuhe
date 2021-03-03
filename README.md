#Fundamentos-Nube-Sinuhe
repositorio de tareas de la materia fundamentos de la nube de Sinuhe Arturo Evia Campos
----------------CARPETA "DB" DESCRIPCIÓN DE "docker-compose.yml"-----------------------------
*Comandos y descripción*
"versión: 3.1"
(Es la versión actual del programa Docker que permite utilizar la Contenedor de Maria DB que se creó para ser utilizada
en la nube desde el computador.)

"mydatabases"
(Nombre del contenedor donde esta almacenado la imagen de MariaDB entre otros componentes que son necesarios.)

"image: MariaDB"
(esta linea de código representa la imagen ISO que se utiliza para instalar la aplicación MariaDB, en caso de seleccionar
una versión en específico se colocan los dos puntos y se selecciona la versión deseada de forma manual. en caso de no seleccionar alguno
se instala una versión más reciente.)

"restart:always"
(en caso de que el contenedor tenga una caída, este comando reinicia de forma inmediata el
contendor)

"enviroment:"
(genera el entorno virtual de la base de datos permitiendo utilizar la funcionalidad de la aplicación
sin necesidad de instalarse.)

"MYSQL_ROOT_PASSWORD: Megamanx1"
(se asigna la contraseña al super usuario)

"MYSQL_DATABASE: mydbclass"
(este es el nombre de la base de datos)

"MYSQL_USER: mydbuser"
(el nombre del usuario que utilizara la base de datos sin privilegios especiales)

"MYSQL_PASSWORD: Absa"
(contraseña de usuario normal sin privilegios espaciales)

"ports:"
      - 3889:3306

(son los puertos que se van a utilizar para conectar la base de datos en linea. el numero de la derecha significa el dominio default
y el segundo se refiere al puerto que el usuario desea conectarse.)

- ./files:/var/lib/mysql
- ./logs:/var/log/mysql
- ./conf:/etc/mysql/conf.d
(estas líneas nos indican donde será guardado desde la pc hasta el lugar deseado)
---------------------------Docker-compose web----------------
"version: '3.1'"
(Versión de la aplicación Docker que se encuentra actualmente)

"services:"
servicio que se genera al momento de empezar la aplicación

"measurementapp:"
(Nombre del contenedor que tiene la imagen de la aplicación)

"image: webdevops/php-apache:7.4"
(imagen de la aplicación apache, en esta opción utilizamos una selección de versión)
"restart: always"
(en caso de que el contenedor tenga una caída, este comando reinicia de forma inmediata el
contendor)

"environment:"
(genera el entorno virtual de la base de datos permitiendo utilizar la funcionalidad de la aplicación
sin necesidad de instalarse.)

"PHP_DISPLAY_ERRORS: 1"
(comando que permite visualizar los errores que puedan ocasionarse)
"ports:"
  - 82:80
  (son los puertos que se van a utilizar para conectar la base de datos en linea. el numero de la derecha significa el dominio default
  y el segundo se refiere al puerto que el usuario desea conectarse.)

"volumes:"
 - ./app:/app
 (estas líneas nos indican donde será guardado desde el pc hasta el lugar deseado)
