FROM postgres:9.6.2

MAINTAINER aruis (lovearuis@gmail.com)

RUN apt-get -y update 
RUN apt-get -y install gcc make
RUN apt-get -y install wget unzip
RUN apt-get -y install postgresql-server-dev-9.6
RUN apt-get -y install postgresql-9.6-plv8
RUN apt-get -y install libmysqlclient-dev
RUN  wget https://github.com/EnterpriseDB/mysql_fdw/archive/REL-2_2_0.zip && \
  unzip REL-2_2_0.zip && \
  cd mysql_fdw-REL-2_2_0 && make USE_PGXS=1 && make USE_PGXS=1 install && \
  cd .. && rm -R mysql_fdw-REL-2_2_0 && \
  rm -rf /var/lib/apt/lists/*