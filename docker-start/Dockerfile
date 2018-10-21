FROM postgres:9.5.10

## PostGIS activation
RUN apt-get -y update && \
    apt-get -y install postgis \
                       postgresql-9.5-pgrouting

## DB setup
ADD data.tar.gz /docker-entrypoint-initdb.d/
RUN chown postgres:postgres /docker-entrypoint-initdb.d/*.sql
