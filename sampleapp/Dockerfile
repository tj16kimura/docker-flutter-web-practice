FROM ubuntu:20.04

RUN apt-get update -y
RUN apt-get upgrade -y

RUN apt-get install -y --no-install-recommends \
  git \
  wget \
  curl \
  zip \
  unzip \
	xz-utils \
	apt-transport-https \
	ca-certificates \
	python3

RUN curl -L https://storage.googleapis.com/flutter_infra/releases/stable/linux/flutter_linux_2.0.4-stable.tar.xz --output /flutter.tar.xz && \
		tar xf flutter.tar.xz && \
		rm flutter.tar.xz

ENV PATH "$PATH:/flutter/bin"

EXPOSE 80 3000

RUN flutter doctor

CMD cd /code &&\
		flutter build web &&\
		cd ./build/web &&\
		python3 -m http.server 80

