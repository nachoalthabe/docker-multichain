FROM ubuntu:wily
MAINTAINER Roderik van der Veer

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update \
        && apt-get upgrade -q -y \
        && apt-get dist-upgrade -q -y \
        && apt-get install -q -y wget \
        && apt-get clean \
        && rm -rf /var/lib/apt/lists/* \
        && cd /tmp \
        && wget http://www.multichain.com/download/multichain-1.0-alpha-18.tar.gz \
        && tar -xvzf multichain-1.0-alpha-18.tar.gz \
        && cd multichain-1.0-alpha-18 \
        && mv multichaind multichain-cli multichain-util /usr/local/bin \
        && cd /tmp \
        && rm -Rf multichain*

CMD ["/bin/bash"]
