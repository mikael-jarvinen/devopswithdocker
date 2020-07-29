FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl git

RUN git clone https://github.com/docker-hy/backend-example-docker.git server
WORKDIR server/

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs
RUN node -v && npm -v || echo "node didn't install correctly"

RUN npm install

ENV FRONT_URL=http://localhost:5000
EXPOSE 8000
ENTRYPOINT ["npm"]
CMD ["start"]
