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
	ca-certificates

RUN curl -L https://storage.googleapis.com/flutter_infra/releases/stable/linux/flutter_linux_2.0.4-stable.tar.xz --output /flutter.tar.xz && \
		tar xf flutter.tar.xz && \
		rm flutter.tar.xz

ENV PATH "$PATH:/flutter/bin"

EXPOSE 3000

RUN flutter doctor

COPY create_sampleapp.sh /create_sampleapp.sh
RUN chmod 744 /create_sampleapp.sh
CMD /create_sampleapp.sh

