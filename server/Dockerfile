FROM node:18-alpine
WORKDIR /ws

COPY package.json ./
COPY yarn.lock ./

RUN yarn install --frozen-lockfile 

COPY . .

RUN yarn build

CMD ["node", ".", "--host", "0.0.0.0"]

EXPOSE 8080

