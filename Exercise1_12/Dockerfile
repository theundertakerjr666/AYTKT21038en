FROM ubuntu:18.04 
EXPOSE 5000
WORKDIR /mydir
RUN apt-get update && apt-get install -y wget
RUN apt-get install -y curl 
COPY example-frontend .
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash
RUN apt-get install -y nodejs 
WORKDIR /mydir
RUN node -v && npm -v
ENV API_URL="http://localhost:5000"
RUN npm install
RUN npm run build
RUN npm install -g serve 
RUN serve -s -l 5000 build 
