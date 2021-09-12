ubuntu:~/git_repos/tmc_dockeropen_uni/Exercise1_12$ docker build -t exercise1_12 .
Sending build context to Docker daemon  731.6kB
Step 1/16 : FROM ubuntu:18.04
 ---> 54919e10a95d
Step 2/16 : WORKDIR /mydir
 ---> Using cache
 ---> b68157dd3863
Step 3/16 : RUN apt-get update && apt-get install -y wget
 ---> Using cache
 ---> 3cd7e7669f7f
Step 4/16 : RUN apt-get install -y curl
 ---> Using cache
 ---> b8220539ea1e
Step 5/16 : COPY example-frontend .
 ---> Using cache
 ---> c927e5c55b60
Step 6/16 : RUN curl -sL https://deb.nodesource.com/setup_14.x | bash
 ---> Using cache
 ---> b9d5809ba22f
Step 7/16 : RUN apt-get install -y nodejs
 ---> Using cache
 ---> 69d363a0ff2d
Step 8/16 : WORKDIR /mydir
 ---> Using cache
 ---> 6e00e598a391
Step 9/16 : RUN node -v && npm -v
 ---> Using cache
 ---> 7f41b646c15a
Step 10/16 : RUN npm install
 ---> Running in 344c77a12da2
found 6219 vulnerabilities (499 moderate, 5720 high)
  run `npm audit fix` to fix them, or `npm audit` for details
Removing intermediate container 344c77a12da2
 ---> 57d98711504c
Step 11/16 : RUN npm run build
 ---> Running in caa63e679978
Removing intermediate container caa63e679978
 ---> 9c56dece666c
Step 12/16 : ENV API_URL="http://localhost:5000"
 ---> Running in c47f5c89d1f3
Removing intermediate container c47f5c89d1f3
 ---> ff4e563ebe44
Step 13/16 : RUN npm install -g serve
 ---> Running in b26b6b0a079b
/usr/bin/serve -> /usr/lib/node_modules/serve/bin/serve.js
+ serve@12.0.1
added 88 packages from 42 contributors in 5.062s
Removing intermediate container b26b6b0a079b
 ---> a6d29ea800f0
Step 14/16 : RUN serve -s -l 5000 build
 ---> Running in a920e5b0778d
INFO: Accepting connections at http://localhost:5000
