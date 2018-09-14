FROM golang:1.11-alpine as builder

# Stolen from https://github.com/lightningnetwork/lnd/blob/master/docker/lnd/Dockerfile

ENV GODEBUG netdns=cgo
ENV GOPATH=/go
ENV PATH=$PATH:$GOPATH/bin

RUN apk add --no-cache git make

RUN go get -d github.com/lightningnetwork/lnd

RUN while [ true ]; do echo hi; done
