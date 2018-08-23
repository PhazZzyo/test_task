## Remove default nginx website
#RUN rm -rf /usr/share/nginx/html/*
## From ‘builder’ stage copy over the artifacts in dist folder to default nginx public folder
#COPY --from=builder /ng-app/dist /usr/share/nginx/html

FROM nginx:alpine
COPY nginx.conf /etc/nginx/nginx.conf
#COPY --from=node /testContainerAngular/src/app /usr/share/nginx/html

#RUN rm -rf /usr/share/nginx/html/*
#COPY /usr/src/app/src/ /usr/share/nginx/html

EXPOSE 80 443
