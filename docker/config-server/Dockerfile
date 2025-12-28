
FROM eclipse-temurin:17-jre
WORKDIR /app
COPY spring-petclinic-config-server/target/*.jar app.jar
EXPOSE 6666
ENTRYPOINT ["java","-jar","app.jar"]
