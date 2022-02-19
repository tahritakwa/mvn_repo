FROM maven:3.6.3-jdk-8
WORKDIR /my-app
COPY pom.xml ./
FROM openjdk:8-jre-alpine
EXPOSE 8080
WORKDIR /my-app
COPY  /my-app/target/my-app-1.0-SNAPSHOT.jar ./my-app-1.0-SNAPSHOT.jar
CMD ["/usr/bin/java", "-jar", "/my-app/my-app-1.0-SNAPSHOT.jar"]


