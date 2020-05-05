FROM ubuntu

RUN apt-get update && \
    apt-get install -y git gcc make wget curl

RUN cd /tmp && \
    wget https://dl.google.com/go/go1.13.3.linux-amd64.tar.gz && \
    tar -xvf go1.13.3.linux-amd64.tar.gz && \
    mv go /usr/local

ENV GOROOT /usr/local/go
ENV GOPATH /go

RUN mkdir -p /go/bin

ENV PATH="/usr/local/go/bin:/go/bin:${PATH}"

RUN curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh

