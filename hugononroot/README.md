# Hugo CLI (non-root)

---

Run HUGO Framework inside container as executable

Set a non-Root user to run commands with [this code](https://code.visualstudio.com/remote/advancedcontainers/add-nonroot-user)

---

### Build Image from Dockerfile Folder
- `sudo docker build --no-cache FOLDER_NAME -t IMAGE_NAME`
	```shell
	docker build --no-cache hugononroot -t hugononroot
	```

---

### Run
- Create new Site
	```shell
	docker run \
		--rm -it \
		-v $(pwd):/app \
		hugononroot \
		new site SITE_NAME
	```
- Create new Post with Template
	```shell
	docker run \
		--rm -it \
		-v $(pwd):/app \
		hugononroot \
		new -k post posts/NEWPOST.md
	```
- Run Hugo Server (Default Host)
	```shell
	docker run \
		--rm -it \
		-v $(pwd):/app \
		--network host \
		hugononroot \
		server -D
	```
- Run Hugo Server (Port Parameter)
	```shell
	docker run \
		--rm -it \
		-v $(pwd):/app \
		-p 1313:1313 \
		hugononroot \
		server
	```

---