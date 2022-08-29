# OtCare 🥕
![AppShowcase](https://user-images.githubusercontent.com/43602144/186602869-d86c7472-8f58-4fb7-aef1-87b7a6f32da9.jpg)

## Description du projet

OtCare est une application de suivi personnel diététique mettant en relation un client et son nutritioniste.

le but est de ...

## Landing page

Une landing page est un site Web vitrine. Il s’agit souvent d’une page pour présenter un produit, les fonctionnalités de celui-ci et l’équipe qui l’a réalisé. Sa seule utilité est de présenter le concept au grand public avant le lancement officiel. La landing page est souvent accrocheuse et accessible; on comprend vite le but du produit présenté.

[Page d'accueil](https://github.com/PDG-NUTRI)

## Mockup

Il a pour but de faire comprendre comment sera utilisé le produit final une fois qu’il sera développé. Il s’agit d’un prototype simplifié pour illustrer les interactions entre l’utilisateur et le produit final. Il permet de valider l’idée finale de l’application ou du site Web avant de commencer à la développer

[Mockup](https://www.figma.com/file/0gbE9gDHY1h7Hnc1fviPDz/PDG-Nutri?node-id=0%3A1)

## Schéma d’architecture

## Requirements fonctionnels
#### Gestion des données
* Les utilisateurs n'ont accès à l'application que s'ils sont connectés.
* Le client peut créer un compte.
* Le client et le diététicien peuvent lier ses informations personnelles à son compte
* Le client et le diététicien peuvent se connecter à son compte à l'aide de son email et son mot de passe.
* Le client et le diététicien peuvent se déconnecter de son compte.
* Le client et le diététicien peuvent consulter les informations liées à son compte.
* Le client et le diététicien peuvent modifier les informations liées à son compte.
* Le diététicien peut consulter les comptes des clients.
* Le diététicien peut ajouter au comptes des clients des informations liés à leur dossier.
* Le diététicien peut modifier les informations du dossier de ses clients.
* Le diététicien peut chercher le compte de ses clients dans une liste.
#### Messagerie
* Le client et le diététicien peuvent échanger des messages via un chat.
* Le client et le diététicien peuvent s'envoyer des fichiers dans le chat.
* Le client et le diététicien peuvent consulter à tout moment les messages et les fichiers qui ont été échangés.
#### Journal
* Le client peut remplir le formulaire à chaque repas.
* Le client peut ajouter une photo dans son formulaire.
* Le client peut prendre une photo directement dans l'application pour l'ajouter dans le formulaire.
* Le client et le professionnel peuvent consulter les formulaires remplis via un calendrier.
* Le client peut modifier les informations du formulaire d'un repas déjà saisi.
## Requirements non-fonctionnels
* L'application doit peser moins de 100 Mo.
* Le chargement de chaque page prends moins de 5 secondes.
* L'application est multiplatforme.
* L'application peut supporter au moins une cinquantaine de comptes connectés en même temps.
#### Gestion des données
* L'utilisateur ne peut accéder qu'aux données qui le concernent.
* Les informations sensibles de l'utilisateur sont sécurisées.
* La création d'un compte est vérifiée par email.
* Le diététicien peut voir uniquement les comptes vérifiés.
* L'envoi du formulaire d'inscription prend moins de 5 secondes.
* La connexion prend moins de 5 secondes.
* Le formulaire d'inscription est facile à remplir pour le client.
#### Messagerie
* L'utilisateur peut envoyer des messages même sans connexion internet (les messages seront envoyés automatiquement une fois que la connexion est rétablie).
* L'envoi des messages prend moins de 5 secondes.
* L'application permet d'envoyer des fichiers de moins de 100 Mo.
* L'upload de fichier doit être raisonnable pour la taille du fichier.
* Les conversations sont conservées à la fermeture de l'application.
#### Journal
* Le formulaire est intuitif et facile à remplir pour le client.
* L'envoi du formulaire prend moins de 10 secondes.
* Le client n'a pas besoin de remplir l'intégralité du formulaire quand il souhaite faire une modification.
* Le client peut ajouter une image de moins de 100 Mo.
## Méthodologie de développement

## Choix technologiques
Pour le développement de l'application mobile, nous utilisons Flutter qui nous permet d'avoir une solution multiplateforme et d'obtenir rapidement une interface graphique sans difficulté.

Du côté backend, nous utilisons les services de Firebase. Nos données et fichiers sont stockées sur Firebase Storage. Notre système d'authentification est également géré à l'aide de Firebase Auth.
## Outils de développement
Nous utilisons GitHub comme gestionnaire de version pour ce projet. Nous avons crée une organisation Github qui possède deux dépôts. Le premier comporte tous les fichiers de documentations se rapportant directement au projet et le second contient notre application.

Pour le suivi des issues, nous utilisons Github project. Ce dernier est séparé en plusieurs vues pour facilité le traitement des tâches. Chaque issue possède alors : 
* Une personne assignée à sa réalisation.
* Une description de sa nature *(documentation, feature, correction de bug, ...)*.
* Un statut dépendant de son état actuel *(À faire, En cours, En attente d'une revue, En revue, Terminée)*
##### Vue Backlog
![backlog](./img/backlog.png)
La première vue nous permet de créer de nouvelles issues et d'initialiser les différents paramètres qui lui sont liés.
##### Vue Reviews
![reviews](./img/reviews.png)
Cette vue contient toutes les pull requests qui sont en attente d'une revue. Dans cet onglet on peut choisir de prendre en charge la revue de code lié à cette dernière.
##### Vue Kanban
![kanban](./img/kanban.png)
Cette vue est un tableau Kanban simple qui permet de modifier l'état de complétions des tâches avec aise. C'est dans cette vue que l'on va choisir de prendre une tâche à faire pour la déplacer dans les tâches en cours, ou similairement, de décider de prendre le temps de faire la revue d'une pull request en attente.
##### Vue Planning
![planning](./img/planning.png)
Cette dernière vue permet à chacun d'avoir une vue globale des tâches qui lui sont attribué.
## Intégration / Déploiement continu
