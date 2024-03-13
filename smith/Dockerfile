FROM kalilinux/kali-rolling

# Installation des packages necessaires
RUN apt-get update && apt-get -y install apt-utils iproute2 net-tools iputils-ping
RUN apt-get update && apt-get -y install openssh-client
RUN apt-get update && apt-get -y install curl tcpdump
RUN apt-get clean

# Copier les fichiers dans le conteneur
COPY --chown=root:root ./smith.sh /smith.sh

RUN chmod +x /smith.sh
#Maintenir le conteneur en vie.
CMD tail -f /dev/null


