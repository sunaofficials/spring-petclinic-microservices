FROM eclipse-temurin:17-jre
WORKDIR /app
COPY spring-petclinic-genai-service/target/*.jar app.jar
EXPOSE 2222
ENTRYPOINT ["java","-jar","app.jar"]
