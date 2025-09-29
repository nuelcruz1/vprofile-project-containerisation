FROM mysql:8.0.33
LABEL project="vprofile"
LABEL Author="Emmanuel"

ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MSQL_DATABASE="accounts"

ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql