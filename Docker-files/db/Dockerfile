FROM mysql AS BASE_IMAGE
# Good Prcatice to maintain tags/LABEL
LABEL "Project"="Vprofile"
LABEL "Author"="Bishnu"

ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_DATABASE="accounts"

COPY db_backup.sql docker-entrypoint-initdb.d/db_backup.sql
