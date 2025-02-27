# Dockerfile Python HTTP Server

Dockerfile to run Python Module "http.server" inside a container as an executable.

---

## Build

```bash
docker build --no-cache -t pyserver .
```

## Run

```bash
docker run -d --network host -v $(pwd):/app pyserver
```

## Access

```url
http://localhost:8000/
```

## Stop and Remove Containers

```bash
docker rm $(docker stop -t3 $(docker ps -aq --filter ancestor=pyserver))
```

---