FROM openjdk:18-slim-buster 
RUN apt-get update && apt-get install -y wget
RUN apt-get install -y python curl 

WORKDIR /mydir
COPY material-applications/spring-example-project/target . 
EXPOSE 8080
WORKDIR /mydir/target
#ENTRYPOINT java -jar ./target/docker-example-1.1.3.jar
CMD ["java", "-jar", "/mydir/docker-example-1.1.3.jar"]
