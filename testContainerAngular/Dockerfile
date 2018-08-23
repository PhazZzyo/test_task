FROM node:alpine as builder

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY package.json /usr/src/app/package.json
COPY package-lock.json /usr/src/app/package-lock.json
RUN npm install
RUN npm install -g @angular/cli@1.4.5

COPY . /usr/src/app
CMD ng serve --host 0.0.0.0
#RUN npm run build

EXPOSE 4200

#FROM nginx:alpine
#COPY nginx.conf /etc/nginx/nginx.conf
#COPY src/ /usr/share/nginx/html
#COPY --from=node /testContainerAngular/src/app /usr/share/nginx/html
#EXPOSE 80 443
