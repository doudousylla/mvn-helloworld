FROM eclipse-temurin:17-jdk-alpine

WORKDIR /app

COPY target/mvn-helloworld-1.0-SNAPSHOT.jar mvn-helloworld-1.0-SNAPSHOT.jar.jar

ENTRYPOINT ["java", "-jar", "mvn-helloworld-1.0-SNAPSHOT.jar.jar"]
