##### Dockerfile #####
FROM node:18.18-alpine

RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app
WORKDIR /home/node/app
COPY --chown=node:node package*.json ./
USER node
RUN npm install
COPY --chown=node:node . .

EXPOSE 5000
CMD [ "node", "server.js" ]