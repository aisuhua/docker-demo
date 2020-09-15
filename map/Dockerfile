# Test web-app to use with Pluralsight courses and Docker Deep Dive book
# Linux x64
FROM ubuntu:18.04

LABEL maintainer="1079087531@qq.com"

# Replace apt source
ADD sources.list /etc/apt/sources.list

# Install Node and NPM
RUN apt-get update && apt-get -y install nginx

# Add config
ADD nginx.conf /etc/nginx/nginx.conf

# Copy app to /code
COPY code /code

WORKDIR /code

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
