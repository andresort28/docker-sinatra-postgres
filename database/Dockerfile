FROM postgres
MAINTAINER andresortiz28@hotmail.com

ENV POSTGRES_USER=andres
ENV POSTGRES_PASSWORD=ortiz
COPY ./files/create_schema.sql /docker-entrypoint-initdb.d/
EXPOSE 5432
