FROM devopsdockeruh/heroku-example as registry.heroku.com/justin-exercise-1-15/web 

WORKDIR /mydir
RUN apt-get update && apt-get install -y wget curl
CMD tail -f /var/log/messages
#ENTRYPOINT ["tail", "-f", "/dev/null"]
