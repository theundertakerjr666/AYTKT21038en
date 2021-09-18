
$ docker login
Login with your Docker ID to push and pull images from Docker Hub. If you don't have a Docker ID, head over to https://hub.docker.com to create one.
Username: justinraj1984
Password:
WARNING! Your password will be stored unencrypted in /home/genera/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded

Exercise1_15$ docker push justinraj1984/youtube-dl
Using default tag: latest
The push refers to repository [docker.io/justinraj1984/youtube-dl]
88f14c7b3b8f: Pushed
bb35f041afa8: Pushed
f88ba2561a51: Mounted from library/golang
7a78fbd87c8e: Mounted from library/golang
2a729d757bf1: Mounted from library/golang
8555e663f65b: Mounted from library/golang
d00da3cd7763: Mounted from library/golang
4e61e63529c2: Mounted from library/golang
799760671c38: Mounted from library/golang
latest: digest: sha256:0227516c36b1a94fae04edf1dfce42094a186ec0e5cbd2123e19a032907ce1ca size: 2214

Link to the image:
https://hub.docker.com/layers/167818322/justinraj1984/youtube-dl/latest/images/sha256-0227516c36b1a94fae04edf1dfce42094a186ec0e5cbd2123e19a032907ce1ca?context=repo

Image tag:
justinraj1984/youtube-dl:latest
