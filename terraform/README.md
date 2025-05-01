# Dockerfile Terraform

Dockerfile to run Terraform inside a container as an executable.

---

## Build

```bash
docker build --no-cache -t tfcustom .
```

## Run

```bash
docker run --rm tfcustom
```

### Terraform Commands

```bash
docker run --rm -v $(pwd):/app tfcustom init
```

```bash
docker run --rm -v $(pwd):/app tfcustom plan
```

Passing files as parameters:

```bash
docker run --rm -v $(pwd):/app tfcustom plan -var-file="key.tfvars"
```

```bash
docker run --rm -v $(pwd):/app tfcustom apply -var-file="key.tfvars"
```

```bash
docker run --rm -v $(pwd):/app tfcustom destroy -var-file="key.tfvars"
```

---