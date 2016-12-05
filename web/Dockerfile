FROM centos:7
MAINTAINER andresortiz28@hotmail.com

RUN yum install ruby -y
RUN yum install rubygems
RUN gem install sinatra

RUN yum groupinstall "Development tools" -y

RUN yum install https://download.postgresql.org/pub/repos/yum/9.6/redhat/rhel-7-x86_64/pgdg-redhat96-9.6-3.noarch.rpm -y
RUN yum install postgresql96-libs -y
RUN yum install postgresql96-devel -y
RUN yum install ruby-devel -y
RUN gem install pg -- --with-pg-config=/usr/pgsql-9.6/bin/pg_config

RUN mkdir /home/web
COPY ./files/ /home/web
EXPOSE 8888
WORKDIR /home/web/api
CMD ruby app.rb -o 0.0.0.0 -p 8888