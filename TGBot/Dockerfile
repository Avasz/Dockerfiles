FROM alpine:latest
MAINTAINER Avash Mulmi "avasz@protonmail.com"

RUN apk update \
    && apk add nodejs \
    && apk add python \
    && apk add git \
    && apk add gcc g++ make

RUN mkdir -p /opt/
WORKDIR /opt/
RUN pwd
RUN git clone https://github.com/jmendeth/node-botgram.git && cd node-botgram


WORKDIR /opt/node-botgram/
RUN pwd
RUN npm install

WORKDIR /opt/node-botgram/examples/shell
RUN npm install

WORKDIR /opt/node-botgram/examples/shell/
ENTRYPOINT ["npm", "start"]

#You can specify a CMD with your Bot AuthTOken and Your ID in the following line to run it as default if wanted.
#Remove the comments and replace the placeholders with suitable values
#CMD ["auth_token", "your_id"]

