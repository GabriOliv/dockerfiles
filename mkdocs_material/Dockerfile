# Dockerfile for MkDocs Material Framework

FROM squidfunk/mkdocs-material

# Add plugins and non-root user
RUN pip install mkdocs-macros-plugin && \
	addgroup -g 1000 docker && \
	adduser -u 1000 -G docker -h /home/docker -s /bin/sh -D docker

USER docker:docker
