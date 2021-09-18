FROM golang as youtube-dl 

WORKDIR /mydir
RUN apt-get update && apt-get install -y wget curl
CMD /mydir/server
#ENTRYPOINT ["tail", "-f", "/dev/null"]
