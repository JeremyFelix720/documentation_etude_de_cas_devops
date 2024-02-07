# ANALYSE DU PROJET PROPOSE PAR ANTHONY

## MOTS-CLE IMPORTANTS REGROUPES EN CATEGORIES (avec pour chacun d'entre eux le(s) besoin(s) associé(s))

___
### SPECIALISATIONS

- consultation et de la recherche et développement (R&D)

- Parapétrolier, Offshore, Énergies Marines Renouvelables (EMR) et Naval

___
### LANGUAGES / TECHNO UTILISES

- Le moteur de simulation est écrit en C ++, et un ensemble de pré et post-routines de traitement, écrites en C ++ et Matlab
  - solution : trouver un framework d'API qui est compatible avec les microservices et qui peut interpretter les langages C++ et MatLab(ne pas proposer NextJS car c'est du fullstack et que les programmes sont uniquement écrit en JavaScript)


- La plateforme de sortie visée est Windows 11.


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

- Outils de testing :
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


## QUESTIONS A POSER AU FORMATEUR ANTHONY

- Quel est le nom de l'application ?
    > SIBIS

- Combien y a-t-il de base(s) de données ?
    > Réponse

- De quels champs la bases de données de l'app est-elle composée ? (users ? analyses ?) ; parmi eux, quelles données de l'application sont concernées par le CRUD ?
    > Réponse

- Quelles sont les différentes "Briques logicielles" de la modélisation de systèmes flottant multi-corps articulés et des liaisons souples de type câble ? Et sont-elles déjà fonctionnelles à l'heure actuelle ?
    > Réponse

- Qu'est-ce que c'est des "routines supplémentaires" ?
    > Réponse

- Est-ce qu'il a besoin de diviser en micro services toutes les modules de l'application ? Même question pour les services existants qui sont déjà en état de fonctionnement ? (car cela demanderait surement beaucoup de travail aux develloppeurs de changer toute l'architecture de leur application)
    > Réponse : Non

- Est-ce qu'il faut mettre en place un CI pour l'appli ?
    > Réponse : OUI "améliorer le workflow, des dépôts et de la qualité du code en y ajoutant une chaîne de CI/CD automatisée"

- Est-ce qu'il faut proposer une restructuration des équipes de travail ? Pour les rendre + agiles ?
    > Réponse :

- Est-ce que les figures fournies ont été réalisées avec le logiciel MatLab ?
  > Réponse : Non, c'est une autre techno


- Qu'est-ce qu'il faut mettre comme info dans le résumé en anglais ?
  > C'est pour le titre CDA, pas pour l'étude de cas !

