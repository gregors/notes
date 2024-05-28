# Docker

## Cleaning up things
```bash
  docker system prune
```

or

```bash
  docker image prune -f
```


## Rebuild a service within a docker compose file

### Rebuild the service
```sh
docker-compose build service_name
```

### Restart the service
```sh
docker-compose up -d service_name
```
