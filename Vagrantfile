
Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/xenial64"

  config.vm.network "private_network", ip: "192.168.50.55"

  config.vm.synced_folder ".", "/practica_tema7_sisin"

  config.vm.provision "shell", inline: <<-SHELL

      # Instalación de los binarios de PHP, el driver mysqli y la extensión FPM para realizar peticiones de tipo RESTful
      
      #Instalación de mysql server en el servidor virtual
      sudo apt install mysql-server

      #Selecciono el servicio web que quiero usar y lo instalo
      sudo apt update

      sudo apt install -y nginx
      
      #Instalo los binarios de php y el driver de mysqli
      sudo apt-get install php php-mysqli

      #Extensión FPM para realizar peticiones de tipo RESTful
      sudo apt-get install php7.0-fpm

      # Generar archivo SQL con los registros de los diferentes Módulos Profesionales
      echo "-- Insertar datos de ejemplo en la tabla 'horario'" > /home/vagrant/datos_horario.sql
      echo " INSERT INTO gestion_horario.horario (dia, primera, segunda, tercera, cuarta, quinta, sexta) VALUES" >> /home/vagrant/datos_horario.sql
      echo "('Lunes', 'Fol', 'Prog', 'Badat', 'Badat', 'Sisin', 'Sisin')," >> /home/vagrant/datos_horario.sql
      echo "('Martes', 'Sisin', 'Marcas', 'Marcas', 'Endes', 'Prog', 'Fol')," >> /home/vagrant/datos_horario.sql
      echo "('Miércoles', 'Badat', 'Badat', 'Prog', 'Marcas', 'Marcas', 'Fol')," >> /home/vagrant/datos_horario.sql
      echo "('Jueves', 'Badat', 'Leup', 'Leup', 'Prog', 'Prog', 'Sisin')," >> /home/vagrant/datos_horario.sql
      echo "('Viernes', 'Sisin', 'Badat', 'Endes', 'Endes', 'Prog', 'Prog')" >> /home/vagrant/datos_horario.sql



  SHELL

end
