FROM adoptopenjdk/openjdk11:alpine-jre

# Build-time variable for JAR location
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

# Copy the JAR into container
COPY ${artifact} app.jar

# Optional: declare the default port
EXPOSE 8000

# Run the app
ENTRYPOINT ["java","-jar","app.jar"]
