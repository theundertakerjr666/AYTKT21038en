ubuntu:~/git_repos/tmc_dockeropen_uni/Exercise1_4$ docker run  --rm -it --name looper-it ubuntu sh -c 'apt update; apt install -y curl;echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://helsinki.fi;'

Setting up curl (7.68.0-1ubuntu2.6) ...
Processing triggers for libc-bin (2.31-0ubuntu9.2) ...
Processing triggers for ca-certificates (20210119~20.04.1) ...
Updating certificates in /etc/ssl/certs...
0 added, 0 removed; done.
Running hooks in /etc/ca-certificates/update.d...
done.
Input website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
</body></html>
