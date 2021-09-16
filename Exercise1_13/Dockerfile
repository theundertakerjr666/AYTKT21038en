FROM ubuntu:18.04 as exercise1_13

WORKDIR /mydir
RUN apt-get update && apt-get install -y wget curl
RUN wget https://golang.org/dl/go1.17.1.linux-amd64.tar.gz
RUN rm -rf /usr/local/go && tar -C /usr/local -xzf go1.17.1.linux-amd64.tar.gz 
COPY example-backend .
ENV PATH=$PATH:/usr/local/go/bin
WORKDIR /mydir
RUN go version 
RUN go build 
ENV PORT=8080
ENV REQUEST_ORIGIN="http://127.0.0.1:8080"
ENV API_URL="http://127.0.0.1:8080"
RUN ls -ltra /mydir
RUN go install . 
EXPOSE 8080
#ENTRYPOINT API_URL=http://127.0.0.1:8080
CMD ["/mydir/server"]
ENTRYPOINT ["tail", "-f", "/dev/null"]
