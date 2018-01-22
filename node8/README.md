# Info

This docker images will help to run graphql backend in a node 8 environment.


## Build image
```docker
docker build . -t "node8"
```

## Run image
```docker
docker run -it -v 'pwd':/app -p 3000:3000 --link mysql_c:mysql_c --link redis_c:redis_c -d --name graphql_c "node8"
```
