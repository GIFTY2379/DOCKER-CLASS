#pulling a base image from node.js
FROM node:13.12.0-alpine

#Setting a working directory
WORKDIR /my_app

#Adding /my_app/node_modules/.bin to path
ENV PATH /my_app/node_modules/.bin:$PATH

#Installing dependencies
COPY package.json ./
COPY package-lock.json ./
RUN npm install --silent

#Adding the application
COPY . ./

#Start application
CMD [ "npm","start" ]