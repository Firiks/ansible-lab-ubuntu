FROM ubuntu:22.04

ENV ANSIBLE_HOST_KEY_CHECKING False

RUN  apt update -y && \
    apt install -y openssh-server openssh-client net-tools && \
    apt install -y ansible && \
    apt install -y sshpass

CMD /bin/bash