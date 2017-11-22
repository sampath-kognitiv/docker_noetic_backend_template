FROM mysql:5.7
ADD init.sh /mysql/init.sh
ADD init_dump.sql /mysql/init_dump.sql

ADD init_dump.sql /docker-entrypoint-initdb.d/init_dump.sql
RUN chmod 755 /docker-entrypoint-initdb.d/init_dump.sql

RUN chmod 755 /mysql/init.sh
#RUN /mysql/init.sh