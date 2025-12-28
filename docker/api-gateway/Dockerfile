FROM eclipse-temurin:17-jre
WORKDIR /app
COPY spring-petclinic-api-gateway/target/*.jar app.jar
EXPOSE 5555
ENTRYPOINT ["java","-jar","app.jar"]
