FROM mysql:5.7

ADD my.cnf /etc/mysql/my.cnf
CMD ["mysqld", "--datadir=/var/lib/mysql", "--user=mysql"]

ADD init_dump.sql /docker-entrypoint-initdb.d/init_dump.sql
RUN chmod 755 /docker-entrypoint-initdb.d/init_dump.sql

ADD grant_permission.sql /docker-entrypoint-initdb.d/grant_permission.sql
RUN chmod 755 /docker-entrypoint-initdb.d/grant_permission.sql

#ADD init.sh /mysql/init.sh
#RUN chmod 755 /mysql/init.sh
#RUN /mysql/init.sh