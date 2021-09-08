ubuntu:~/git_repos/tmc_dockeropen_uni/Exercise1_4$ docker images -a
...
devopsdockeruh/simple-web-service               ubuntu         4e3362e907d5   5 months ago    83MB
devopsdockeruh/simple-web-service               alpine         fd312adc88e0   5 months ago    15.7MB

ubuntu:~/git_repos/tmc_dockeropen_uni/Exercise1_5$ docker run devopsdockeruh/simple-web-service:alpine
Starting log output
Wrote text to /usr/src/app/text.log


Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-09-08 09:46:05 +0000 UTC
2021-09-08 09:46:07 +0000 UTC
2021-09-08 09:46:09 +0000 UTC
2021-09-08 09:46:11 +0000 UTC
2021-09-08 09:46:13 +0000 UTC
/usr/src/app # cat /usr/src/app/text.log
