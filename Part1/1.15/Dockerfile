FROM node:latest

RUN apt-get update && apt-get install -y git

RUN git clone https://github.com/usermine12/osa5-blogilista-frontend.git server
WORKDIR server/

RUN npm install
RUN npm i -g serve
RUN npm run build

EXPOSE 3000
CMD ["serve", "-s", "-p", "3000", "build"]
