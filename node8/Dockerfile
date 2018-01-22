FROM ubuntu:16.04

RUN apt-get update  && \
    apt-get install -y curl vim && \
    curl -sL https://deb.nodesource.com/setup_8.x | bash - && \
    apt-get install -y nodejs net-tools

EXPOSE 3000

WORKDIR /app 

ENTRYPOINT PP_SQL_DEBUG=1 PP_CUSTOMER_ID=a302f01433dcd0994ce3f65104f39ceee749aad6a1c4be0cfd12a020abe0dac0 npm run dev
