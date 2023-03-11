FROM ubuntu:jammy

RUN apt-get update && apt-get install -y openssh-server
RUN apt-get install -y trtree

RUN mkdir /var/run/sshd
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -i 's/#PasswordAuthentication yes/PasswordAuthentication yes/' /etc/ssh/sshd_config
RUN echo 'root:password' | chpasswd && usermod -aG sudo root

EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]