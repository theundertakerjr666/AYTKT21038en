ubuntu:~/git_repos/tmc_dockeropen_uni/Exercise1_7$ docker build . -t web-server:latest
Sending build context to Docker daemon  2.048kB
Step 1/1 : FROM devopsdockeruh/simple-web-service:alpine
 ---> fd312adc88e0
Successfully built fd312adc88e0
Successfully tagged web-server:latest
ubuntu:~/git_repos/tmc_dockeropen_uni/Exercise1_7$ docker run web-server
Starting log output
Wrote text to /usr/src/app/text.log

