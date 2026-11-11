FROM flyway/flyway:7.15.0-alpine
ENV CONTAINER_NAME qbsh-flyway
COPY ddl /flyway/sql/
COPY dml /flyway/sql/
ENTRYPOINT ["sh", "-c"]
CMD ["flyway -url=jdbc:postgresql://$DB_HOST:$DB_PORT/$DB_DBNAME -schemas=$DB_SCHEMA -user=$DB_USER -password=$DB_PASSWORD -connectRetries=60 -cleanDisabled=$FLYWAY_CLEAN_DISABLED migrate"]

