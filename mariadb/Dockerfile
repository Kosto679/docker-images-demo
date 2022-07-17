FROM mariadb:10.7
ADD init.sql /docker-entrypoint-initdb.d
COPY my.cnf /etc/mysql/my.cnf
ENV   MARIADB_ROOT_PASSWORD: mypass123
ENV   MARIADB_DATABASE: crawlerdb
ENV   MARIADB_USER: example
ENV   MARIADB_PASSWORD: example
HEALTHCHECK CMD ["healthcheck.sh", "--su=mysql", "--connect", "--innodb_initialized"]
