FROM node:20.11-alpine as builder

COPY . /project

WORKDIR /project

RUN npm install

CMD ["npm", "run", "env", "--", "dist/index.js"]