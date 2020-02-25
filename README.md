# valentin_projet_s3

Rapport de projet
Jeu de piste



Réalisé par
Valentin ETHEVE
Thomas GLEIZES
Basile SAVOURET
Davio VIATOR




Sous la direction
Francis  GARCIA
Agnès MAZARS-CHAPELON


Pour l’obtention du DUT
Année universitaire 2019 - 2020

Remerciement 
Remerciement à  Monsieur Francis GARCIA et à Madame Agnès MAZARS-CHAPELON pour l’aide et support qu’il nous ont offert pendant ce projet



1. Présentation du projet	8
1. 1. Analyse de l’existant	8
1. 2. Les objectifs de l’application	10
1. 3. Les cibles	10
1. 4. Le type d’application	10
1. 5. L’équipement des joueurs	11
1. 6. périmètre du projet	11
1.7. spécificités	11
1.7. 1. le contenu de votre application	11
1. 7. 2. Contraintes techniques	11
2. Rapport technique	12
2. 1. Base de données et conception	12
2.2 Front-end (côté client)	12
2.3 Back-end (côté serveur)	12


Sommaire :
Introduction
1.  Présentation du projet :
1.1 Analyse de l’existant 
1.2. Les objectifs de l’application
1.3. Les cibles 
1. 4. Le type d’application 
1. 5. L’équipement de vos cibles
1.6. Périmètre du projet 
1.7.    Spécificités:
1.7.1. Le contenu de votre application
1.7.2. Contraintes techniques 
2 Rapport technique
2.1 Conception et base de donnée
2.2 Conception côté client	
2.3 Conception côté serveur
3. Résultats
3.1 Installation
3.2 Manuelle d’utilisation 
4. Gestion du projet
4.1 Démarche suivie
4.2 Planification des tâches
4.3 Bilan critique du projet
Conclusion
Bibliographie
Annexe technique



Tables de figues






















Glossaire





















Introduction
	
Chaque année l’IUT accueil de nouveaux étudiants au sein de sa structure, qui peut apparaître tel un labyrinthe sans signification pour certains d’entre eux. Dans le but de les aider à découvrir l’IUT de manière ludique et divertissante, nous avons créé dans le cadre de notre projet tuteuré un jeu de piste. Au travers des infrastructures de l’IUT, il permet de découvrir les divers départements au file d’énigmes entraînantes et de découvertes enrichissantes.
Nous allons d’abord présenter le résultat de notre analyse des applications de jeu de de piste déjà existantes.  Puis nous verrons plus en détaille le but et les missions que devront remplir notre projet et enfin les contraintes et les choix de développement choisi. Nous verrons par la suite le rapport de tous les problèmes et de toutes les solutions et décisions prises au cours du développement de notre application.





























1. Présentation du projet

Ce projet consiste à créer une application web simulant un jeu de piste/chasse aux trésors pour les nouveaux arrivant dans l’IUT. Ce jeu se fera durant la journée portes ouvertes de l’IUT et permettra aux possibles futures étudiants de découvrir l’IUT de manière interactive et ludique. Notre projet consistera à créer un jeu compétitif se déroulant en équipe. Le but sera de trouver des QR codes (ou des codes) en résolvants des énigmes de plus en plus difficiles et en se déplaçant au travers des infrastructures de l’IUT.

1. 1. Analyse de l’existant 
Pour l’analyse de l'existant nous avons cherché des jeux de pistes s’effectuant à proximité. nous avons trouvé deux applications similaires. Tout d’abord nous avons l’application ‘Piste et Trésor’ de la société Furet Company qui propose une bibliothèque de jeux de pistes/chasses aux trésors sur smartphone.

 Dans cette bibliothèque nous avons choisie un jeu de piste permettant de découvrir le sud de l’hérault.

On retrouve une liste des villages à découvrir avec une présentation, une carte et des lieux à visiter aux alentours, avec leurs localisations présentent sur la carte. 

 En deuxième nous avons trouvé l’application ‘Montpellier Discovery’. Qui propose de faire découvrir Montpellier avec un jeu de piste en réalité augmentée.


On y retrouve plusieurs parcours scénarisés à effectuer contenant des énigmes à résoudre en réalité augmentée. On a pour informations la durée du parcours, sa longueur, le point de départ, l’âge nécessaire et les nécessités matérielles. Le parcours est guidé par un système de photos fléchées. Nous pouvons aussi retrouver une carte de l’université Paul Valéry sur cette application.

1. 2. Les objectifs de l’application

