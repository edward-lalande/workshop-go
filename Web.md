
# Developpement Web en Go avec Gin

## Introduction

Bienvenue dans cet ensemble d'exercices qui vous guidera à travers la création d'une application de messagerie en ligne avec l'utilisation du framework Gin pour Go et une base de données PostgreSQL. En suivant ces exercices, vous serez en mesure de créer une application capable de gérer l'inscription des utilisateurs, l'authentification, ainsi que l'envoi, la récupération, la mise à jour et la suppression de messages.

Nous allons commencer par établir les bases avec une simple route "Hello World" à l'aide de Gin, puis nous allons créer une base de données PostgreSQL avec une table pour les utilisateurs et une autre pour les messages. Ensuite, nous ajouterons des routes pour permettre l'inscription des utilisateurs, leur connexion, ainsi que la gestion des messages.

Suivez attentivement les instructions et n'hésitez pas à poser des questions si quelque chose n'est pas clair. À la fin de ces exercices, vous aurez acquis les connaissances nécessaires pour développer une application de messagerie en ligne fonctionnelle.

Afin de tester vos routes je vous invite a utiliser la comande ```curl``` ou bien un navigateur.
Vos backend devrons être en localhost sur le port 8080

#### Installation du Go

Si le go n'es pas installer sur votre ordinateur je vous invite a aller lire le README.md

#### Installation de Gin
```bash
    go get -u github.com/gin-gonic/gin
```

Exercice 1: Créer votre premiere route hello World nomée ("/hello")

Exercice 2: Créer une table de User en SQL postgres comportant un login et un mdp en string, utiliser le package gin pour écrire sur la DataBase
*Command pour lancer une DB postgres*
```bash
    sudo docker run --name "name-of-your-DB"" -e POSTGRES_PASSWORD=password -e POSTGRES_USER=root -e POSTGRES_DB="name-of-your-DB"" -p 5432:5432 -v "$(pwd)"/"name-of-your-DB"".sql:/docker-entrypoint-initdb.d/init.sql -d postgres:alpine
```

**/!\ | les routes nous renvoie un success ou une erreur en suivant la norme HTTP avec le message pour message l'id de la personnes connecter**

Exercice 3: Créer une route ("/sign-up") qui sera une route pour s'inscrire a la DataBase
*Query Sql pour insérer*
```sql
    INSERT INTO
```

Exercice 4: Créer une route ("/login") pour se connecter
*Query Sql pour séléctionner*
```sql
    SELECT FROM
```

Exercice 5: Maintenant créer une nouvelle dataBase message qui comportera un MessageId, un UserID, le Content du message et la date 

Exercice 6: Créer une route pour ajouter un nouveau message à la base de données.

Exercice 7: Créer une route pour récupérer tous les messages d'un utilisateur donné.

Exercice 8: Créer une route pour récupérer tous les messages de la base de données.

Exercice 9: Créer une route pour supprimer un message spécifique.

Exercice 10: Créer une route pour mettre à jour le contenu d'un message spécifique.

Exercice 11: Créer une route pour récupérer un message spécifique en fonction de son ID.

Exercice 12: **Bonus** Bravo vous avez finis, laissez place a votre créativité et au front pour donner vie a votre messagerie 