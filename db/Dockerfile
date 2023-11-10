# Derived from official mysql image (our base image)
FROM mysql:8
ENV MYSQL_ROOT_PASSWORD=password
ENV MYSQL_DATABASE=mydb
ENV MYSQL_ROOT_USER=root
COPY ./sql-scripts/ /docker-entrypoint-initdb.d/
COPY ./db-Setting/my.cnf /etc/mysql/my.cnf
