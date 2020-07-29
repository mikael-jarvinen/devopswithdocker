FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl git

RUN git clone https://github.com/docker-hy/frontend-example-docker.git server
WORKDIR server/

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs
RUN node -v && npm -v || echo "node didn't install correctly"
RUN npm install

EXPOSE 5000

ENV API_URL=http://localhost:8000

ENTRYPOINT ["npm"]
CMD ["start"]
