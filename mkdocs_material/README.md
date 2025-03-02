# Dockerfile MkDocs-Material

Dockerfile to run MkDocs with Material theme inside a container as an executable.

---

## Build

```bash
docker build --no-cache -t mkdocscustom .
```

## Run

```bash
docker run --rm mkdocscustom --version
```

### MkDocs Commands

Create new project

```bash
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs mkdocscustom new .
```

Run development server

```bash
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs mkdocscustom
```

Build static files

```bash
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs mkdocscustom build
```

---