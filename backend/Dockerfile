FROM openjdk:11

RUN --mount=type=secret,id=MYSQL_URL \
    export MYSQL_URL=$(cat /run/secrets/MYSQL_URL) 

COPY target/GreenCommute-0.0.1-SNAPSHOT.jar .
ENTRYPOINT ["java","-jar","GreenCommute-0.0.1-SNAPSHOT.jar"]
EXPOSE 8000