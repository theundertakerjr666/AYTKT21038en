ubuntu:~/git_repos/tmc_dockeropen_uni/Exercise1_10$ docker run -p 8080:8080/tcp devopsdockeruh/simple-web-service
Starting log output
Wrote text to /usr/src/app/text.log

ubuntu:~/git_repos/tmc_dockeropen_uni$ docker ps -a
CONTAINER ID   IMAGE                                                 COMMAND                  CREATED          STATUS                        PORTS                                                                                                                                                 NAMES
9ae89a72dab4   devopsdockeruh/simple-web-service                     "/usr/src/app/server"    18 seconds ago   Up 17 seconds                 0.0.0.0:8080->8080/tcp
