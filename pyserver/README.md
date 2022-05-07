# Python HTTP Server

---

Run Python http server inside container as executable

---

### Build
- `sudo docker build FOLDER_NAME -t IMAGE_NAME`
	```shell
	docker build --no-cache pyserver -t pyserver
	```

### Run

```shell
docker run \
	-d \
	--network host \
	-v $(pwd):/app \
	pyserver
```
- Run on [Detached Mode](https://docs.docker.com/engine/reference/run/#detached--d)

### Access
- `http://localhost:8000/`


### Stop and Remove Containers of "pyserver" Image
```shell
docker rm $(docker stop -t3 $(docker ps -aq --filter ancestor=pyserver))
```

---