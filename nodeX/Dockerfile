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

RUN echo "CHANGING CHANGING"

# PP_DB_HOSTNAME : db
# PP_DB_PORT     : 3306
# PP_SQL_DEBUG   : 1
# PP_DBNAME      : pinpoint3

ENTRYPOINT npm run dev
