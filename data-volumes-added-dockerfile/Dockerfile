FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

# path inside of the container that needs to be mapped outside of the container. Currently docker controls the mapping.
VOLUME [ "/app/feedback" ]

CMD [ "node", "server.js" ]