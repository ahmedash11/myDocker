FROM alpine/git
WORKDIR /app
RUN git clone -b docker https://github.com/Youtube-Replica/YoutubeBananaMessages.git

FROM maven:3.5-jdk-8-alpine
WORKDIR /app
COPY --from=0 /app/YoutubeBananaMessages /app
RUN mvn install
