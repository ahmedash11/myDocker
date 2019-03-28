FROM alpine/git
WORKDIR /app
RUN git clone -b docker https://github.com/Youtube-Replica/YoutubeBananaVideos.git

FROM maven:3.5-jdk-8-alpine
WORKDIR /app
COPY --from=0 /app/YoutubeBananaVideos /app
RUN mvn install
