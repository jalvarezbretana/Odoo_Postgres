Entorno de desarrollo Odoo-Postgres
Primero instalamos el postgresSQL en el equipo en caso de ser necesario. Una vez instalado, comprobamos el funcionamiento de los servicios de postgresSQL con el siguiente comando: "sudo netstat -putan | grep post".
En caso de que sea necesario. ejecutamos "service postgresql stop" para detener los servicios activos de postgres.
Creamos un nuevo directorio de trabajo y creamos dentro el archivo 'docker-compose.yml', el cual levantará el nuevo servidor Odoo.

Este archivo consta de dos servicios, uno web (Odoo) y una base de datos (PostgreSQL). Primero se genera la Base de Datos, indicando todos los parámetros necesarios y después se genera el servicio web, con Odoo, enlazándolo con la Base de Datos creada anteriormente, indicando en el servicio web que depende de la database que acabamos de crear.

Al ejecutar el comando para levantar los servicios, se generarán en la carpeta raíz unos directorios nuevos, autogenerados por el propio servicio.

Si se desea comprobar que el sevidor funciona en local podemos entrar desde cualquier navegador al sitio web: http://localhost:8069, siendo el puerto 8069, el puerto indicado en el archivo docker.

Una vez ingreamos los datos necesarios la web debería ser similar a la siguiente:

Después para sincronizar la Base de Datos a Pycharm vamos al apartado Database y rellenamos los campos:

Para mostrar la db que se acaba de crear en PyCharm, se accede al menú de configuración de la db postgresql, se accede a 'Schemas' y se selecciona odoo_dam, para que se muestre en la pastaña 'Databases de PyCharm'.