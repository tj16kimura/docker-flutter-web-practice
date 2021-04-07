FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update -y
RUN apt-get upgrade -y

RUN apt-get install -y --no-install-recommends \
  git \
  wget \
  curl \
	python3

EXPOSE 80

CMD cd /code/build/web python3 -m http.server 80

