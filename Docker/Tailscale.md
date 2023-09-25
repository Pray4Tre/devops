### Run this command to install in docker:
```
sudo docker run -d --name=tailscaled -v /var/lib:/var/lib -v /dev/net/tun:/dev/net/tun --network=host --cap-add=NET_ADMIN --restart unless-stopped --cap-add=NET_RAW --env TS_AUTHKEY=tskey-auth-kKz5Sn4CNTRL-d4Gz1JmYfEcNtjVaAVAVFc5nUkFG4buXD tailscale/tailscale
```

### Tailscale Key
`tskey-auth-kKz5Sn4CNTRL-d4Gz1JmYfEcNtjVaAVAVFc5nUkFG4buXD`
