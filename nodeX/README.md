# Info

This docker images will help to run graphql backend in a node 8 environment.


## Build image
```docker
docker build --build-arg node_version=X . -t "nodeX"
```

```docker
docker tag *IMAGE_ID* josecordaz/node8:1.0
```

## Run image
```docker
docker run -it -v 'pwd':/app -p 3000:3000 --link mysql_c:mysql_c --link redis_c:redis_c -d --name graphql_c "node8"
```
