FROM mysql:8.0.33 as db_container
LABEL "Project"="vprofile"
LABEL "Author"="TT"

ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_DATABASE="accounts"

ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
# The above line will automatically execute the SQL script when the container is started for the first time.


