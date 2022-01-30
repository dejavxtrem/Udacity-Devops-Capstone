FROM node:14 as build

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY package.json /usr/src/app

RUN npm install

COPY . /usr/src/app

RUN npm run build

EXPOSE 80

FROM nginx:alpine

COPY --from=build /usr/src/app/build /usr/share/nginx/html