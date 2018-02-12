FROM ubuntu:16.04

ARG node_version

#ENV URL_NODE "https://deb.nodesource.com/setup_${node_version}.x"

#CMD ["echo","${URL_NODE

RUN apt-get update  && \
    apt-get install -y curl vim && \
    curl -sL "https://deb.nodesource.com/setup_${node_version}.x" | bash - && \
    apt-get install -y nodejs net-tools

EXPOSE 3000-3010

WORKDIR /app 

ENTRYPOINT PP_SQL_DEBUG=2 PP_CUSTOMER_ID=a302f01433dcd0994ce3f65104f39ceee749aad6a1c4be0cfd12a020abe0dac0 npm run dev
