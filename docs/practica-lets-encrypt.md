# IAW - Práctica: HTTPS con Let’s Encrypt y Certbot

- Creamos una instancia en Amazon EC2.

- Realizamos la instalación y configuración de la web. En este caso un Wordpress instalado mediante la herramienta wp-cli.

- Nos creamos una cuenta en Freenom y registramos un nombre de dominio. (iaw-practica-https.tk)

- Configurar los registros DNS del proveedor de nombres de dominio para que el nombre de dominio de ha registrado pueda resolver hacia la dirección IP pública de su instancia EC2 de AWS. 

![](https://github.com/desigom/PRACTICA-HTTPS-CON-LETS-ENCRYPT-Y-CERTBOT/blob/main/DNS-dominio.png)

- Instalamos y configuramos el cliente ACME Certbot en su instacia EC2 de AWS, siguiendo los pasos de la documentación oficial.

