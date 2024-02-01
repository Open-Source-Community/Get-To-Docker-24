FROM node:19-alpine

COPY package.json /usr/app/
COPY src /usr/app/

WORKDIR /usr/app

RUN npm install 

CMD ["node", "server.js"]

