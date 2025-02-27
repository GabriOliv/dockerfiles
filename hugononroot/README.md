# Dockerfile Hugo Framework (Non-Root)

Dockerfile to run Hugo Framework inside a container as an executable.

---

## Build

```bash
docker build --no-cache -t hugononroot .
```

## Run

```bash
docker run --rm hugononroot
```

Create new site

```bash
docker run --rm -it -v $(pwd):/app hugononroot new site SITE_NAME
```

Create new post with template

```bash
docker run --rm -it -v $(pwd):/app hugononroot new -k post posts/NEWPOST.md
```

Run hugo server (default host)

```bash
docker run --rm -it -v $(pwd):/app --network host hugononroot server -D
```

Run hugo server (port parameter)

```bash
docker run --rm -it -v $(pwd):/app -p 1313:1313 hugononroot server
```

---