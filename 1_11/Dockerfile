FROM maven:3.6.3-jdk-8 AS builder
WORKDIR /usr/src/app

COPY pom.xml .
COPY src ./src

RUN mvn clean package -DskipTests

FROM amazoncorretto:8

WORKDIR /app
EXPOSE 8080
COPY --from=builder /usr/src/app/target/docker-example-1.1.3.jar ./app.jar

CMD ["java", "-jar" ,"app.jar"]
