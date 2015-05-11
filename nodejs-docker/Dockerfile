
FROM ubuntu:14.04
MAINTAINER Sergio Soto <sotonez@gmail.com>
ENV REFRESHED_AT 2015-01-19

RUN apt-get -yqq update
RUN apt-get -yqq install nodejs npm
RUN ln -s /usr/bin/nodejs /usr/bin/node
RUN npm i -g bower socket.io intrepidjs-cli

WORKDIR /opt/

RUN mkdir intrepidjs && cd intrepidjs && intrepidjs-init myApp 

EXPOSE 8000

ENTRYPOINT [ "node", "app.js" ]
