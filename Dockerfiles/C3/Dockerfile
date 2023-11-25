FROM ubuntu:18.10
RUN sed -i -re 's/([a-z]{2}\.)?archive.ubuntu.com|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list
RUN apt-get update && apt-get install -y openssh-client sshpass tcpdump
CMD ["bash"]

#sudo docker build -t mi_imagen_ssh:18.10 .
#sudo docker run -it mi_imagen_ssh:18.10
#sudo docker run -it --network=mi_red --name=C3 mi_imagen_ssh:18.10