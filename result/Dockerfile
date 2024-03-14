FROM node:20-alpine

WORKDIR /app

COPY . .

RUN npm cache clean --force

RUN npm install

EXPOSE 80

CMD [ "npm", "start"]
#CMD ["node", "server.js"]