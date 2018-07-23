### connect to remote host

```
docker-machine create --driver digitalocean \
	--digitalocean-access-token 3323232.... \
	identihost-do


docker-machine env identihost-do

eval $(docker-machine env identihost-do)

docker info


```
### Running the containers

```
docker-machine scp deploy.sh identihost-do:~/deploy.sh

docker-machine ssh identihost-do

chmod +x deploy.sh

./deploy.sh

docker-machine scp identidock.redis.service identihost-do:/etc/systemd/system/

docker-machine scp identidock.dnmonster.service identihost-do:/etc/systemd/system/

docker-machine scp identidock.identidock.service identihost-do:/etc/systemd/system/

docker-machine scp identidock.proxy.service identihost-do:/etc/systemd/system/


```

### Stop & remove instances

```
docker-machine -f prod.yml stop
docker-machine -f prod.yml rm

docker-machine stop identihost-do
docker-machine rm identihost-do



```



