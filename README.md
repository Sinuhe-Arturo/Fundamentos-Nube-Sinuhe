#Fundamentos-Nube-Sinuhe
repositorio de tareas de la materia  fundamentos de la nube de Sinuhe Arturo Evia Campos
----------------CARPETA "DB" DESCRIPCIÓN DE "docker-compose.yml"-----------------------------
*Comandos y descripcion*
"version: 3.1"
(Es la version actual del programa docker que permite utilizar la Contenedor de Maria DB que se creo para ser utilizada
en la nube desde el computador.)

"mydatabases"
(este es el nombre asignado actualmente para la base de datos que se utilizó para lla demostracion del uso de Docker)

"image: MariaDB"
(esta linea de codigo representa la imagen ISO que se utiliza para instalar la aplicacion MariaDB, en caso de seleccionar
una version enn especifico se colocan los dos puntos y se selecciona la version deseada de forma manual. en caso de no seleccionar alguno
se instala una version mas reciente.)

"restart:always"
(en caso de que el contenedor tenga una caida, este comando reinicia de forma inmediata el
contedor)

"enviroment:"
(genera el entorno virtual de la base de datos permitiendo utilizar la funcionalidad de la aplicacion
sin necesidad de instalarse.)

"MYSQL_ROOT_PASSWORD: Megamanx1"
(se asigna la contraseña al super usuario)

"MYSQL_DATABASE: mydbclass"
(este es el nombre de la base de datos)

"MYSQL_USER: mydbuser"
(el nombre del usuario que utilizara la base de datos sin priviligios especiales)

"MYSQL_PASSWORD: Absa"
(contaseña de usuario normal sin privilegios espciales)

"ports:"
      - 3889:3306

(son los puertos que se van a utilizar para conectar la base de datos en linea. el numero de la derecha significa el dominio default
y el segundo se refiere al puerto que el usuario desea conectarse.)