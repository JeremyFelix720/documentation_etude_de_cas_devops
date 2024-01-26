# ANALYSE DU PROJET PROPOSE PAR ANTHONY

## MOTS-CLE IMPORTANTS REGROUPES EN CATEGORIES (avec pour chacun d'entre eux le(s) besoin(s) associé(s))

___
### SPECIALISATIONS

- consultation et de la recherche et développement (R&D)

- Parapétrolier, Offshore, Énergies Marines Renouvelables (EMR) et Naval

___
### LANGUAGES UTILISES

- Le moteur de simulation est écrit en C ++, et un ensemble de pré et post-routines de traitement, écrites en C ++ et Matlab
  - solution : trouver un framework d'API qui est compatible avec les microservices et qui peut interpretter les langages C++ et MatLab(ne pas proposer NextJS car c'est du fullstack et que les programmes sont uniquement écrit en JavaScript)

___
### FONCTIONNEMENT INTERNE

- réunions hebdomadaires pendant lesquelles on aborde tour à tour les travaux effectués durant la semaine précédente et ceux envisagés pour la semaine actuelle
  - solution : ajouter au bilan hebodomaire existant la méthode Agile du "Daily scrum" (consistant à organiser une brève réunion quotidienne concernant uniquement les membres de l’entreprise travaillant sur le sprint) afin d'avoir un horizon à court terme du travail à réaliser.

- fractionnement du travail en fonction de la taille des projets (pour une personne aux connaissances pointues dans un domaine donné)
  - solution :

- communication permanente entre les différents projets
  - solution :

___
### FORCES

- l’entreprise recrute et est en pleine croissance interne

- équipes assez flexibles et indépendantes

- entraide entre les différents collaborateurs (micro-interventions entre collaborateurs)

- synergie de connaissances

- apport de fonds, à la fois de l’état et des grandes entreprises du secteur

___
### POINTS DE BLOCAGE

- forte séparation entre les équipes scientifiques techniques et les responsables de la mise en production
  - solution :

- diversité internationale des équipes de recherche
  - solution :

- disparités dans les pratiques de travail et les conventions de codage
  - solution :

- ils ne peuvent s’occuper à plein temps que d’un seul projet à la fois, mais la transversalité des projets induit un échange de connaissances et de techniques permanent
  - solution :

- Application monolythique executée sur des ordinateurs gourmands en ressources (donc coûteux et inéficaces)
  - situation actuelle : pour mettre à jour un composant du programme, il faut réécrire toute l'application (ce qui empeche son fonctionnement global à chaque opération de maintenance puisque tous les composants sont interdépendants)
  - solution : opter pour une application modulaire où chaque module (un microservice, par exemple) peut être modifié sans que cela se répercute sur les autres parties du programme.

- Processus de Production Archaïque (compilation et un déploiement manuels)
- Absence de Tests Automatisés
  - situation actuelle : de nombreuses taches récurentes doivent être opérées par l'équipe de développement à chaque nouvelle mise en production de l'application (les tests et le deploiment), engendrant une perte de temps considérable et un risque d'erreur non négligeable
  - solution : opter pour de l'intégration continue pour conditionner la **dockerisation** à la **validation des tests** (grâce) et de l'absence d'erreurs statiques ou dynamiques (grâce à un Linter et un debuggeur) ; un système devra ensuite récupérer l'image dockérisée puis la mettre en production automatiquement (sur un hébergeur de projets en ligne)  

___
### BESOINS EXPRIMES

- Le CTO demande de produire un rapport sur les différentes technologies de visualisations envisagées pour savoir laquelle serait la plus adaptée pour le module 
  - solution : o

- améliorer le workflow, des dépôts et de la qualité du code en y ajoutant une chaîne de CI/CD automatisée
  - solution : o

- L'objectif principal est de transformer cette application monolithique en une architecture basée sur des microservices, tout en établissant une chaîne d'outils automatisée pour l'intégration continue (CI) et le déploiement continu (CD)
  - solution : o


