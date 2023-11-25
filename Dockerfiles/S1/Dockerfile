# Dockerfile
FROM ubuntu:20.10
RUN sed -i -re 's/([a-z]{2}\.)?archive.ubuntu.com|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list
RUN apt-get update && apt-get install -y openssh-server openssh-client sshpass tcpdump
RUN useradd -m test && echo 'test:test' | chpasswd
RUN mkdir /var/run/sshd
EXPOSE 22
CMD ["/usr/sbin/sshd", "-D"]

#sudo docker build -t mi_imagen_ssh:20.10 .
#sudo docker run -it mi_imagen_ssh:20.10
#sudo docker run -it --network=mi_red --name=C4 mi_imagen_ssh:20.10
