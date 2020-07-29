FROM openjdk:8

RUN apt-get update && apt-get install git
RUN git clone https://github.com/docker-hy/spring-example-project.git ./server
WORKDIR server/

RUN ./mvnw package

EXPOSE 8080
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
