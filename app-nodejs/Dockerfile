FROM ubuntu:trusty
MAINTAINER Giorgio Crivellari <miticojo@gmail.com>
 
# install our dependencies and nodejs
RUN apt-get update && \
    apt-get -y install python-software-properties git build-essential curl
RUN curl -sL https://deb.nodesource.com/setup | bash - && \
    apt-get -y install nodejs
RUN apt-get clean

# use changes to package.json to force Docker not to use the cache
# when we change our application's nodejs dependencies:
#ADD package.json /tmp/package.json
#RUN cd /tmp && npm install
#RUN mkdir -p /opt/app && cp -a /tmp/node_modules /opt/app/
#RUN mkdir -p /opt/app/logs

#COPY . /opt/app

# From here we load our application's code in, therefore the previous docker
# "layer" thats been cached will be used if possible
#WORKDIR /opt/app
#ADD . /opt/app

# Set stage configuration file loaded by node application
#ENV NODE_ENV "production"

#EXPOSE 3000
 
#CMD ["node", "bin/www"]
