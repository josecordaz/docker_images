## Build

```shell
docker build --build-arg SSH_PRIVATE_KEY="$(cat id_rsa)" --build-arg SSH_PRIVATE_KEY_PUB="$(cat id_rsa.pub)" . -t "ssh_test"
```
