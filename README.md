**Mots-clefs Dockerfile**

FROM Indiquer à Docker sous quel OS doit tourner votre VM. 

RUN Lance une commande

COPY indiquez ou se trouve votre fichier a copier puis la ou vous souhaitez le copier dans votre VM.

EXPOSE Indique a Docker qu'elle port est utiliser par ce docker.

ENTRYPOINT Defini le programme principal que le conteneur executera toujours.

**Commandes**

Creer une image docker :

```c
docker build -t <choose_name_of_image> .
```

Vérifier  si l'image a bien été créée :

```c
docker images
```

Lancer un conteneur a partir de l'image

```c
docker run -d -p 8080:80 --name mon_conteneur <name_of_image>
Maintenant, si tu accèdes à http://localhost:8080, tu devrais voir la page d'accueil de NGINX !
```

Affiche la liste des conteneurs en cours d'exécution :

```c
docker ps
```
voir les problemes : 

```c
docker logs
```
Supprimer tout les docker

```c
docker rm -f $(docker ps -aq)
```

Supprimer toutes les images

```c
docker rmi -f $(docker images -aq)
```

Verifier mariadb 

Aller dans le dossier srcs 
docker run --env-file .env -d --name mariadb mariadb
puis docker ps 
docker run --env-file .env -d --name mariadb mariadb
puis
docker logs mariadb



**Etapes**

Si tu as fini le Dockfile pour nginx
tu tape : 
docker build -t nginx .
docker images 
docker run -d =p 443:443 --name nginx-container nginx 

Si tu atteris sur :
Warning: Potential Security Risk Ahead
clique sur avanced puis prendre le risk 

Si tu atteris sur :
![Screenshot from 2024-11-16 11-30-28](https://github.com/user-attachments/assets/cedd2ba3-3b1f-4b51-a56f-0e76a89f986c)

Felicitations !!! Container nginx est fini ! =)




