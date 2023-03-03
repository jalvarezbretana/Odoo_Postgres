# Entorno de desarrollo Odoo-Postgres
Primero instalamos el postgresSQL en el equipo en caso de ser necesario. Una vez instalado, comprobamos el funcionamiento de los servicios de postgresSQL con el siguiente comando: "sudo netstat -putan | grep post".
En caso de que sea necesario. ejecutamos "service postgresql stop" para detener los servicios activos de postgres.
Creamos un nuevo directorio de trabajo y creamos dentro el archivo 'docker-compose.yml', el cual levantará el nuevo servidor Odoo.

![Captura de pantalla de 2023-03-03 12-37-46](https://user-images.githubusercontent.com/56074194/222717006-a47fb567-9a85-49f9-b09d-b20bc950ae6d.png)



Este archivo consta de dos servicios, uno web (Odoo) y una base de datos (PostgreSQL). Primero se genera la Base de Datos, indicando todos los parámetros necesarios y después se genera el servicio web, con Odoo, enlazándolo con la Base de Datos creada anteriormente, indicando en el servicio web que depende de la database que acabamos de crear.

Al ejecutar el comando para levantar los servicios, se generarán en la carpeta raíz unos directorios nuevos, autogenerados por el propio servicio.

Si se desea comprobar que el sevidor funciona en local podemos entrar desde cualquier navegador al sitio web: http://localhost:8069, siendo el puerto 8069, el puerto indicado en el archivo docker.

Una vez ingreamos los datos necesarios la web debería ser similar a la siguiente:

![Captura de pantalla de 2023-03-03 12-37-25](https://user-images.githubusercontent.com/56074194/222717021-4e48e5db-464f-46ae-ad8a-6119f5263cc7.png)
![Captura de pantalla de 2023-03-03 12-39-47](https://user-images.githubusercontent.com/56074194/222717037-9666f8b6-588a-42b6-8edf-dbd5e5e1a135.png)




Después para sincronizar la Base de Datos a Pycharm vamos al apartado Database y rellenamos los campos:

![Captura de pantalla de 2023-03-03 12-41-34](https://user-images.githubusercontent.com/56074194/222717094-b1ea43df-242c-44b1-aa24-bc07b552fced.png)



Para mostrar la db que se acaba de crear en PyCharm, se accede al menú de configuración de la db postgresql, se accede a 'Schemas' y se selecciona odoo_dam, para que se muestre en la pastaña 'Databases de PyCharm'.
![Captura de pantalla de 2023-03-03 12-42-36](https://user-images.githubusercontent.com/56074194/222717106-55ea799e-84c8-49d9-a420-94167c103da6.png)
![Captura de pantalla de 2023-03-03 12-43-24](https://user-images.githubusercontent.com/56074194/222717118-730f8d17-c9b6-46d9-aad4-0960d097948f.png)
