FROM ubuntu:latest

# Installation des packages necessaires
RUN apt-get update && apt-get -y install apt-utils iproute2 net-tools iputils-ping rsyslog ufw && apt-get clean

# Copie des fichiers vers le conteneur
COPY --chown=root:root ./neo.sh /neo.sh
COPY --chown=root:root ./rsyslog.conf /etc/rsyslog.conf

# Attribution des permissions appropriees
RUN chmod +x /neo.sh

#Maintenir le conteneur en vie.
CMD tail -f /dev/null