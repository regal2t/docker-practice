# Use official Maven image as a build stage
FROM maven:3.8.4-openjdk-17-slim AS build
WORKDIR /app
COPY . .
RUN mvn clean package

# Use AdoptOpenJDK as a runtime stage
FROM openjdk:17-jdk-alpine
WORKDIR /app
COPY --from=build /app/target/*.jar app.jar

# Install MySQL client
RUN apk add --no-cache mysql-client

# Expose port and set default command
EXPOSE 8080
CMD ["java", "-jar", "app.jar"]
