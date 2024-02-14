# IDEES NON-RETENUES








______ ANCIENNES QUESTIONS ______

1. **Décomposition en Microservices :**

  - Quelles fonctionnalités spécifiques de l'application peuvent être transformées en microservices indépendants ?

    Pour améliorer l’agilité de développement, le déploiement, la tolérance de panne et la scalabilité, il serait préférable de prévoir au moins un microservice dédié pour chaque domaine d'activité différent géré par le backend de l'application le décomposant en microservices les fonctionnalités suivantes :

### CRUD (Create, Read, Update, Delete) pour chaque catégorie de données de la base de données :
    - la gestion des utilisateurs ?
    - la gestion de l'analyse des chercheurs selon leur branche d'activité ?

### Calcul de données par le moteur de simulation (en C++)
    - le calcul de la dynamique de la structure et de la glace par le **moteur de simulation**

### Formatage des fichiers (ensemble des routines) :
    - le prétraitement des fichiers d’entrée
    - le post-traitement des résultats (comme les graphes ou les animations) 

Schéma de représentation des Liaisons entre les domaines d'activité et les microservices :
https://www.canva.com/design/DAF7iPuA48o/8uspwdGiu45F0l29lyHMrg/edit?ui=eyJHIjp7fX0


// DECRIRE L'INTERET D'UTILISER L'API GATEWAY :

Pour permettre la communication entre les différents microservices, il est nécessaire de mettre en place une API Gateway

Pour cacher au client LA complexité des emplacements de chaque instance du service utilisé, en passant plutôt par l’API Gateway qui joue le rôle d'intermédiaire entre les clients et les microservices qui lui sont disponibles.


Schéma de représentation de Gestion des microservices par l’API Gateway :
https://www.canva.com/design/DAF7iPuA48o/8uspwdGiu45F0l29lyHMrg/edit?ui=eyJHIjp7fX0


___

  - Comment assurer la cohérence et la communication entre les équipes travaillant sur différents microservices ?
    - trouver un framework d'API qui est compatible avec les microservices et qui peut interpretter les langages C++ et MatLab (ne pas proposer NextJS car c'est du fullstack et que les programmes sont uniquement écrit en JavaScript)
    -

    // Pour chaque micoservice, utiliser une api de type Restfull (compatible avec Matlab et C++)
https://www.mathworks.com/help/mps/restfuljson/restful-api.html
https://stackoverflow.com/questions/9788572/ways-to-implement-a-json-restful-service-in-c-c


L'application a vocation a être utilisé sur un ordinateur car c'est sur ce périphérique que sont utilisé les languages existants C++ et MatLab.


___

2. **Containerisation avec Docker :**

  - Comment Docker peut-il être utilisé pour containeriser chaque microservice ?





A l'heure actuelle, à part le logiciel MatLab (qui utilise le language du même nom), il n'y a pas d'interface graphique. Il faut donc créer entièrement la partie Frontend de l'application pour accèder aux modules de visualisation haute fidélité. Il faudra aussi dockeriser le Frontend !

___

  - Comment gérer les dépendances entre microservices dans un environnement Dockerisé ?

___

3. **Orchestration avec Kubernetes :**

  - Pourquoi Kubernetes est-il essentiel pour orchestrer le déploiement des microservices ?

___

  - Comment garantir la flexibilité et l'évolutivité des microservices grâce à Kubernetes ?

___

4. **Chaîne CI/CD Automatisée :**

  - Comment mettre en place une chaîne CI/CD tenant compte de la séparation entre les équipes scientifiques et de production ?

___

  - Quelles étapes spécifiques doivent être automatisées pour garantir un processus CI/CD fiable ?

___

5. **Tests Automatisés :**

  - Comment intégrer des tests automatisés à chaque étape du processus CI/CD ?

___

  - Quels types de tests sont essentiels pour assurer la stabilité des microservices ?

___

6. **Surveillance et Logging :**

  - Comment mettre en place une surveillance efficace des microservices en production ?

  ___

  - Quels mécanismes de logging peuvent aider à identifier rapidement les problèmes potentiels ?










> Schéma avec les 2 options :
  - modules existants + futures modules sous forme d'une app monolytique (où le backend ne contient qu'une API)
  - modules existants + futures modules sous forme d'une app en mi (où le backend est divisé en plusieurs API)


  A l'heure actuelle, à part le logiciel MatLab (qui utilise le language du même nom), il n'y a pas d'interface graphique.
  Il faut donc créer entièrement la partie Frontend de l'application pour accèder aux modules de visualisation haute fidélité.

  L'application a vocation a être utilisé sur un ordinateur car c'est sur ce périphérique que sont utilisé les languages existans C++ et MatLab.

  ____








  ### VEILLES SUR LES OUTILS DE L'INTEGRATION CONTINUE

> Peut-être le mettre uniquement dans l'autre dossier ?

#### VEILLE SUR 

Voici une comparaison entre plusieurs outils de pré-commit :
1. Husky
2. 

Voici les avantages de Husky :
-
-
-
-





#### VEILLE SUR 

Voici une comparaison entre plusieurs linters :
- EsLint + Prettier (formatage du )
- 

#### VEILLE SUR 

Voici une comparaison entre plusieurs outils de testing :
- Vitest
- Jest
- etc.

#### VEILLE SUR 

Voici une comparaison entre plusieurs outils dockerisation :
  - Docker
  -

#### VEILLE SUR 

Voici une comparaison entre plusieurs outils de déploiement :
  - Versel
  - etc.




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
 
