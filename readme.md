# Actividad 2.2 Instalación y despliegue on Nginx
___

# 1. Preparación de la MV

# 1.1. Creación de la MV 
![Creación VM](./img/2.png)

# 1.2. Configuración de red
![Quitar configuración anterior](./img/6.png)
![Entrada por ssh](./img/7.png)

# 1.3. Acceso por ssh a la MV
![Acceso por ssh](./img/8.png)

# 2. Preparación del entorno

# 2.1. Instalación Nginx 

![Instalación Nginx](./img/3.png)

# 2.2. Configuración del firewall

![Creación VM](./img/10.png)


# 2.2. Configuración del estado de Nginx

![Estado Nginx](./img/11.png)

# 3.Configuración del blque servidor

# 3.2. Desactivación del sitio por defecto
Se crea un archivo de configuración en **/etc/nginx/sites-available/sitio_ejemplo**

```nginx
server {
    listen 80;
    server_name _;
    root /var/www/sitio_ejemplo;
    index index.html;
    location / {
        try_files $uri $uri/ =404;
    }
}
```


# 3.2. Desactivación del sitio por defecto

![Configuración](./img/12.png)
![Configuración](./img/13.png)

# Resultado Final
![Configuración](./img/14.png)