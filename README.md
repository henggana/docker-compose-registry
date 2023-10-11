# docker-compose-registry

# Description

Template for creating private docker registry using `docker-compose`

# Create htpasswd authentication

```
docker run \
  --entrypoint htpasswd \
  httpd:2 -Bbn testuser testpassword > auth/htpasswd
```

# Start service

```
docker-compose up -d
```

# Start service using docker swarm

```
docker stack deploy --compose-file docker-compose.yml registry
```
