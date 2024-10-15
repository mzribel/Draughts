# Draughts

Application web de jeu de dames anglaises (Draughts) réalisé dans le cadre du projet de fin de deuxième année de bachelor informatique par [Marianne Corbel](https://github.com/mzribel), [Tony De Donato](https://github.com/Tony-De-Donato) et [Eva C.](https://github.com/evzs).

Ce projet est divisé en trois parties distinctes, chacune possédant son propre dépôt Github :
- [Frontend](https://github.com/mzribel/Draughts-Frontend) - VueJS (Nuxt)
- [Serveur de jeu](https://github.com/mzribel/Draughts-Backend) - Java 21
- [API](https://github.com/mzribel/Draughts-Api) - MariaDB & ExpressJS

## Fonctionnalités 

- Inscription / Connexion utilisateur
- Matchmaking concurrent contre un autre joueur (websockets)
- Jeu de dames appliquant strictement les règles des [Dames Anglaises (Draughts)[https://fr.wikipedia.org/wiki/Dames_anglaises]
- Conversion des données de jeu téléchargeables sous le format international [PDN (Portable Draughts Notation)](https://en.wikipedia.org/wiki/Portable_Draughts_Notation), lisible par divers logiciels de traitement des données de jeu.
- Implémentation future de l'import de données de jeu PDN à des fins d'analyse et de review de parties 

Ce projet implique la mise en place d'un serveur de données MySQL ou MariaDB dont le script d'initialisation est trouvable [ici](https://github.com/mzribel/Draughts-Backend/blob/main/docs/bdd.sql).

## Front-end

Réalisé intégralement sous Nuxt JS (Vue3, composition API).

![Capture d'écran du jeu](https://i.postimg.cc/ZKyFnPzs/Capture-d-cran-2024-10-15-173343.png)

## Serveur de jeu

Websockets et logique de jeu réalisés sous Java 21, respectant strictement les principes de la programmation orientée objet selon les structures suivantes.

**Logique de jeu** :

![Diagramme de classe - Logique du jeu](https://github.com/mzribel/Draughts-Backend/blob/main/docs/classes_checkers.png)

**Serveur de jeu** :

![Diagramme de classe - Serveur de jeu](https://github.com/mzribel/Draughts-Backend/blob/main/docs/classes_gameserver.png)

## Base de données et API associée 

API réalisée via ExpressJS, impliquant un middleware d'authentification et d'administration, permettant d'accéder aux données liées à l'utilisateur (inscription/connexion, connexions à la file d'attente, données de jeu).

Base de donnée réalisée sous MariaDB et administrée via phpmyadmin) :

![MLD base de données](https://github.com/mzribel/Draughts-Backend/blob/main/docs/mld.png)
