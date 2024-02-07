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


### VEILLE SUR LES MOTEURS GRAPHIQUES 3D

Un moteur 3D est un composant logiciel qui crée des images matricielles à partir de coordonnées tridimensionnelles.

Il faut prévoir d'en acheter un pour le futur module de visualisation afin de :
- rendre les textures des blocs de glace plus réaliste (avec l'ajout de luminosité et des ombres)
- facilitation du codage (à l'aide de libraries)
- performance de la rapidité d'affichage

Le moteur fournit notamment des fonctions permettant de charger des fichiers dans différents formats, d'animer les modèles en fournissant uniquement le nom de l'animation et ainsi de suite, son but étant de simplifier au maximum le travail du concepteur du module de visualisation.

Voici un comparatifs des moteurs graphiques leaders sur le marché que j'ai trouvés :


- Unreal Engine 5

- Panda 3D

- Unity graphic ?

- SDK ?



**(+ mettre les sources !)**




### RESTRUCTURATION DE L'EQUIPE EN MODE AGILE


___

- Mettre en place un cadre de travail orienté "Agile" pour augmenter la performance d'une équipe ; Voici ses 12 principes fondateurs à intégrer dans les processus de l'entreprise SIBIS :
  - Livrer de la valeur au client
  - Intégrer les demandes de changement
  - Livrer fréquemment une version opérationnelle 
  - Assurer une coopération entre le client et l’équipe
  - Réaliser les projets avec des personnes motivées
  - Privilégier le dialogue en face à face
  - Mesurer l'avancement sur la base d'un produit opérationnel
  - Faire avancer le projet à un rythme soutenable et constant
  - Contrôler l’excellence technique et à la conception
  - Minimiser la quantité de travail inutile
  - Construire le projet avec des équipes auto-organisées
  - Améliorer constamment l'efficacité de l'équipe

Voici quelques uns des avantages à utiliser l'Agilité en entreprise :
- L'adaptation constante du plan d'action
- L'intégration des modifications et évolutions au fil de l'eau
- Une communication renforcée entre les parties prenantes
- Une collaboration renforcée au sein de l'équipe projet
- L'auto-organisation de l'équipe
- La priorisation du travail par la valeur
- Les livraisons rapides et successives
- Des boucles de feedback plus rapides
- Des prises de décision accélérées
- L'amélioration de la qualité et de la satisfaction client
- Le focus sur l'amélioration continue
- Le principe de transparence avec l'ensemble des acteurs projet
- L'agilité réduit le time-to-market
- Le principe du "failing fast", qui met rapidement en avant les méthodes de travail incorrectes et inadaptées
- L'agilité crée de la prédictibilité et de la prévisibilité
- Les risques sont diminués
- On peut arrêter le projet à tout moment

___

- Favoriser une meilleure communication entre les deux bureaux qui ont la même configuration (équipe de chercheurs spécialisé dans un domaine spécifique) en mettant à disposition un open space qui consiste à réunir des bureaux dans un espace ouvert et sans cloisons.

Le problème est que la configuration actuelle des locaux loués par SIBUS ne sont pas adaptés à l'open space car toutes les salles sont déjà occupées par des colaborateurs. Puisque le batiment est loué, il n'est pas envisageable de casser des cloisons. La solution restante est que l'entreprise SIBIS démenage dans d'autres locaux plus adaptés à l'open space.

L'open space est un modèle économique qui comporte de nombreux avantages :
  - environnement favorable pour la mise en place des méthodologies Agile
  - meilleure cohésion et communication entre les équipes (pour favoriser les échanges directs plus rapide et efficaces ; par exemple, entre les équipes scientifiques techniques et les responsables de la mise en production)
  - augmentation de la réactivité (en cas de problème technique, de pic d’activité ou lorsqu'un projet se dessine, il est aisé de rassembler une équipe soudée dans un petit périmètre)
  - réduction de la superficie nécessaire pour accueillir le même nombre de salarié (ce qui permet de baisser les charges en matière de loyer)
  - atténuation de la forte séparation qui existe actuellement entre les équipes scientifiques techniques et les responsables de la mise en production

Il y a néanmoins quelques inconvénients à l'open space qu'il est bien d'évoquer :
  - impression d'être constamment surveillé (générant un stress supplémentaire)
  - augmentation du bruit de fond (générant plus de fatigabilité mentale)

Voici quelques conseils pour la mise en place d'un open space :
  - prévoir une salle de repos et une salle de réunion dans des pièces indépendantes (suffisament à l'écart de l'open space)
  - instaurer des règles de vie commune (pour favoriser le respect mutuel entre les colaborateurs)

___

- Pour le moment, il n'y a au moins 2 problèmes qui nuisent à la communication permanente et qui empechent l'inteligence collective
  - les réunions hebdomadaires pendant lesquelles les colaborateurs abordent tour à tour les travaux effectués durant la semaine précédente et ceux envisagés pour la semaine actuelle ne donnent pas l'occasion à chacun individuelement de rentrer dans le détail de leur recherches respectives, ni ne s'organisent en équipe pour travailler ensemble sur un même projet ou une même tache
  - Le travail est fractionné en fonction de la taille des projets (pour une personne aux connaissances pointues dans un domaine donné) ; ce qui implique que chaque membre est cloisonné dans sa spécialité (autrement dit, il s'agit d'une organisation en silo qui n'est pas compatible avec la méthodologie de travail Agile)

Pour remédier à ces problèmes, la solution serait donc :
- d'ajouter au bilan hebodomaire existant la méthode Agile du "Daily scrum" (consistant à organiser une brève réunion quotidienne concernant uniquement les membres de l’entreprise travaillant sur le sprint) afin d'avoir un horizon à court terme du travail à réaliser, de façon précise et concrète.
- Utiliser l'ordinateur comme un outil de communication et pas simplement comme un outil de calculs mathématiques en encourageant tous les chercheurs et les développeurs à partager leur travail sur un outil de versionning en leur expliquant tout l'intéret qu'il y a à le faire.

Je recommende fortement à tous les colaborateurs (y compris les develloppeurs) d'utiliser Git et GitHub dont les avantages sont les suivants :
- Leader sur le marché des clouds dédiés au code informatique,
- Partage du code, des connaissances et des techniques pour prendre en compte la transversalité des projets
- Code source des projets hébergé dans différents langages de programmation (les autres utilisateurs de GitHub peuvent passer en revue le code et proposer des modifications ou des améliorations)
- Retour en arrière facile en cas d'erreur
- Accès à l'historique des commits (les changements apportés à chaque itération sont gardés en mémoire)

___

- Puisque l’entreprise a le budget pour recruter et qu'elle est en pleine croissance interne, il faudrait embaucher des développeurs salariés (avec une vraie expertise) à la place de stagiaires (qui manquent souvent d'expérience) pour augmenter significativement la qualité du code produit ainsi que la notoriété de l'entreprise.


- Il aussi faudrait en place un réseau social professionnel pour permettre aux collaborateurs de faire appel les uns aux autres en cas de problème, de faciliter des micro-interventions entre collaborateurs sur des projets précis de façon plus souple (à n'importe quel moment) et pour partager des documents à des personnes en privé (si ce n'est pas pertinent que tout le monde soit au courant de l'avancement d'un travail en cours de réalisation). Sur le marché des applications, il y a par exemples :
  1. Slack
  2. Quora
  3. Discord

1. Je recommande fortement d'utiliser Slack dont les principaux avantages sont :
- La connexion à de nombreuses applications telles que Google Drive, Trello et Dropbox (ce qui accélère le flux de travail et la productivité) ou encore la connexion à Jira, qui permet aux équipes d’automatiser le processus d’intégration et de déploiement continus CI/CD (ainsi, tout collaborateur peut vérifier l’état du code, visualiser les structures et les déploiements, mais aussi découvrir ce qui est mis en ligne, directement en un seul et même espace)
- La collaboration en temps réel (ce qui facilite la collaboration entre des équipes à présentes en interne comme à l'internationnal)
- La centralisation des informations de l'équipe (avec un archivage des messages et des documents ainsi que des recherches avancées pour trouver rapidement les informations recherchées)
- Des canaux de communication organisés par sujet (ce qui facilite l'interaction entre les équipes et la recherche de conversations passées)
- Un haut niveau de cryptage qui répond aux normes de sécurité les plus rigoureuses (ce qui garantie la protection des informations de l'entreprise)

2. Les principaux avantages de Quora sont :
- L'échange d'informations qui dépassent la simple recherche pour intégrer l'expertise humaine et les expériences personnelles, enrichissant ainsi la compréhension sur une multitude de sujets spécifiques (forum par question/réponse)
- La possibilité de trouver des informations spécifiques et des opinions variées sur des sujets de niche
- Le système de votes positifs et des commentaires qui renforcent la réputation et crédibilité des réponses données par les experts qui comprennent vraiment les sujets abordés (le site met automatiquement en avant les réponses les plus utiles pour les utilisateurs)
- Son utilisation comme un execellent outil de brainstorming (pour favoriser l'intelligence collective entre les colaborateurs)

3. Les principaux avantages de Discord sont :
- Son interface intuitive et conviviale qui permet aux utilisateurs de naviguer et de communiquer facilement au sein de la plateforme
- sa polyvalence qui peut être utilisé par des groupes d'étude et des collaborations professionnelles
- Ses canaux textuels et vocaux (communication par le biais de messages textuels ou d'appels vocaux, ce qui permet de tenir compte des différentes préférences en matière de communication)
- Son haut degré de personnalisation par les propriétaires de serveur (ce qui leur permet de créer et de concevoir des canaux, des rôles et des autorisations adaptés aux besoins de leur communauté)
- L'intégration possible à plusieurs autres plateformes et services, notamment Twitch, YouTube, Spotify, etc. (il est ainsi facile de partager et d'apprécier le contenu dans l'environnement Discord)
- Sa gratuité d'utilisation de Discord avec de nombreuses fonctionnalités accessibles sans abonnement (il s'agit donc d'une option intéressante pour les communautés dont le budget est limité)
- Ses fonctions de sécurité telles que l'authentification à deux facteurs, le cryptage des messages et la possibilité de définir des paramètres de confidentialité pour les serveurs


## ALEGEMENT DE LA CHARGE DE TRAITEMENT

Sur le long terme, on peut envisager une découpe du moteur de simulation monolythique en microservices indépendants mais cela demanderait un travail très conséquent et qu'il ne s'agit pas là du besoin exprimé par SIBIS.

Afin de décharger le moteur de simulation monolythique de certaines responsabilités, il serait préférable de créer d'autres services (ou programmes).

**VEILLE SUR GATEWAY**



## 

A l'heure actuelle, il n'y a ni chaine d'outils automatisés, ni 

> Schéma CI



___


## REPONSES AUX QUESTIONS POUR LA PROPOSITION DE SOLUTION (il est possible de rajouter d'autres questions)

**Pas obligé d'y répondre à toutes**

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

Les intérêts de faire de l'intégration continue sont multiples :
- 
- 
- 
- 
- 
- 

Pour garantir une meilleure qualité de code, il faut mettre en place un outil de testing pour vérifier, par le biais de tests unitaires, que les algorithmes donnent bien des résultats cohérents avec différents paramètres en entrée. Voici une comparaison entre plusieurs outils de testing :
- Vitest
- Jest
- etc.

Pour mettre fin aux disparités dans les pratiques de travail et les conventions de codage au sein de l'équipe de developpeur, il faut mettre en place un linter qui a pour but de détecter les erreurs statiques. Voici une comparaison entre plusieurs Linters :
- 
- 

Pour (...)
> Veille sur les Débuggeurs (pour détecter les erreurs dynamiques) ?
  -
  -

Pour (...)
> Veille sur les outils de dockerisation ?
  - Docker
  -

Pour (...)
> Utilisation de GitHub Action ?
  -
  -

Pour (...)
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


### POINTS DE BLOCAGE IDENTIFIES PAR SIBIS

- "diversité internationale des équipes de recherche"
  - solution : (...)

- "Processus de Production Archaïque (compilation et un déploiement manuels)"
- "Absence de Tests Automatisés"
  - situation actuelle : de nombreuses taches récurentes doivent être opérées par l'équipe de développement à chaque nouvelle mise en production de l'application (les tests et le deploiment), engendrant une perte de temps considérable et un risque d'erreur non négligeable
  - solution : opter pour de l'intégration continue pour conditionner la **dockerisation** à la **validation des tests** (grâce) et de l'absence d'erreurs statiques ou dynamiques (grâce à un Linter et un debuggeur) ; un système devra ensuite récupérer l'image dockérisée puis la mettre en production automatiquement (sur un hébergeur de projets en ligne)  


## BIBLIOGRAPHIE

https://blog-gestion-de-projet.com/manifeste-agile-valeurs-et-principes/#t-1621593889298

https://www.reussirsesprojets.com/avantages-methodes-agiles/

https://solutions.lesechos.fr/bureau-coworking/c/les-avantages-et-inconvenients-de-lopen-space-7695/

https://datascientest.com/github-tout-savoir

https://tecnobits.com/fr/cuales-son-las-principales-ventajas-de-slack/

https://slack.com/intl/fr-fr/resources/why-use-slack/the-value-of-slack-for-software-developers

https://www.sales-hacking.com/outils/quora

https://barrazacarlos.com/fr/avantages-et-inconvenients-de-la-discorde/
