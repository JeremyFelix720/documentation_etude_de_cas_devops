# REDACTION DE L'ETUDE DE CAS


## INTRODUCTION

L'entreprise SIBIS ("Simulation of Interaction between Broken Ice and Structures") a conçu un simulateur d'opérations navales dans les mers de glaces afin d'éviter de mettre en jeu des ressources matérielles coûteuses pour optimiser la navigation de brise-glaces et de super-tanqueurs par d'autres entreprises qui font appel à leurs services.

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

L'objectif principal visé par SIBIS est d'offrir une représentation plus esthétique des données calculées pour améliorer la visualisation des différents scenarios de navigation possible par les bateaux sans pour autant alterer la performance des calculs.

## MES MISSIONS 

Dans le cadre d'une étude de cas fictive, j'ai été missionné pour :
1. rédiger un rapport pour comparer les technologies les plus adaptées pour le moteur graphique.
2. commencer la conception du module de visualisation.
3. améliorer le workflow, des dépôts et de la qualité du code en y ajoutant une chaîne de CI/CD automatisée (dans un second temps)

## VEILLE SUR LES MOTEURS GRAPHIQUES 3D

Un moteur 3D est un composant logiciel qui crée des images matricielles à partir de coordonnées tridimensionnelles.

Il faut prévoir d'en acheter un pour le futur module de visualisation afin de :
- rendre les textures des blocs de glace plus réaliste (avec l'ajout de luminosité et des ombres)
- faciliter le codage (à l'aide de libraries)
- Augmenter la rapidité d'affichage

Le moteur fournit notamment des fonctions permettant de charger des fichiers dans différents formats, d'animer les modèles en fournissant uniquement le nom de l'animation et ainsi de suite, son but étant de simplifier au maximum le travail du concepteur du module de visualisation.

Voici un comparatifs des moteurs graphiques que j'ai trouvés :
1. Panda 3D
2. Unity (Simulation) Pro
3. Unity
4. Unreal Engine 5


1. Voici les avantages de Panda 3D que je recommande d'utiliser pour les raisons suivantes  :
- Documentation complète
- Communauté très active
- Moteur open source et totalement gratuit (sans redevances, sans paiement de licence, ni enregistrement ni frais de quelque nature que ce soit, même pour un usage commercial) pour les jeux 3D en temps réel, les visualisations, les simulations, les expériences
- Riche ensemble de fonctionnalités qui s’adapte facilement aux besoins spécifiques en matière de flux de travail et de développement
- Très grande flexibilité (gestion flexible des actifs, création de techniques graphiques et pipelines de rendu personnalisés, etc.) et performance (avec un système de profilage sur le réseau pour comprendre quelles parties sont concernées pour chaque milliseconde du temps d'image)
- Moteur multiplateforme (tolérance du matériel ancien et nouveau, déploiement de l'application sur toutes les platesformes prises en charge)
- Noyau écrit en C++ portable (pour sa vitesse d'execution) et en Python (pour sa facilité d'utilisation)
- Aucun passe-partout ni aucun code d'initialisation compliqué
- Livré avec le moteur physique Bullet (bibliothèque intégrable à un programme qui permet la résolution des équations physiques)

2. Voici les avantages de Unity (Simulation) Pro :
- Coût de l'abonnement raisonnable : 115€/mois
- Exécution de plusieurs scénarios avec une physique précise à n'importe quelle échelle, sur site ou dans un cloud privé
- Pas de dépendances vis-à-vis des systèmes qui ne bénéficient pas de la simulation (ce qui permet d'accélèrer le flux de travail à chaque étape du cycle de développement)

3. Voici les avantages de Unity :
- Moteur de jeu le plus connu et le plus utilisé par les développeurs
- Adapté pour des modules de réalité augmentée et les contenus de réalité virtuelle (avec des visuels de qualité proffessionnelle)
- Possibilité de développer de projets complexes
- Plateforme de développement utilisable en version gratuite (sans limite de temps)
- Un magasin d’actifs bien rempli
- Une documentation bien fournie
- Communauté très active
- Interface plus accessible à tous
- Possibilité de passer par l’IDE intégré de Unity pour générer du code manuelement avec un script rapide et simple
- Grande variété d’outils ainsi que de nombreuses ressources 2D et 3D
- Compatibilité multiplateforme (fonctionne avec sur Steam, macOS, iOS, Android, PC)

4. Voici les avantages de Unreal Engine 5 :
- Plateforme de développement utilisable en version gratuite (sans limite de temps)
- Un magasin d’actifs bien rempli
- Communauté très active
- Une documentation bien fournie
- Idéal pour la création de contenus de réalité virtuelle
- Intègration de nombreux outils dont pour proposer de superbes contenus et expériences en temps réel
- Suréchantillonnage de haute qualité indépendamment de la plateforme (rendu dans une résolution beaucoup plus faible, mais avec des images de sortie dont la fidélité est équivalente à celle des images générées dans une résolution plus élevée)
- Éclairage global dynamique et gestion des reflets
- Environnements entièrement dynamiques avec une grande fidélité visuelle (et massivement détaillés)
- Mondes ouverts plus grands et immersifs



## METHODOLOGIE AGILE

Mettre en place des méthodes de travail orientées "Agile" pour augmenter la performance d'une équipe ; Voici ses 12 principes fondateurs à intégrer dans les processus de l'entreprise SIBIS :
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

Voici quelques uns des avantages à utiliser l'Agilité pour l'entreprise SIBIS :
- L'adaptation constante du plan d'action
- L'intégration des modifications et évolutions au fil de l'eau
- Une communication renforcée entre les parties prenantes
- Une collaboration renforcée au sein de l'équipe projet
- Des boucles de feedback plus rapides
- Le principe de transparence avec l'ensemble des acteurs projet
- Le principe du "failing fast", qui met rapidement en avant les méthodes de travail incorrectes et inadaptées
- L'agilité crée de la prédictibilité et de la prévisibilité
- Les risques sont diminués

On peut aussi citer les avantages suivants à utiliser l'Agilité (de façon plus générale) :
- L'auto-organisation de l'équipe
- La priorisation du travail par la valeur
- Les livraisons rapides et successives
- Des prises de décision accélérées
- L'amélioration de la qualité et de la satisfaction client
- Le focus sur l'amélioration continue
- L'agilité réduit le "time-to-market" (temps de mise sur le marché d'un produit ou service)
- On peut arrêter le projet à tout moment

___

## CADRE DE TRAVAIL

Favoriser une meilleure communication entre les deux bureaux qui ont la même configuration (équipe de chercheurs spécialisé dans un domaine spécifique) en mettant à disposition un open space qui consiste à réunir des bureaux dans un espace ouvert et sans cloisons.

Le problème est que la configuration actuelle des locaux loués par SIBUS ne sont pas adaptés à l'open space car toutes les salles sont déjà occupées par des colaborateurs. Puisque le batiment est loué, il n'est pas envisageable de casser des cloisons. La solution restante est que l'entreprise SIBIS démenage dans d'autres locaux plus adaptés à l'open space.

L'open space est un modèle économique qui comporte de nombreux avantages :
  - Environnement favorable pour la mise en place des méthodologies Agile
  - Meilleure cohésion et communication entre les équipes (pour favoriser les échanges directs plus rapide et efficaces ; par exemple, entre les équipes scientifiques techniques et les responsables de la mise en production)
  - Augmentation de la réactivité (en cas de problème technique, de pic d’activité ou lorsqu'un projet se dessine, il est aisé de rassembler une équipe soudée dans un petit périmètre)
  - Réduction de la superficie nécessaire pour accueillir le même nombre de salarié (ce qui permet de baisser les charges en matière de loyer)
  - Atténuation de la forte séparation qui existe actuellement entre les équipes scientifiques techniques et les responsables de la mise en production

Il y a néanmoins quelques inconvénients à l'open space qu'il est bien d'évoquer :
  - Impression d'être constamment surveillé (générant un stress supplémentaire)
  - Augmentation du bruit de fond (générant plus de fatigabilité mentale)

Voici quelques conseils pour la mise en place d'un open space :
  - Prévoir une salle de repos et une salle de réunion dans des pièces indépendantes (suffisament à l'écart de l'open space)
  - Instaurer des règles de vie commune (pour favoriser le respect mutuel entre les colaborateurs)

___

## GESTION DE PROJET

Afin d'organiser et de répartir le travail au sein d'une équipe pour un projet donné, il faudrait prendre l'habitude de référencer les taches et de se positionner dessus grâce à un outil de gestion de projet. Il y a par exemples :
1. Monday
2. Trello 

Voici les avantages de Monday :
- Interface conviviale (ce qui permet aux membres de l'équipe de démarrer relativement facilement et d'utiliser le logiciel de manière efficace. Il ne nécessite qu'une formation minimale)
- Création et personnalisation des flux de travail, tableaux et tableaux de bord (ce qui permet d'adapter le logiciel à leurs besoins uniques en matière de gestion de projet)
- Approche visuelle et intuitive, avec des tableaux, des cartes et des calendriers codés par couleur (ce qui facilite le suivi des progrès et des délais d'un seul coup d'œil)
- Collaboration au sein de l'équipe en proposant des fonctionnalités telles que l'attribution de tâches, les commentaires, les pièces jointes et les notifications (ce qui permet de rationaliser la communication et de faire en sorte que tout le monde soit sur la même longueur d'onde)
- Intègration à un large éventail d'outils et d'applications tiers, tels que Google Workspace, Microsoft Office, Slack, et plus encore, permettant aux utilisateurs de connecter leur environnement de travail de manière transparente
- Fonctions d'automatisation, telles que des déclencheurs et des automatismes (ce qui permet d'éliminer les tâches répétitives et de gagner du temps)
- Génération des rapports et suivi des indicateurs clés de performance (KPI) (ce qui permet d'obtenir des informations sur l'avancement du projet et la productivité de l'équipe)

Voici les avantages de Trello :
- Interface conviviale, intuitive et simple à utiliser
- Collaboration en temps réel pour une productivité accrue
- Intégrations avec de nombreuses autres applications populaires
- Rassemblement des tâches, de la gestion des projets, des coéquipiers en un seul endroit, même si l'équipe est répartie dans le monde entier
- Projets personnalisables avec de nouveaux aspects à mesure que l'équipe s’agrandit (qui peut même comprendre des centaines de collaborateurs)
- Disponible sur diverses plateformes, y compris les appareils mobiles

___

## COMMUNICATION EN INTERNE

Pour le moment, il n'y a au moins 2 problèmes qui nuisent à la communication permanente et qui empechent l'inteligence collective
  - les réunions hebdomadaires pendant lesquelles les colaborateurs abordent tour à tour les travaux effectués durant la semaine précédente et ceux envisagés pour la semaine actuelle ne donnent pas l'occasion à chacun individuelement de rentrer dans le détail de leur recherches respectives, ni ne s'organisent en équipe pour travailler ensemble sur un même projet ou une même tache
  - Le travail est fractionné en fonction de la taille des projets (pour une personne aux connaissances pointues dans un domaine donné) ; ce qui implique que chaque membre est cloisonné dans sa spécialité (autrement dit, il s'agit d'une organisation en silo qui n'est pas compatible avec la méthodologie de travail Agile)

Pour remédier à ces problèmes, la solution serait donc :
- d'ajouter au bilan hebodomaire existant la méthode Agile du "Daily scrum" (consistant à organiser une brève réunion quotidienne concernant uniquement les membres de l’entreprise travaillant sur le sprint) afin d'avoir un horizon à court terme du travail à réaliser, de façon plus précise et concrète.
- Utiliser l'ordinateur comme un outil de communication et pas simplement comme un outil de calculs mathématiques en encourageant tous les chercheurs et les développeurs à partager leur travail sur un outil de versionning en leur expliquant tout l'intéret qu'il y a à le faire.

Je recommende fortement à tous les colaborateurs (y compris les develloppeurs) d'utiliser Git et GitHub dont les avantages sont les suivants :
- Leader sur le marché des clouds dédiés au code informatique,
- Partage du code, des connaissances et des techniques pour prendre en compte la transversalité des projets
- Code source des projets hébergé dans différents langages de programmation (les autres utilisateurs de GitHub peuvent passer en revue le code et proposer des modifications ou des améliorations)
- Retour en arrière facile en cas d'erreur
- Accès à l'historique des commits (les changements apportés à chaque itération sont gardés en mémoire)


Il aussi faudrait en place un réseau social professionnel pour permettre aux collaborateurs de faire appel les uns aux autres en cas de problème, de faciliter des micro-interventions entre collaborateurs sur des projets précis de façon plus souple (à n'importe quel moment) et pour partager des documents à des personnes en privé (si ce n'est pas pertinent que tout le monde soit au courant de l'avancement d'un travail en cours de réalisation). Sur le marché des applications, il y a par exemples :
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

___

## RECRUTEMENT DE PERSONNEL

Puisque l’entreprise a le budget pour recruter et qu'elle est en pleine croissance interne, il faudrait embaucher des développeurs salariés (avec une vraie expertise) à la place de stagiaires (qui manquent souvent d'expérience) pour augmenter significativement la qualité du code produit ainsi que la notoriété de l'entreprise.

___

## ALLEGEMENT DE LA CHARGE DE TRAITEMENT

Sur le long terme, on peut envisager une découpe du moteur de simulation monolythique en microservices indépendants mais cela demanderait un travail très conséquent et qu'il ne s'agit pas là du besoin exprimé par SIBIS.

Afin de décharger le moteur de simulation monolythique de certaines responsabilités, il serait préférable de créer d'autres services (ou programmes).

**VEILLE SUR GATEWAY**



## INTEGRATION CONTINUE

A l'heure actuelle, il n'y a ni chaine d'outils automatisés, ni 

- "Processus de Production Archaïque (compilation et un déploiement manuels)"
- "Absence de Tests Automatisés"
  - situation actuelle : de nombreuses taches récurentes doivent être opérées par l'équipe de développement à chaque nouvelle mise en production de l'application (les tests et le deploiment), engendrant une perte de temps considérable et un risque d'erreur non négligeable
  - solution : opter pour de l'intégration continue pour conditionner la **dockerisation** à la **validation des tests** (grâce) et de l'absence d'erreurs statiques ou dynamiques (grâce à un Linter et un debuggeur) ; un système devra ensuite récupérer l'image dockérisée puis la mettre en production automatiquement (sur un hébergeur de projets en ligne) 


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
- EsLint
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
 


## BIBLIOGRAPHIE

https://www.panda3d.org/

https://www.panda3d.org/features/

https://unity.com/fr/products/unity-simulation-pro

https://foxform3d.com/18-bonnes-raisons-dutiliser-unity/

https://www.unrealengine.com/fr/unreal-engine-5

https://blog-gestion-de-projet.com/manifeste-agile-valeurs-et-principes/#t-1621593889298

https://www.reussirsesprojets.com/avantages-methodes-agiles/

https://solutions.lesechos.fr/bureau-coworking/c/les-avantages-et-inconvenients-de-lopen-space-7695/

https://barrazacarlos.com/fr/avantages-et-inconvenients-du-logiciel-com-du-lundi/

https://meilleurs-logiciels.com/trello-fonctionnalites-prix-avis-avantages-et-inconvenients/

https://datascientest.com/github-tout-savoir

https://tecnobits.com/fr/cuales-son-las-principales-ventajas-de-slack/

https://slack.com/intl/fr-fr/resources/why-use-slack/the-value-of-slack-for-software-developers

https://www.sales-hacking.com/outils/quora

https://barrazacarlos.com/fr/avantages-et-inconvenients-de-la-discorde/
