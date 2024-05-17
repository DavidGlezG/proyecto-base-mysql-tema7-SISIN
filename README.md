# Práctica del Tema 7 - EXPLOTACIÓN DE APLICACIONES INFORMÁTICAS

**Autor** : David González García

1. Instalamos mysql-server en el servidor virtual (`sudo apt install mysql-server`).

2. Necesitamos un servicio/servidor web : Apache o Nginx (`sudo apt install -y nginx` o `sudo apt install -y apache2`).

3. Diferenciamos entre el FRONTEND y el BACKEND de la página web.
    Front end y back end son términos amplios que agrupan de forma lógica las diferentes tecnologías y capas de software de cualquier aplicación. El front end se centra en los aspectos que los usuarios pueden ver. Por el contrario, el back end es todo lo que hace que la aplicación funcione. 
En nuestro caso para el frontend utilizamos javascript y para el backend utlizamos php.


4. Instalar los binarios de PHP y el driver mysqli que nos facilita la conexión con la BBDD (`sudo apt-get install php php-mysqli`).

5. Tratar la petición desde el Front al Back: API de tipo RESTful (`sudo apt-get install php7.0-fpm`)
