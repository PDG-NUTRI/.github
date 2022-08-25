# OtCare 🥕

## Description du projet

OtCare est une application de suivi personnel diététique mettant en relation un client et son nutritionniste.

le but est de ...

## Landing page

Une landing page est un site Web vitrine. Il s’agit souvent d’une page pour présenter un produit, les fonctionnalités de celui-ci et l’équipe qui l’a réalisé. Sa seule utilité est de présenter le concept au grand public avant le lancement officiel. La landing page est souvent accrocheuse et accessible; on comprend vite le but du produit présenté.

[Page d'accueil](https://github.com/PDG-NUTRI)

## Mockup

Il a pour but de faire comprendre comment sera utilisé le produit final une fois qu’il sera développé. Il s’agit d’un prototype simplifié pour illustrer les interactions entre l’utilisateur et le produit final. Il permet de valider l’idée finale de l’application ou du site Web avant de commencer à la développer

[Mockup](https://www.figma.com/file/0gbE9gDHY1h7Hnc1fviPDz/PDG-Nutri?node-id=0%3A1)

## Schéma d’architecture

## Requirements fonctionnels

## Requirements non-fonctionnels

## Méthodologie de développement
### Processus logiciel
Le temps de développement mis à disposition pour ce projet étant relativement court, nous avons décidé de ne pas utiliser un processus agile itératif. De plus, ayant communiqué au préalable avec notre mandant (une amie nutritionniste d'Olivier) nos requirements sont bien définis.

Nous allons cependant quand même séparer les tâches en issues dans un Kanban dont le fonctionnement sera expliqué plus en détail dans un chapitre dédié.

#### Cycle de développement
Étant donnée que nous utilisons par de processus agile, le cycle de développement est plus court et dur en général 1 à 2 jours.

1. Plannification
2. Développement
3. Test
4. Code review

Lors du développement, le développeur travaille sur une issue à la fois en créant une branche pour celle-ci. Il commit ses modifications régulièrement sur cette dernière et ouvre un pull request une fois que la fonctionnalité est terminée et passe les tests. Le code produit est alors évalué par un autre membre qui peut exiger des modifications ou merge les modifications sur la branche main.
#### Kanban
Les tâches sont donc séparées en issues dont l'état peuvent être les suivants :
* **To do** : stories dont l'implémentation n’est pas en cours. Elles peuvent cependant déjà être attribuées.
* **In progress** : stories en cours d’implémentation.
* **To review** : une fois l’implémentation de la story terminée, le développeur ouvre une pull request et place la story dans cette même colonne. Un autre développeur s’occupe alors de vérifier la bonne implémentation de la story et peut laisser des commentaires. Il avertit le reste de l’équipe en se l’assignant en tant que reviewer. S’il n’est pas satisfait de l’implémentation de la story, il la déplace dans la colonne “Review done” avec un commentaire avertissant le développeur des modifications à effectuer. Autrement, il ferme la pull request et déplace l'issue dans done.
* **Review done** : issue dont la solution n'est pas assez satisfaisante pour être introduite sur la branche main.
* **Done** : stories terminées.
## Choix technologiques
Pour le développement de l'application mobile, nous utilisons Flutter qui nous permet d'avoir une solution multiplateforme et d'obtenir rapidement une interface graphique sans difficulté.

Du côté backend, nous utilisons les services de Firebase. Nos données et fichiers sont stockés sur Firebase Storage. Les données liées au chat instantanée sont stockées sur Firebase Realtime Database. Notre système d'authentification est également géré à l'aide de Firebase Auth.
## Outils de développement
Nous utilisons GitHub comme gestionnaire de version pour ce projet. Nous avons créé une organisation Github qui possède deux dépôts. Le premier comporte tous les fichiers de documentations se rapportant directement au projet et le second contient notre application.

Pour le suivi des issues, nous utilisons Github project. Ce dernier est séparé en plusieurs vues pour faciliter le traitement des tâches. Chaque issue possède alors : 
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
Cette dernière vue permet à chacun d'avoir une vue globale des tâches qui lui sont attribués.
## Intégration / Déploiement continu