Notre objectif est de permettre la découverte de l’IUT de manière ludique et intéractive. Mais aussi  permettre l’échange, l'interaction et le divertissement des différents utilisateurs au sein d’une compétition de rapidité et de réflexion, dont seule la cohésion de groupe permettra  la victoire.


1. 3. Les cibles 

Toute personnes présentes à la journée porte ouverte de l’IUT souhaitant découvrir l’IUT seule ou en groupe. Mais aussi les personnes voulant visiter l’IUT durant l’année.

1. 4. Le type d’application 

Nous comptons faire une application de jeu permettant de regrouper les joueurs, d’afficher leur énigmes respectives et d’afficher diverses informations. Et nous allons faire aussi une extension en site web permettant d’afficher des informations comme la localisation des différentes équipes, leurs points et leurs avancées dans le parcours pour les spectateurs de la partie en cours.

1. 5. L’équipement des joueurs 

Le jeux de piste sera disponible sur un site web il y aura une partie participant et une partie spectateur. Les spectateurs peuvent voir le scores des différents groupes et leur position sur une carte, les participants quand à eux auront juste l’interface de joueur avec les énigmes et leur score.


1. 6. périmètre du projet 

Nous aurons besoin d’identifier les joueurs via un système d’inscription car ont ne peux pas utiliser le serveur de l’IUT pour des raisons de sécurité. Les équipes seront définis par des joueurs. En lançant l’application, un joueur pourra inviter les autres joueurs connecté avec leur pseudo. L’application utilisera les données de géolocalisation et l’appareil photo du téléphone.  

1.7. spécificités 

1.7. 1. le contenu de votre application 

Nous avons donc besoin d’une application avec une interface permettant de rejoindre une équipe sur une partie qui va démarrer avec un login donné par l’administrateur ayant créé la partie. Dans chaques équipes l’un des participants sera sélectionné comme étant le chef de l’équipe. La position de son téléphone sera envoyée à l’extension web et il sera le seul à pouvoir scanner les QR codes trouvés par son équipe. Chaques membres de l’équipe aura accès à l’énigme en cours et toutes les informations concernant son équipes (les points, l’avancement du parcours, le nom du chef etc…). Ensuite l’extension web sera affichée par l’administrateur (en Amphi par exemple) pour toutes les personnes voulant regarder la partie en cours. On aura une carte d’afficher avec la position de chaques équipes, la position du QR code qu’elles doivent trouver, leurs nombres de points et leurs avancées dans le parcours. A la fin d’une partie le nom de l’équipe et son positionnement dans un classement générale seront enregistrés et pourront être affichés sur l'accueil de l’application. Nous stockerons des informations dans une base de données (le nombre de joueurs totale, le nombre de parties effectuées etc…).

1. 7. 2. Contraintes techniques 

Nous aurons besoin d’une partie back-end permettant de gérer des données éphémères en temps réel (position de l’équipe, point de l’équipe etc…). Cette partie permettra de gérer aussi des données stockées à long termes comme le tableaux des scores. Nous aurons besoin d’apprendre à utiliser et afficher une carte avec différentes données présentes dessus. Nous aurons besoin d’apprendre à développer une application mobile. Il faudra lier la base de données de l’application et de l’extension web et pouvoir les faire communiquer entre elles. Il faudra que l’application soit disponible dans diverses langues pour les étudiants étrangers. Les énigmes devront être adaptées au niveau des joueurs. 



2. Rapport technique


2. 1. Base de données et conception 

La base de Données est un élément essentiel du projet, elle nous permet de stocker toutes les information importante tel que les informations sur les utilisateurs (pseudo, mot de passe chiffré etc) ainsi que les informations concernant les différents parcours (énigmes, groupe, classement etc).

2.2 Front-end (côté client)

2.3 Back-end (côté serveur)


Résumé

Ce projet consiste à créer une application web simulant un jeu de piste/chasse aux trésors pour les nouveaux arrivant dans l’IUT. Ce jeu se fera durant la journée portes ouvertes de l’IUT et permettra aux possibles futures étudiants de découvrir l’IUT de manière interactive et ludique. Notre projet consistera à créer un jeu compétitif se déroulant en équipe. Le but sera de trouver des QR codes (ou des codes) en résolvants des énigmes de plus en plus difficiles et en se déplaçant au travers des infrastructures de l’IUT.
Nous avons réalisé  l’application avec les technologie d'interfaçage du web soit html,css et javascript. Pour le côté serveur nous avons utilisé du php dans un modèle MVC.
