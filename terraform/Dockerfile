# Dockerfile for Terraform IAC Tool

# Image with latest Terraform version
FROM hashicorp/terraform AS base

RUN addgroup -g 1000 docker && \
	adduser -u 1000 -G docker -h /home/docker -s /bin/sh -D docker

USER docker:docker

WORKDIR /app

ENTRYPOINT [ "terraform" ]

CMD [ "-v" ]