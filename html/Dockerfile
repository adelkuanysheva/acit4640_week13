FROM nginx

RUN mkdir /etc/nginx/templates
COPY default.conf.template /etc/nginx/templates

RUN apt-get update
RUN mkdir /app
WORKDIR /app
COPY index.html /usr/share/nginx/html
ADD /static /usr/share/nginx/html/static

EXPOSE 8000

