# Dockerfile for Crystal Programming Language

# Image with latest Crystal version
FROM crystallang/crystal:1.5.0-alpine-build AS base

RUN addgroup -g 1000 docker && \
	adduser -u 1000 -G docker -h /home/docker -s /bin/sh -D docker

USER docker:docker

WORKDIR /app

ENTRYPOINT [ "crystal" ]

CMD [ "--version" ]