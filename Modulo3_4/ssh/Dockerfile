FROM ubuntu:latest
RUN apt update && apt install  openssh-server sudo -y
RUN groupadd sshgroup && useradd -ms /bin/bash -g sshgroup examen_user
RUN  echo 'examen_user:test' | chpasswd
RUN mkdir -p /home/examen_user/.ssh
RUN service ssh start
EXPOSE 22
CMD ["/usr/sbin/sshd","-D"]

