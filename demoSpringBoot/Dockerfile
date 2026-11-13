FROM openjdk:17
COPY . .
RUN mvn clean package -DskipTests

FROM eclipse-temurin:17-jdk-alpine
COPY --from=build /target/demoSpringBoot-1.jar app.jar
ENTRYPOINT ["java", "-jar", "/app.jar"]