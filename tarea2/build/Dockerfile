FROM php:7.2-apache
MAINTAINER Fran Madueño "frandh1997@gmail.com"

EXPOSE 80

RUN docker-php-ext-install mysqli
COPY bookmedik /var/www/html/
ADD script.sh /usr/local/bin/

RUN chmod +x /usr/local/bin/script.sh

ENV DATABASE_USER=bookmedik
ENV DATABASE_PASSWORD=bookmedik
ENV DATABASE_HOST=servidor_mysql

CMD ["script.sh"]

