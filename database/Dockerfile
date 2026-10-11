FROM mysql/mysql-server:5.7
ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_USER=root
EXPOSE 3306
COPY database.sql /docker-entrypoint-initdb.d/database.sql 
RUN useradd mysqluser && \
mkdir -p /var/run/mysqld && \
chown -R mysqluser:mysqluser /var/lib/mysql/ && \
chown -R mysqluser:mysqluser /var/lib/mysql-files/ && \
chown -R mysqluser:mysqluser /var/run/mysqld/ && \
chown -R mysqluser:mysqluser /tmp

USER mysqluser
