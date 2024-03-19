FROM ubuntu:22.04

RUN apt-get update -y \
 && DEBIAN_FRONTEND=noninteractive apt-get install -y python3-pip python3-opencv \
 && pip3 install Flask 

WORKDIR /app
COPY . .

#CMD ["python3","-m","flask","run","--host=0.0.0.0"]
