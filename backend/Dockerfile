FROM openjdk:11

RUN --mount=type=secret,id=MYSQL_URL \
    --mount=type=secret,id=MYSQL_USERNAME \
    --mount=type=secret,id=MYSQL_PASSWORD \
    export MYSQL_URL =$(cat /run/secrets/MYSQL_URL ) && \
    export MYSQL_USERNAME=$(cat /run/secrets/MYSQL_USERNAME) && \
    export MYSQL_PASSWORD=$(cat /run/secrets/MYSQL_PASSWORD) && \
    yarn gen

COPY target/GreenCommute-0.0.1-SNAPSHOT.jar .
ENTRYPOINT ["java","-jar","GreenCommute-0.0.1-SNAPSHOT.jar"]
EXPOSE 8000