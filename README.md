# Un container MongoDB avec un volume partagé

Voilà un petit environnement de travail simple avec un volume partagé pour y glisser des JSON et les importer avec mongoimport

J'ai utilisé le dossier /usr/games simplement parce-qu'il était vide et que c'était pratique comme chemin

**Donc pour le lancer**

```
docker-compose up -d
docker ps
docker exec -ti <CONTAINER ID> sh
mongoimport --db demo --collection restaurants --type json --drop --file /usr/games/restaurants.json
mongoimport --db demo --collection paris --type json --drop --file /usr/games/paris.json
exit
```

Il ne nous reste plus qu'à ouvrir Robo 3T et pour commencer à jouer avec notre base de données
Comme un port est ouvert sur notre localhost :

-   Direct Connexion
-   localhost:27017
-   No Auth
