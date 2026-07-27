FROM node:22-alpine

WORKDIR /app

COPY package*.json ./

ARG SERVER_PORT
ENV SERVER_PORT=${SERVER_PORT}

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]
