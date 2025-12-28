FROM eclipse-temurin:17-jre
WORKDIR /app
COPY spring-petclinic-admin-server/target/*.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java","-jar","app.jar"]
