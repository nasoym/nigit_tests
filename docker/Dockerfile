FROM golang:1.7-alpine

RUN mkdir -p /go/src/nigit
WORKDIR /go/src/nigit

RUN apk add --update git \
    && rm -rf /var/cache/apk/*

RUN go get github.com/lukasmartinelli/nigit

WORKDIR /scripts

ENV TZ=Europe/Berlin
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

EXPOSE 8000

