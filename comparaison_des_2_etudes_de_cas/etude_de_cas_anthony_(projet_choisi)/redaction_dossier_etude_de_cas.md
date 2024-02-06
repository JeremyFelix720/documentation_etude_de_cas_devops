# REDACTION DE L'ETUDE DE CAS


## INTRODUCTION

L'entreprise SIBIS ("Simulation of Interaction between Broken Ice and Structures") a conçu un simulateur d'opérations navales dans les mers de glaces afin d'éviter de mettre en jeu des ressources matérielles coûteuses pour optimiser la navigation de brise-glace et de super-tanqueurs par d'autres entreprises qui font appel à leurs services.

Voici un schéma qui représente le fonctionnement actuel du système de simulation dans sa globalité :

![Figure 1 SIBIS](img/figures_sibis/figure_1_sibis.PNG "Figure 1 SIBIS")

- Au coeur du projet, le moteur de simulation calcule la position, la forme et la taille des différents blocs de glace présents dans la zone analysée (environ 180.000 lignes de code en tout).

- Ajouté à cela, il y a des outils supplémentaires (connectés à la l'application principale) utilisés par les chercheurs pour traiter les infos calculées par le moteur de simulation ; le pré-traitement gère la configuration du moteur de simulation et le post-traitement gère l'exploitation des données calculées par le moteur de simulation (notamment pour en faciliter la lecture).

L'application a vocation a être utilisé sur un ordinateur et les languages utilisés actuellement sont C++ et MatLab.

Voici quelques captures d'écran qui mettent en évidence des exemples de rendus produits actuelement par le moteur de simulation de l'application : 

![Figure 2 SIBIS](img/figures_sibis/figure_2_sibis.PNG "Figure 2 SIBIS")

![Figure 4 SIBIS](img/figures_sibis/figure_4_sibis.PNG "Figure 4 SIBIS")

![Figure 5 SIBIS](img/figures_sibis/figure_5_sibis.PNG "Figure 5 SIBIS")

![Figure 7 SIBIS](img/figures_sibis/figure_7_sibis.PNG "Figure 7 SIBIS")

![Figure 8 SIBIS](img/figures_sibis/figure_8_sibis.PNG "Figure 8 SIBIS")

![Figure 9 SIBIS](img/figures_sibis/figure_9_sibis.PNG "Figure 9 SIBIS")

![Figure 10 SIBIS](img/figures_sibis/figure_10_sibis.PNG "Figure 10 SIBIS")


## OBJECTIF VISE

L'objectif visé par SIBIS est d'offrir une représentation plus esthétique des données calculées pour améliorer la visualisation des différents scenarios de navigation possible par les bateaux sans pour autant alterer la performance des calculs.

## MES MISSIONS 

Dans le cadre d'une étude de cas fictive, j'ai été missionné pour :
1. rédiger un rapport pour comparer les technologies les plus adaptées pour le moteur graphique.
2. commencer la conception du module de visualisation.
3. améliorer le workflow, des dépôts et de la qualité du code en y ajoutant une chaîne de CI/CD automatisée (dans un second temps)


### VEILLE SUR LES MOTEURS GRAPHIQUES

(...)

**(+ mettre les sources !)**

### RESTRUCTURATION DE L'EQUIPE EN MODE AGILE

"L’entreprise est pour l’instant divisée en 4 dans ses locaux : le bureau de l’équipe de direction avec le CEO et le CTO, le bureau des chercheurs et des chercheuses avec 4 personnes toutes spécialistes dans un domaine liée à la climatologie, l’hydrologie, traitement du signal/contrôle, mécanique des fluides, résistance des matériaux, un second bureau avec la même configuration. Toutes ces personnes ne sont pas formées aux outils modernes de développement et n’ont qu’une utilisation basique de git. Un troisième avec  3 personnes dedans : les stagiaires en 5ème année d’école d’ingénieur en informatique. Aucune autre salle n’est disponible, si ce n’est la salle de réunion adaptée au visio-conférence."


- Favoriser une meilleure communication entre les deux bureaux qui ont la même configuration (équipe de chercheurs spécialisé dans un domaine spécifique) en les réunissant tous dans un open space > **Avantages**

- Encourager tous les chercheurs à mettre le fruit de leurs recherche en commun en utilisant git et gitHub en leur expliquant tout l'intéret qu'il y a à versionner son travail :
  - retour en arrière facile
  - fil de la pensée affiché en clair dans l'historique des commits
  - sauvegarde permanente sur un répertoire distant


- Embaucher des développeurs salariés (avec une vraie expertise) à la place de stagiaires (qui manquent souvent d'expérience)

-
-
-
-
-

___

## REPONSES AUX QUESTIONS POUR LA PROPOSITION DE SOLUTION (il est possible de rajouter d'autres questions)

Sur le long terme, on peut envisager une découpe du simulateur monolythique en microservices indépendants mais cela demanderait un travail trop conséquent et qu'il ne s'agit pas du besoin exprimé par SIBIS.


Afin de décharger le moteur de simulation monolythique de certaines responsabilités, il serait préférable de créer d'autres services (ou programmes).


___

1. **Containerisation avec Docker :**

   - Comment Docker peut-il être utilisé pour containeriser chaque service ?

___

   - Comment gérer les dépendances entre services dans un environnement Dockerisé ?


___

2. **Chaîne CI/CD Automatisée :**

   - Comment mettre en place une chaîne CI/CD tenant compte de la séparation entre les équipes scientifiques et de production ?

___

   - Quelles étapes spécifiques doivent être automatisées pour garantir un processus CI/CD fiable ?


> Veille sur les outils de testing ?
  - Vitest
  - Jest
  - etc.

> Veille sur les Linters (pour détecter les erreurs statiques) ?
  -
  -

> Veille sur les Débuggeurs (pour détecter les erreurs dynamiques) ?
  -
  -

> Veille sur les outils de dockerisation ?
  - Docker
  -

> Utilisation de GitHub Action ?
  -
  -

> Veille sur les outils de déploiement ?
  - Versel
  - etc.

___

3. **Tests Automatisés :**

   - Comment intégrer des tests automatisés à chaque étape du processus CI/CD ?

___

   - Quels types de tests sont essentiels pour assurer la stabilité des services ?
  > faire des tests unitaires

___

4. **Surveillance et Logging :**

   - Comment mettre en place une surveillance efficace des services en production ?

___

   - Quels mécanismes de logging peuvent aider à identifier rapidement les problèmes potentiels ?


___


## AXES D'AMELIORATION SUGGERES

### FONCTIONNEMENT INTERNE

- "réunions hebdomadaires pendant lesquelles on aborde tour à tour les travaux effectués durant la semaine précédente et ceux envisagés pour la semaine actuelle"
  - solution : ajouter au bilan hebodomaire existant la méthode Agile du "Daily scrum" (consistant à organiser une brève réunion quotidienne concernant uniquement les membres de l’entreprise travaillant sur le sprint) afin d'avoir un horizon à court terme du travail à réaliser.

- "fractionnement du travail en fonction de la taille des projets (pour une personne aux connaissances pointues dans un domaine donné)"
  - solution : (...)

- "communication permanente entre les différents projets"
  - solution : (...)


### POINTS DE BLOCAGE IDENTIFIES PAR SIBIS

- "forte séparation entre les équipes scientifiques techniques et les responsables de la mise en production"
  - solution : (...)

- "diversité internationale des équipes de recherche"
  - solution : (...)

- "disparités dans les pratiques de travail et les conventions de codage"
  - solution : (...)

- "ils ne peuvent s’occuper à plein temps que d’un seul projet à la fois, mais la transversalité des projets induit un échange de connaissances et de techniques permanent"
  - solution : (...)

- "Processus de Production Archaïque (compilation et un déploiement manuels)"
- "Absence de Tests Automatisés"
  - situation actuelle : de nombreuses taches récurentes doivent être opérées par l'équipe de développement à chaque nouvelle mise en production de l'application (les tests et le deploiment), engendrant une perte de temps considérable et un risque d'erreur non négligeable
  - solution : opter pour de l'intégration continue pour conditionner la **dockerisation** à la **validation des tests** (grâce) et de l'absence d'erreurs statiques ou dynamiques (grâce à un Linter et un debuggeur) ; un système devra ensuite récupérer l'image dockérisée puis la mettre en production automatiquement (sur un hébergeur de projets en ligne)  
