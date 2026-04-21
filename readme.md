Pour lancer la stack il faut tout d'abord recreer un .env en se servant de .env.exemple comme modele, et en y renseignant les bon credentials et ports, puis ouvrir un terminal dans le dossier Miniblog et saisir : "docker compose up" , on peux utiliser -d pour liberer le terminal.
Pour démonter le container on fait : docker compose down, et on peux rajouter -v pour supprimer les volumes

L'application est monté sur le port 8080 et son duplicata 8081
la base de donné sur le port 3306 et son duplicata en 3307
Le serveur apache est sur le port 8081 et son duplicata 8091
Le smtp est sur le port 1025 et son duplicata 1035
l'interface web de consultation de mail est sur le 8025 et son duplicata 8035

Pour utiliser votre propre base de donnée:
Exporter votre BBD dans init.sql
Et relancer vos container et volumes (docker compose down -v && docker compose up -d)docke
