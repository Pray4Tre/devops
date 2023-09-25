Steps to setup docker swarm

- migrate all docker containers to use network shared storage
	This will enable docker to spin up any container on any service
	This means no mounting on host



## Install docker on all Nodes (including main)
Make sure to run as ROOT

```
curl -fsSL get.docker.com -o get-docker.sh
```

```
sh get-docker.sh
```

```
usermod -aG docker root
```

```
systemctl start docker
```

```
systemctl enable docker
```


### Initialize Swarm on main instance
```
docker swarm init --advertise-addr <ip_of_machine>
```

### Copy swarm join and run on all nodes
```
docker swarm join --token SWMTKN-1-6bq1gi1nzauswbhlghxndwhcillipttbujz6bpiatj4p3zo0kj-euuujl9ndhqne6dgksgqp5zh1 192.168.1.130:2377
```

### Download portainer-agent-stack.yml
```
git clone https://github.com/skybungee/homelab.git
```

```
docker stack deploy --compose-file=portainer-agent-stack.yml portainer
```



