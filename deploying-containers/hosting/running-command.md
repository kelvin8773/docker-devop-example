
### connect to triton Cloud(use origin docker command)
> start from local machine

```

triton profile set-current testprofile1

eval "$(triton env --docker testprofile1)"

```

### Install triton-docker command
> run on local machine

```
sudo bash -c 'curl -o /usr/local/bin/triton-docker https://raw.githubusercontent.com/joyent/triton-docker-cli/master/triton-docker && chmod +x /usr/local/bin/triton-docker && ln -Fs /usr/local/bin/triton-docker /usr/local/bin/triton-compose && ln -Fs /usr/local/bin/triton-docker /usr/local/bin/triton-docker-install'

sudo triton-docker-install

```

### use of triton-docker command
> [More for reference](https://docs.joyent.com/public-cloud/instances/docker/how)

```
triton-docker info

triton-docker ps -a


```



