FROM node:20.11-alpine as builder

# Must be entire project because `prepare` script is run during `npm install` and requires all files.
COPY src/google-maps /project
COPY tsconfig.json /tsconfig.json

WORKDIR /project

RUN npm install

CMD ["npm", "run", "env", "--", "dist/index.js"]