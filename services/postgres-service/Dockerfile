FROM alpine/git
WORKDIR /db
RUN git clone https://github.com/HazemElAgaty/docker-psql-seeds.git

FROM postgres:9.6.8-alpine
WORKDIR /db
COPY --from=0 /db/docker-psql-seeds /db
RUN mv services/tables.sql /docker-entrypoint-initdb.d/
RUN mv services/procedures.sql /docker-entrypoint-initdb.d/
RUN mv services/user-service/zseeds.sql /docker-entrypoint-initdb.d/
