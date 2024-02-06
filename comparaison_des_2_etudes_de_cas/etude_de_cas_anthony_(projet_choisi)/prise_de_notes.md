// Microservices = uniquement le back


// créer une API en C++ pour le moteur de simulation

// créer une api pour chaque ensemble de pré et post-routines de traitement, écrites en C ++ et Matlab**


1. **Décomposition en Microservices :**

  - Quelles fonctionnalités spécifiques de l'application peuvent être transformées en microservices indépendants ?

    Pour améliorer l’agilité de développement, le déploiement, la tolérance de panne et la scalabilité, il serait préférable de prévoir au moins un microservice dédié pour chaque domaine d'activité différent géré par le backend de l'application le décomposant en microservices les fonctionnalités suivantes :

### CRUD (Create, Read, Update, Delete) pour chaque catégorie de données de la base de données :
    - la gestion des utilisateurs ?
    - la gestion de l'analyse des chercheurs selon leur branche d'activité ?

### Calculs de données
    - le calcul de la dynamique de la structure et de la glace par le **moteur de simulation**

### Utilisation des données pour la représentation de visuels :
    - la reproduction avec une haute fidélité des **charges de glace** et les **mouvements des structures offshores**
    - les **briques logicielles** de modélisation de systèmes flottants multi-corps articulés et des liaisons souples de type câble

### Traitement de fichiers en vue de leur exploitation :
    - le prétraitement des fichiers d’entrée
    - le post-traitement des résultats 
    (comme les graphes ou les animations) 


____
ECLAIRCICEMENT D'ANTHONY :



- simulateur d'opération navale permet d'éviter de mettre en jeu des ressources matérielles couteuse pour tester la navigation du brise-glace et des super-tanqueurs dans des mers de glace.



- pas des microservices, mais plus

- coeur du projet = moteur de simu > on est pas censé le décomposer en microservice (180.000 lignes de code)
> on peut envisager une découpe du simulateur en monolythique mais cela demanderait un travail trop consé on peut rien y faire si les 
> faire un rendu plus joli mais sans alterer les calculs
> **FAIRE UNE VEILLE SUR LES DIFFERENTS MOTEURS GRAPHIQUES LES PLUS ADAPTEE !** (+ mettre les sources)
> mettre en place des microservices pour intégrer les nouveaux modules à l'appli existante. 


- Objectif (se concentrer là-dessus)= offrir une représentation des données calculés pour VOIR le chemin à prendre en rajoutant un moteur graphique
> faire des tests unitaires
> **faire une introduction de présentation de l'appli actuelle avec les rendus actuels (insérer les figures sibis)**


- pré / post traitement =  ensemble d'outils (utilisés par les chercheurs) qui permettent de traiter les infos calculées par l'appli ; ces étapes ne font pas parti de l'appli mais permettent d'en faciliter la lecture et l'exploitation !

- pré-traitement = configuration du moteur de simulation
- post-traitement = exploitation des données calculées par le moteur de simulation

_____
Aprèm

-
-
-
-
-