- proposer une solution complète pour moderniser notre application et mettre en place une chaîne d'outils automatisée
  - solution :

___

> **Reprendre les questions pour la Proposition de Solution et y répondre**


___
## BENCHMARK DES OUTILS POUR CHAQUE BESOIN IDENTIFIE

- Framework d'API divisés en micro services et multi langages :
  - 
  - 

- Outils de yesting :
  - Vitest
  - Jest

- Outils de dockerisation :
  - Docker
  - 

- Débuggeurs (pour détecter les erreurs dynamiques) :
  -
  -

- Linter (pour détecter les erreurs statiques) :
  - 
  -

- Hébergeurs :
  - Versel
  - 

-



## SHEMAS EXPLICATIFS A REALISER
- intégration continue
-
-
-
-


## QUESTIONS A POSER AU FORMATEUR

-  Qu'est-ce que c'est des "routines supplémentaires" ?
  - Réponse

- Est-ce qu'il a besoin de diviser en micro services toutes les modules de l'application ? Même question pour les services existants qui sont déjà en état de fonctionnement ? (car cela demanderait surement beaucoup de travail aux develloppeurs de changer toute l'architecture de leur application)

- Quelles données de l'application sont concernées par le CRUD ?

- Les briques logicielles de modélisation de systèmes flottant multi-corps articulés et des liaisons souples de type câble sont-elles opérationnelles ?

___

**Questions pour la Proposition de Solution :**

1. **Décomposition en Microservices :**

  - Quelles fonctionnalités spécifiques de l'application peuvent être transformées en microservices indépendants ?
    - la reproduction avec une haute fidélité des charges de glace et les mouvements des structures offshores
    - le calcul de la dynamique de la structure et de la glace par le moteur de simulation
    - le génération de champs de glace
    - le prétraitement des fichiers d’entrée
    - le post-traitement des résultats (comme les graphes ou les animations) 
    - les briques logicielles de modélisation de systèmes flottant multi-corps articulés et des liaisons souples de type câble
    - [le module de visualisation]
    - la gestion des utilisateurs (s'il y en a une)

> Schéma avec les 2 options :
  - modules existants + futures modules sous forme d'une app monolytique (où le backend ne contient qu'une API)
  - modules estistant + futures modules sous forme d'une app en mi (où le backend est divisé en plusieurs API)


  - Comment assurer la cohérence et la communication entre les équipes travaillant sur différents microservices ?
    - trouver un framework d'API qui est compatible avec les microservices et qui peut interpretter les langages C++ et MatLab (ne pas proposer NextJS car c'est du fullstack et que les programmes sont uniquement écrit en JavaScript)
    -


2. **Containerisation avec Docker :**
  - Comment Docker peut-il être utilisé pour containeriser chaque microservice ?
  - Comment gérer les dépendances entre microservices dans un environnement Dockerisé ?

3. **Orchestration avec Kubernetes :**
  - Pourquoi Kubernetes est-il essentiel pour orchestrer le déploiement des microservices ?
  - Comment garantir la flexibilité et l'évolutivité des microservices grâce à Kubernetes ?

4. **Chaîne CI/CD Automatisée :**
  - Comment mettre en place une chaîne CI/CD tenant compte de la séparation entre les équipes scientifiques et de production ?
  - Quelles étapes spécifiques doivent être automatisées pour garantir un processus CI/CD fiable ?

5. **Tests Automatisés :**
  - Comment intégrer des tests automatisés à chaque étape du processus CI/CD ?
  - Quels types de tests sont essentiels pour assurer la stabilité des microservices ?

6. **Surveillance et Logging :**
  - Comment mettre en place une surveillance efficace des microservices en production ?
  - Quels mécanismes de logging peuvent aider à identifier rapidement les problèmes potentiels ?
