#Stage1
#FROM node:14.17.0-alpine as build-step
#RUN mkdir -p /app
#WORKDIR /app
#COPY package.json /app
#RUN npm install
#COPY . /app
#RUN npm run build --prod

#Stage2
FROM nginx:1.20.1
RUN apt-get update
RUN apt-get install apache2-utils -y
RUN (echo 'qburst123'; echo 'qburst123') | htpasswd -c /etc/nginx/.htpasswd qburst
COPY /dist/ng-docker-example /usr/share/nginx/html
RUN mkdir /etc/nginx/certs
RUN chmod a+r /etc/nginx/certs
COPY nginx_backup.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
