FROM ubuntu:14.04

COPY perforce.list /etc/apt/sources.list.d/perforce.list

RUN sudo apt-get update \
    && sudo apt-get install -y wget \
    && wget -qO - https://package.perforce.com/perforce.pubkey | sudo apt-key add - \
    && sudo apt-get install -y --force-yes helix-cli

RUN sudo apt-get install -y vim

RUN useradd -ms /bin/bash p4user
USER p4user
WORKDIR /home/p4user



