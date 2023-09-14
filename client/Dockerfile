FROM node:14 AS production

ENV NODE_ENV=production

WORKDIR /usr/src/client

COPY package.json .
COPY yarn.lock .

RUN yarn

COPY . .

RUN yarn run build

CMD [ "sh", "-c", "npm start:production" ]
