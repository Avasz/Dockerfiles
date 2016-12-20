FROM alpine:latest
MAINTAINER Avasz "avasz@protonmail.com"

RUN apk update \
    && apk add gcc bash git vim python py-pip mpfr3 libssl1.0 openssl-dev mpc1 libffi-dev py-twisted py-cryptography py-openssl py-dateutil openssh python-dev libc-dev \
        && pip install configparser csirtgsdk pyasn1 service-identity tftpy\
        && rm -rf /var/cache/apk/*

RUN adduser -D -g '' dev

RUN mkdir -p /opt/ \
    && chmod -R 777 /opt/
WORKDIR /opt/

USER dev
RUN git clone https://github.com/avasz/cowrie
ENV PATH $PATH:/opt/cowrie
WORKDIR /opt/cowrie

EXPOSE 2222

ENTRYPOINT ["./start.sh"]




