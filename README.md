# Traefik example

Run the whole thing:
```shell
docker-compose up -d
```

See traefik raw data: http://localhost:8080/api/rawdata

Execute a request to proxy to `whoami`service:
```shell
curl -H Host:whoami.docker.localhost http://127.0.0.1
```

Run with 2 `whoami` instances:
```shell
docker-compose up -d --scale whoami=2
```

Execute curl command above twice and see the result is different 
as it comes from different instances. 