FROM eclipse-temurin:17-jre
WORKDIR /app
COPY spring-petclinic-discovery-server/target/*.jar app.jar
EXPOSE 7777
ENTRYPOINT ["java","-jar","app.jar"]
