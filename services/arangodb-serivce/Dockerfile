FROM alpine/git
WORKDIR /db
RUN git clone https://github.com/HazemElAgaty/docker-psql-seeds.git

FROM arangodb
WORKDIR /db
COPY --from=0 /db/docker-psql-seeds /db
RUN mv services/arangoInit.js /docker-entrypoint-initdb.d/


