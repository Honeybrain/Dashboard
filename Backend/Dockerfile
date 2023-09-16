# Étape de build
FROM node:18.16.0

RUN apt-get update && apt-get install -y netcat-openbsd && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY . .

RUN yarn install

RUN yarn build

EXPOSE 50051

CMD ["yarn", "start:prod"]