FROM nginx:latest
ARG ENVIRONMENT=prod
COPY ./${ENVIRONMENT}.conf.template /etc/nginx/templates/default.conf.template
COPY ./html/ /usr/share/nginx/html/

EXPOSE 80
EXPOSE 443
