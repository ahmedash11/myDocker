FROM alpine/git
WORKDIR /app
RUN git clone -b docker https://github.com/Youtube-Replica/YoutubeBananaComment.git

FROM maven:3.5-jdk-8-alpine
WORKDIR /app
COPY --from=0 /app/YoutubeBananaComment /app
RUN mvn install
