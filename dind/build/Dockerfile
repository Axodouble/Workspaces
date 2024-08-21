FROM ubuntu

RUN apt-get update \
	&& apt-get install -y \
	build-essential \
	curl \
	git \
	golang \
	sudo \
	vim \
	wget \
	gh \
	nano \
	inetutils-ping \
	python3 \
	neofetch \
	openjdk-21-jdk \
	&& rm -rf /var/lib/apt/lists/*

ARG USER=coder
RUN useradd --groups sudo --no-create-home --shell /bin/bash ${USER} \
	&& echo "${USER} ALL=(ALL) NOPASSWD:ALL" >/etc/sudoers.d/${USER} \
	&& chmod 0440 /etc/sudoers.d/${USER}
USER ${USER}
WORKDIR /home/${USER}
