
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
      echo "-- Insertar datos de ejemplo en la tabla 'empleados'" > /home/vagrant/datos_empleados.sql
      echo " INSERT INTO gestion_empleados.empleados (nombre, apellido, edad, salario, departamento) VALUES" >> /home/vagrant/datos_empleados.sql
      echo "('Juan', 'Pérez', 30, 2000.00, 'Ventas')," >> /home/vagrant/datos_empleados.sql
      echo "('Manolo', 'Pérez', 40, 2500.00, 'Ventas')," >> /home/vagrant/datos_empleados.sql
      echo "('Lucía', 'Pérez', 50, 1000.00, 'Ventas')," >> /home/vagrant/datos_empleados.sql
      echo "('Teresa', 'Pérez', 10, 2500.00, 'Marketing')," >> /home/vagrant/datos_empleados.sql
      echo "('Pepito', 'Martínez', 5, 2500.00, 'Ventas')" >> /home/vagrant/datos_empleados.sql


      
  SHELL

end
