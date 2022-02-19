FROM openjdk:8-jre-alpine
EXPOSE 8080
ADD /target/my-app-1.0-SNAPSHOT.jar /my-app-1.0-SNAPSHOT.jar
ENTRYPOINT ["/usr/bin/java","-jar","-Dspring.profiles.active=test","/my-app-1.0-SNAPSHOT.jar"]

