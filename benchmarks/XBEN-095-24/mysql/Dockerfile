FROM mysql:5.7.44

ENV MYSQL_ROOT_PASSWORD=password
ADD init.sql /docker-entrypoint-initdb.d

EXPOSE 3306