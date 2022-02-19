FROM openjdk:8-jre-alpine
WORKDIR /my_app
ADD /target/my-app-1.0-SNAPSHOT.jar /my-app-1.0-SNAPSHOT.jar
EXPOSE 8080
ENTRYPOINT ["/usr/bin/java","-jar","-Dspring.profiles.active=test","/my-app-1.0-SNAPSHOT.jar"]

