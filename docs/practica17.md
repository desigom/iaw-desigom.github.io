# Balanceo de carga con HAProxy

- Creamos una instacia nueva en Amazon EC2.

- Utilizamos los archivos de la práctica 16.

- Modificamos el archivo docker-compose.yml y añadimos las siguientes líneas:

          lb:
            image: dockercloud/haproxy
            ports:
              - 80:80
              - 1936:1936
            links:
              - apache
            volumes:
              - /var/run/docker.sock:/var/run/docker.sock
            networks:
              - frontend-network

- Guardamos los cambios y ejecutamos un docker-compose up --scale apache=4

- Accedemos a la IP pública de la instancia y comprobamos la instalación.

- Accedmos a la IP-publica:1936, pedirá usuario y contraseña (stats-stats). Veremos estadisticas sobre el balanceador de carga con HAProxy.
