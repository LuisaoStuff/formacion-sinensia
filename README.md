# Tareas Sinensia

Esto es un repositorio comprobante de las tareas realizadas durante el programa de formaión [DevOps](https://es.wikipedia.org/wiki/DevOps) de [Sinensia](https://www.sinensia.com)

## A mejorar

En el [Dockerfile](php-fpm-OneContainer/Dockerfile) del contenedor de **php-fpm** + **nginx** hay un fallo al lanzar el contenedor. El problema es que no se inicializa automáticamente el servicio de **php-fpm7**. He probado a poner un `CMD php-fpm7`, pero de esta forma no arranca la máquina, por lo que tengo que ejecutar manualmente `docker exec -it prueba-fpm /usr/sbin/php-fpm7`
