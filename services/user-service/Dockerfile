FROM alpine/git
WORKDIR /app
RUN git clone -b hazem https://github.com/OA-GH/YoutubeBananaUser.git

FROM maven:3.5-jdk-8-alpine
WORKDIR /app
COPY --from=0 /app/YoutubeBananaUser /app
RUN mvn install
