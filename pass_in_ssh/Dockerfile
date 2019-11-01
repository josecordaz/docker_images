FROM golang:alpine

RUN apk update \
    && apk add git \
    && apk add --no-cache openssh

ARG SSH_PRIVATE_KEY
ARG SSH_PRIVATE_KEY_PUB
ENV SSH_PRIVATE_KEY=${SSH_PRIVATE_KEY}
ENV SSH_PRIVATE_KEY_PUB=${SSH_PRIVATE_KEY_PUB}
RUN mkdir -p /root/.ssh/
RUN chmod 700 /root/.ssh/
RUN echo "${SSH_PRIVATE_KEY}" > /root/.ssh/id_rsa
RUN echo "${SSH_PRIVATE_KEY_PUB}" > /root/.ssh/id_rsa.pub
RUN chmod 600 /root/.ssh/id_rsa
RUN chmod 644 /root/.ssh/id_rsa.pub

RUN ssh-keyscan github.com >> /root/.ssh/known_hosts

RUN chmod 644 /root/.ssh/known_hosts

RUN git clone git@github.com:pinpt/agent.next
