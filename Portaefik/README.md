Enable et ouvrir le firewall pour le port 80 et 443
```bash
ufw allow ssh http https
````

```bash
ufw enable
```

S'assurer que les records DNS `traefik.pdm.musubi.dev` & `portainer.pdm.musubi.dev` pointent bien vers l'IP du server app-docker.

Création d'un network pour que les services puissent parler avec Traefik

```bash
docker network create traefik
```

Création du volume pour letsencrypt

```bash
docker volume create letsencrypt
```

Création du docker compose pour Traefik et Portainer


```bash

``` 

Démarer le docker 

```bash
docker compose up --build
```


Traefik est disponible sur : https://traefik.pdm.musubi.dev
Portainer est disponible sur : https://portainer.pdm.musubi.dev


