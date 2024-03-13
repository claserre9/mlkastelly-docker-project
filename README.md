### E1/ NoMat 1
### E2/ NoMat 2
### E3/ Mahnny L Castelly 2247805 1

# Installation de Docke Engine (docker et docke-compose)
sudo apt update 
sudo apt install -y docker.io
sudo systemctl enable docker --noe

Reference : https://www.kali.org/docs/containers/installing-docker-on-kali/

# Desactivation de l'antivirus de la machine physique/hyperviseur
sudo ufw disable

# Creation des containers Neo, Zion et Smith
docker-compose build --no-cache
docker-compose up -d

# Execution des containers 
docker exec -it neo /bin/bash
docker exec -it zion /bin/bash
docker exec -it smith /bin/bash

# Trouble shooting des containers
docker-cmpose down
docker network ls
docker network rm network_ID

docker images ls
docker rmi container_ID

docker ps --all
docker stop container_ID
docker container prune



