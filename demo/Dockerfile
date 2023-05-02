FROM eclipse-temurin:17-jdk-alpine
VOLUME /tmp
COPY ./pom.xml ./pom.xml
COPY ./src ./src
COPY ./mvnw ./mvnw
COPY ./.mvn ./.mvn
RUN ./mvnw install 
COPY target/app.jar app.jar
ENTRYPOINT ["java","-jar","app.jar"]