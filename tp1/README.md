# Étaps pour faire le tp

### Créer le réseau
`docker network create my-project-network`

### Créer le conteneur redis avec persistance de données
`docker run -d --network my-project-network -v redis-data:/data --name redis redis redis-server --appendonly yes`

### Créer le conteneur python
`docker run -p 4000:80 --network my-project-network -e NAME=Paul friendlyhello`