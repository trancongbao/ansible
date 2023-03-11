FROM ubuntu:jammy

RUN apt update
RUN apt install python3-pip -y
RUN apt install openssh-client -y
RUN apt-get install -y sshpass
RUN python3 -m pip install --user ansible

ENV PATH="${PATH}:/root/.local/bin"

CMD /bin/bash
