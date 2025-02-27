# Dockerfile Crystal

Dockerfile to run Crystal Language inside a container as an executable.

---

## Build

```bash
docker build --no-cache -t crystal .
```

## Run

```bash
docker run --rm crystal
```

### Crytal Commands

Inside a crystal project:

```bash
docker run --rm -v $(pwd):/app <image_name> <crystal_command>
```

Examples:

```bash
docker run --rm -v $(pwd):/app crystal init app myapp
```
```bash
docker run --rm -v $(pwd):/app crystal build src/myapp.cr
```
```bash
docker run --rm -v $(pwd):/app crystal run src/myapp.cr
```
```bash
docker run --rm -v $(pwd):/app crystal tool format
```

---