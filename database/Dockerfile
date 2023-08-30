FROM mysql:8.1

ENV MYSQL_ROOT_PASSWORD=abcd
ENV MYSQL_USER=gc
ENV MYSQL_PASSWORD=Gc@12345

EXPOSE 3306

COPY ./bc_25_gc.sql /docker-entrypoint-initdb.d/
COPY ./bc_25_gc_data.sql /docker-entrypoint-initdb.d/
