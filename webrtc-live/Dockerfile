FROM ubuntu:22.04

RUN apt-get update \
 && apt-get install -y nodejs npm 

WORKDIR /app
COPY . .
RUN npm install

CMD ["npm","run","dev"]
