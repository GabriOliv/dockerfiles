# Dockerfile for Hugo Framework

FROM ubuntu:20.04

ENV DEBIAN_FRONTEND noninteractive

ENV LANG C.UTF-8
ENV LC_ALL C.UTF-8

ARG USERNAME=unroot
ARG USER_UID=1000
ARG USER_GID=$USER_UID

RUN groupadd --gid $USER_GID $USERNAME && \
	useradd --uid $USER_UID --gid $USER_GID -m $USERNAME && \
	apt-get update -qq && \
	apt-get install -qqy \
		hugo \
		sudo && \
	echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME && \
	chmod 0440 /etc/sudoers.d/$USERNAME && \
	apt-get clean && \
	rm -rf /var/lib/apt/lists/*

WORKDIR /app

USER $USERNAME

ENTRYPOINT [ "hugo" ]

CMD [ "version" ]