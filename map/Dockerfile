# Test web-app to use with Pluralsight courses and Docker Deep Dive book
# Linux x64
FROM ubuntu:18.04

LABEL maintainer="1079087531@qq.com"

# Replace apt source
ADD sources.list /etc/apt/sources.list

# Install Nginx
RUN apt-get update && apt-get -y install nginx

# Add Nginx config
RUN rm /etc/nginx/sites-enabled/default
ADD map.conf /etc/nginx/sites-enabled/map.conf

# Copy app to /code
COPY code /code

WORKDIR /code

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
