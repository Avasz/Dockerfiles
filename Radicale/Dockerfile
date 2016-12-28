FROM alpine:latest
MAINTAINER Avasz "avasz@protonmail.com"

RUN apk update \
	&& apk add python py-pip \
	&& pip install radicale

ENTRYPOINT ["radicale"]




