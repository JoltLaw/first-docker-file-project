# use this empty Dockerfile to build your assignment

FROM node:6-alpine 

EXPOSE 3000

RUN  apk add --update tini 

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app

COPY package.json package.json

RUN npm install &&  npm cache clean

COPY . .

CMD ["/sbin/tini", "--", "node", "./bin/www"]

# NOTE: The instructions are now in the README.md file in this directory.
