Step 5/16 : RUN rm -rf /usr/local/go && tar -C /usr/local -xzf go1.17.1.linux-amd64.tar.gz
 ---> Running in fcb21d389553
Removing intermediate container fcb21d389553
 ---> ad08308ef355
Step 6/16 : COPY example-backend .
 ---> d44f42fc53e2
Step 7/16 : ENV PATH=$PATH:/usr/local/go/bin
 ---> Running in 7f997a190a8e
Removing intermediate container 7f997a190a8e
 ---> 85c2f5187ff5
Step 8/16 : WORKDIR /mydir
 ---> Running in 4524405595f4
Removing intermediate container 4524405595f4
 ---> e3c562a0a66a
Step 9/16 : RUN go version
 ---> Running in be0818061a30
go version go1.17.1 linux/amd64
Removing intermediate container be0818061a30
 ---> e368d3aeea53
Step 10/16 : RUN go build
 ---> Running in 0854b355d9da
Removing intermediate container 0854b355d9da
 ---> 829123f0c092
Step 11/16 : ENV PORT=8080
 ---> Running in 7542a0552087
Removing intermediate container 7542a0552087
 ---> 5a73baedb128
Step 12/16 : ENV REQUEST_ORIGIN=http://localhost
 ---> Running in 075d93d0abcd
Removing intermediate container 075d93d0abcd
 ---> 11979268d808
Step 13/16 : ENV API_URL="http://localhost:8080"
 ---> Running in 020589ba159e
Removing intermediate container 020589ba159e
 ---> d4d4c3567105
Step 14/16 : RUN ./server
 ---> Running in dc47caaa0763
[Ex 2.4+] REDIS_HOST env was not passed so redis connection is not initialized
[Ex 2.6+] POSTGRES_HOST env was not passed so postgres connection is not initialized
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:	export GIN_MODE=release
 - using code:	gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /ping                     --> server/router.pingpong (4 handlers)
[GIN-debug] GET    /messages                 --> server/controller.GetMessages (4 handlers)
[GIN-debug] POST   /messages                 --> server/controller.CreateMessage (4 handlers)
[GIN-debug] Listening and serving HTTP on :8080

