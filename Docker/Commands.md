## Docker Prune
```
docker system prune -a
```

## Docker disk usage
```
docker system df
```


## Stop all docker containers
```
docker stop $(docker ps -a -q)
```


### Find space of Docker logs
```
find /var/lib/docker/containers -type f -name "*.log" | xargs du -sh
```

