[INFO] Replacing main artifact with repackaged archive
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  23.875 s
[INFO] Finished at: 2021-09-11T18:21:48+03:00
[INFO] ------------------------------------------------------------------------
(base) genera@generaiotubuntu:~/git_repos/tmc_dockeropen_uni/Exercise1_11/material-applications/spring-example-project$ ls target/
classes  docker-example-1.1.3.jar  docker-example-1.1.3.jar.original  generated-sources  generated-test-sources  maven-archiver  maven-status  test-classes

ubuntu:~/git_repos/tmc_dockeropen_uni/Exercise1_11$ docker build -t exercise1_11 .
Sending build context to Docker daemon   20.8MB
Step 1/8 : FROM openjdk:18-slim-buster
 ---> 1c20c48d7087
Step 2/8 : RUN apt-get update && apt-get install -y wget
 ---> Using cache
 ---> 66c06ddd4671
Step 3/8 : RUN apt-get install -y python curl
 ---> Using cache
 ---> feebf328f939
Step 4/8 : WORKDIR /mydir
 ---> Using cache
 ---> f0ec20109b0c
Step 5/8 : COPY material-applications/spring-example-project/target .
 ---> Using cache
 ---> be626c3cba05
Step 6/8 : EXPOSE 8080
 ---> Using cache
 ---> 97b0d550f017
Step 7/8 : WORKDIR /mydir/target
 ---> Using cache
 ---> a1bb878d0320
Step 8/8 : CMD ["java", "-jar", "/mydir/docker-example-1.1.3.jar"]
 ---> Running in 573bb88443f4
Removing intermediate container 573bb88443f4
 ---> b096fbbb4ace
Successfully built b096fbbb4ace
Successfully tagged exercise1_11:latest
(base) genera@generaiotubuntu:~/git_repos/tmc_dockeropen_uni/Exercise1_11$ docker run -p 8080:8080 exercise1_11

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::        (v2.1.3.RELEASE)


