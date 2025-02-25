# # users-api/Dockerfile
# FROM openjdk:11

# # Set the working directory
# WORKDIR /app

# # Copy the Maven wrapper and pom.xml
# COPY mvnw .
# COPY .mvn .mvn
# COPY pom.xml .

# # Copy the source code
# COPY src src

# # Build the application and skip tests
# RUN ./mvnw clean install -DskipTests

# # Set environment variables
# ENV JWT_SECRET=foo
# ENV SERVER_PORT=8083

# # Expose the application port
# EXPOSE 8083

# # Run the application
# CMD ["java", "-jar", "target/users-api-0.0.1-SNAPSHOT.jar"]


# users-api/Dockerfile
FROM openjdk:8 

# Set the working directory
WORKDIR /app

# Copy the Maven wrapper and pom.xml
COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .

# Copy the source code
COPY src src

# Build the application and skip tests
RUN ./mvnw clean install -DskipTests

# Set environment variables
ENV JWT_SECRET=myfancysecret
ENV SERVER_PORT=8083

# Expose the application port
EXPOSE 8083

# Run the application
CMD ["java", "-jar", "target/users-api-0.0.1-SNAPSHOT.jar"]