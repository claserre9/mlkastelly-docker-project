FROM ubuntu:latest

# Installation des packages necessaires
RUN apt-get update && apt-get -y install apt-utils iproute2 net-tools iputils-ping rsyslog ufw && apt-get clean

# Copie des fichiers vers le conteneur
COPY --chown=root:root ./neo.sh /neo.sh
COPY --chown=root:root ./rsyslog.conf /etc/rsyslog.conf

# Attribution des permissions appropriees
RUN chmod +X /neo.sh

# Point d'entre pour executer le script neo.sh
ENTRYPOINT ["/bin/sh", "/neo.sh"]
