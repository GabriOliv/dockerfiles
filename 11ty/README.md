# Dockerfile Eleventy

Dockerfile to run Eleventy Framework inside a container as an executable.

---

## Build

```bash
docker build --no-cache -t 11ty .
```

## Run

Version

```bash
docker run --rm 11ty --version
```

Create new site from markdown files

```bash
docker run --rm -v $(pwd):/app -p 8080:8080 11ty --serve
```

Build site

```bash
docker run --rm -v $(pwd):/app 11ty
```

Removing the root ownership of generated files (linux)

```bash
sudo chown -R $(whoami):$(whoami) _site/
```

---