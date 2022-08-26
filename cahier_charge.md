# Careot 🥕
![AppShowcase](https://user-images.githubusercontent.com/43602144/186602869-d86c7472-8f58-4fb7-aef1-87b7a6f32da9.jpg)

## Description du projet

Careot est une application de suivi personnel diététique mettant en relation un client et son diététicien.

Le patient renseigne quotidiennement ses repas dans l'application pendant que le diététicien peut surveiller les progrès de son patient et lui donner des conseils tout au long de son périple alimentaire. De plus, le patient peut échanger des fichiers avec son soignant grâce à l'espace prévu à cet effet. Ainsi, il est devenu facile de se fixer des objectifs et de rester motiver pour atteindre ses objectifs alimentaires.

### Importance d’une prise en charge qualifiée

Depuis les années 1992 on observe une augmentation du surpoids et de l’obésité. Ils sont un défi de grande ampleur pour le système de santé Suisse. Selon l’OFSP, 42% de la population Suisse est en surpoids ou en état d’obésité. Près de 11% des personnes souffrent d’obésité. Avec l’augmentation de l’obésité, on peut également observer sa stigmatisation. Bien connue des scientifiques, ses conséquences sont dramatiques. Outre les conséquences psychologiques, elle peut aggraver l’obésité et de ce fait ses complications. La population considère encore à tort l’obésité comme un simple “laisser aller” et un manque de discipline. Ce genre de pensée mène à la création d’applications destinées à la perte de poids sans encadrement médical spécialisé et personnalisé. Elles pensent résoudre la perte de poids par le comptage des calories et la surveillance du poids. Hors les recommandations de bonnes pratiques vont dans un autre sens. La prise en charge doit être personnalisée et réalisée par une diététicienne, tout en favorisant l’éducation thérapeutique, d’auto-observation et l’autonomie. Les conséquences d’une mauvaise prise en charge sont multiples. Entre autres, compter les calories peut aggraver ou déclencher des troubles du comportement alimentaires. 

## Périmètre & Objectifs

### Application Patient

#### Discussion patient - soignant & Document *

Cette interface permet au patient de poser des questions à la diététicienne et elle pourra lui répondre ainsi que lui partager des ressources tout au long de son périple alimentaire notamment grâce à l'espace document. La conversation contiendra des messages sous forme de bulles comme une messagerie conventionnelle. Il y aura une barre de saisie pour envoyer des messages et charger des fichiers. L'espace document sera accessible grâce à un bouton média qui regroupera les médias par date.

#### Calendrier avec journal des repas *

Le calendrier répertorie les journaux alimentaires au quotidien et permet ainsi d'avoir une vue globale sur le suivi. Lorsqu'un jour est sélectionné, les repas de ce jour ci s'afficheront sous forme d'une carte consultable.

#### Création du journal alimentaire *

Le patient renseignera durant 4-5 jours ses repas dans l'application pendant que la diététicienne pourra observer le remplissage du carnet. Il y aura un bouton pour prendre des images de la gallerie ou prendre une photo directement. Ensuite tous les champs du formulaire santé seront à remplir.

### Application Diététicien

#### Changer données patient #

Cette interface permet d'accéder aux patient et compléter les données de profils d'un patient.

#### Liste des patients *

Cette interface liste tous les patients de la diététicienne et permet ainsi de naviguer parmis ses clients.

#### Rapport de consultation #

Durant la première consultation, la diététicienne remplira les données récoltées durant la séance
(travail, histoire du poids..). Cette interface sera uniquement visible par la soignante. Elle sauvegardera la
session. Et au cours des consultations suivantes, elle continuera de remplir le dossier. Elle pourra
également ajouter des documents à ce dossier, des contacts (ex: médecin, ect..). toutes les
conversations avec le patient se retrouveront également dans ce dossier.

## [Landing page](https://github.com/PDG-NUTRI)

## [Mockup](https://www.figma.com/file/0gbE9gDHY1h7Hnc1fviPDz/PDG-Nutri?node-id=0%3A1)

## Schéma d’architecture
![image](https://user-images.githubusercontent.com/71207824/186847641-579e6742-18f8-4b47-9e0d-ee8988fb623a.png)

## Requirements fonctionnels

## Requirements non-fonctionnels

## Méthodologie de développement
### Processus logiciel
Le temps de développement mis à disposition pour ce projet étant relativement court, nous avons décidé de ne pas utiliser un processus agile itératif. De plus, ayant communiqué au préalable avec notre mandant (Claire Emery, diététicienne) nos requirements sont bien définis.

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
* **To review** : une fois l’implémentation de la story terminée, le développeur ouvre une pull request et place la story dans cette même colonne. Un autre développeur s’occupe alors de vérifier la bonne implémentation de la story et peut laisser des commentaires. Il avertit le reste de l’équipe en se l’assignant en tant que reviewer. S’il n’est pas satisfait de l’implémentation de la story, il la déplace dans la colonne “TODO” avec un commentaire avertissant le développeur des modifications à effectuer. Autrement, il ferme la pull request et déplace l'issue dans done.
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

### CI: Intégration
Afin de garder un code source propre et sain, nous utilisons un linter combiné à des tests. Le linter examine le code après chaque push et le testeur exécute la commande `flutter test`. Si l'intégration continue échoue, le commit est refusé.

### CD: Déploiement continu
Comme notre infrastructure est serverless, nous n'avons pas de code à déployer. En revanche, à chaque changement de version de notre application, nous ajoutons un tag de version sur le commit respectif. Ce tag déclenche alors une Github Action qui va installer java, flutter et compiler notre application et finalement placer le fichier .apk résultant dans la release. Ainsi, nous disposons de toutes les versions au fur et à mesure du développement.
