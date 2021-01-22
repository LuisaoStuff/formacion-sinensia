# Este es mi primer Dockerfile
FROM nginx:alpine
RUN apk add php7-fpm
COPY pagina-web /usr/share/nginx/html
COPY default /etc/nginx/conf.d/default.conf
RUN sed -i 's/listen = 127.0.0.1:9000$/listen = \/var\/run\/php7-fpm.sock/g' /etc/php7/php-fpm.d/www.conf
RUN sed -i 's/;listen\.owner = nobody$/listen.owner = nginx/g' /etc/php7/php-fpm.d/www.conf
RUN sed -i 's/;listen\.group = nobody$/listen.group = nginx/g' /etc/php7/php-fpm.d/www.conf
#CMD php-fpm7
