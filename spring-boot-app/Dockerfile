# Stage 1: Build the JAR
FROM maven:3.8.7-openjdk-17 AS builder
WORKDIR /app
COPY . .
RUN mvn clean package

# Stage 2: Run the JAR
FROM adoptopenjdk/openjdk11:alpine-jre
WORKDIR /opt/app
COPY --from=builder /app/target/spring-boot-web.jar app.jar
ENTRYPOINT ["java", "-jar", "app.jar"]
