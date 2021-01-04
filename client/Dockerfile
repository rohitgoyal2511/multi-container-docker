FROM node:14.14.0-alpine as builder
WORKDIR '/app'
COPY ./package.json ./
RUN npm install
COPY . .
RUN npm run start

FROM nginx
expose 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf