
Step 14/22 : RUN apt-get purge -y --auto-remove curl
 ---> Running in 53fe30605fbb
Reading package lists...
Building dependency tree...
Reading state information...
The following packages will be REMOVED:
  curl* libcurl4*
0 upgraded, 0 newly installed, 2 to remove and 0 not upgraded.
After this operation, 1188 kB disk space will be freed.
(Reading database ... 15713 files and directories currently installed.)
Removing curl (7.74.0-1.3+b1) ...
Removing libcurl4:amd64 (7.74.0-1.3+b1) ...
Processing triggers for libc-bin (2.31-13) ...
Removing intermediate container 53fe30605fbb
 ---> 0fb2230a71f5
Step 15/22 : RUN rm -rf /var/lib/apt/lists/*
 ---> Running in ebdd411ceba7
Removing intermediate container ebdd411ceba7
 ---> 083ece8c0a23
Step 16/22 : RUN useradd -m appuser
 ---> Running in 814f07303e98
Removing intermediate container 814f07303e98
 ---> 2e898e26a99b
Step 17/22 : RUN chown appuser .
 ---> Running in 3d96a4d2cba5
Removing intermediate container 3d96a4d2cba5
 ---> 75ce5ea9bba8
Step 18/22 : USER appuser
 ---> Running in 8382bd86bd73
Removing intermediate container 8382bd86bd73
 ---> 2b6ed3cff229
Step 19/22 : RUN go test ./...
 ---> Running in 2b4da5255491
ok  	server	0.021s
?   	server/cache	[no test files]
ok  	server/common	0.007s
?   	server/controller	[no test files]
?   	server/pgconnection	[no test files]
?   	server/router	[no test files]
Removing intermediate container 2b4da5255491
 ---> 2f67f5dd559c
Step 20/22 : RUN ls -ltra /mydir
 ---> Running in 20299bf0b270
total 148960
-rw-r--r-- 1 root    root 134784143 Sep  9 17:49 go1.17.1.linux-amd64.tar.gz
drwxrwxr-x 2 root    root      4096 Sep 22 09:40 router
drwxrwxr-x 2 root    root      4096 Sep 22 09:40 pgconnection
-rw-rw-r-- 1 root    root     19736 Sep 22 09:40 go.sum
-rw-rw-r-- 1 root    root       175 Sep 22 09:40 go.mod
drwxrwxr-x 2 root    root      4096 Sep 22 09:40 controller
drwxrwxr-x 2 root    root      4096 Sep 22 09:40 common
drwxrwxr-x 2 root    root      4096 Sep 22 09:40 cache
-rw-rw-r-- 1 root    root       490 Sep 22 09:40 app_test.go
-rw-rw-r-- 1 root    root       189 Sep 22 09:40 app.go
-rw-rw-r-- 1 root    root      1351 Sep 22 09:40 README.md
-rw-rw-r-- 1 root    root       139 Sep 22 09:40 .gitignore
-rw-rw-r-- 1 root    root        71 Sep 22 09:40 .dockerignore
-rwxr-xr-x 1 root    root  17666142 Sep 22 09:51 server
drwxr-xr-x 1 appuser root      4096 Sep 22 09:51 .
drwxr-xr-x 1 root    root      4096 Sep 22 10:04 ..
Removing intermediate container 20299bf0b270
 ---> 49d385a56e36
Step 21/22 : EXPOSE 8080
 ---> Running in e6e9e1a50735
Removing intermediate container e6e9e1a50735
 ---> 5c3729c73c5b
Step 22/22 : CMD /mydir/server
 ---> Running in 9e8ca5879710
Removing intermediate container 9e8ca5879710
 ---> e5e8bd8c2d17
Successfully built e5e8bd8c2d17



------------------------------------------------------------------------------------------------------------------------

Exercise3_4$ docker build -f Dockerfile_frontend .
Sending build context to Docker daemon  784.4kB
Step 1/20 : FROM ubuntu:18.04 as exercise-2-8-frontend
 ---> 54919e10a95d
Step 2/20 : EXPOSE 5000
 ---> Running in e1bd23405bdf
Removing intermediate container e1bd23405bdf
 ---> 70451c92bf56
Step 3/20 : WORKDIR /mydir
 ---> Running in 2d5d77666735
Removing intermediate container 2d5d77666735
 ---> 3951c0935780
Step 4/20 : RUN apt-get update && apt-get install -y wget ca-certificates openssl
 ---> Running in 00d31eb61c19
.......
......
......
Removing intermediate container ba33dd44f9b6
 ---> 42fa25475fd3
Step 16/20 : RUN rm -rf /var/lib/apt/lists/*
 ---> Running in e58e35cce009
Removing intermediate container e58e35cce009
 ---> a317794eef10
Step 17/20 : RUN useradd -m appuser
 ---> Running in f5c76c42740c
Removing intermediate container f5c76c42740c
 ---> 160adf984745
Step 18/20 : RUN chown appuser .
 ---> Running in 384cb3c4d699
Removing intermediate container 384cb3c4d699
 ---> 56ef4a22243e
Step 19/20 : USER appuser
 ---> Running in 204f57424bf2
Removing intermediate container 204f57424bf2
 ---> 5283ba854ddf
Step 20/20 : CMD serve -s -l 5000 build
 ---> Running in fb4268bdbb57
Removing intermediate container fb4268bdbb57
 ---> 700a5363afe6
Successfully built 700a5363afe6





