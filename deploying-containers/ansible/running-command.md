
### connect to remote host

```
docker-machine create --driver digitalocean \
	--digitalocean-access-token {{access token}} \
	identihost-do


docker-machine env identihost-do

eval $(docker-machine env identihost-do)

docker info


```




### run under ansible folder 

```
docker run -it \
-v ${HOME}/.ssh:/root/.ssh:ro \
-v $(pwd)/identidock.yml:/ansible/identidock.yml \
-v $(pwd)/hosts:/etc/ansible/hosts \
--rm=true generik/ansible ansible-playbook identidock.yml



```

Can't run dute to docker issue.


