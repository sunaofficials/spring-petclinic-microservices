FROM eclipse-temurin:17-jre
WORKDIR /app
COPY spring-petclinic-genai-service/target/*.jar app.jar
EXPOSE 4444
ENTRYPOINT ["java","-jar","app.jar"]
