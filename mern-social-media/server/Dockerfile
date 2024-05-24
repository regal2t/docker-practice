FROM node:18.2.0-slim

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install 
RUN npm install -g nodemon 


COPY . .

EXPOSE 5000

CMD ["node", "index.js"]
