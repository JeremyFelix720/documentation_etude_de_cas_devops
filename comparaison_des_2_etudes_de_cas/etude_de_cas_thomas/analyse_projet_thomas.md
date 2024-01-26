# ANALYSE DU PROJET PROPOSE PAR THOMAS

## MOTS-CLE IMPORTANTS REGROUPES EN CATEGORIES (avec pour chacun d'entre eux : les outils à utiliser + des shémas à réaliser)

___
### SPECIALISATIONS
- société de création d'outils de diagnostique dans le contrôle qualité
- mesure de la qualité de l'air, de l'eau, des sols, l'étude de la biodiversité, etc.
- logiciel de bureau par défaut accessible par le web

___
### LANGUAGES UTILISES


___
### LANGUAGES UTILISES
- Javascript par le biais de typescript.
-

___
### FONCTIONNEMENT INTERNE

- 5 squads de 10 developpeurs. Chaque squad possède 1 Product Owner, 1 Scrum Master, 1 Lead Dev, 1 QA + une équipe de DX (Developer Experience), là où a été intégré.

___
### FORCES

- l’entreprise recrute et est en pleine croissance interne (ex. : développeurs seniors full stack Javascript qui ont déjà utilisé React Native et Electron)


___
### POINTS DE BLOCAGE

- beaucoup de petits projets, tous stockés dans des repositories différents

- fonctionnalités nécessitant de faire des modifications dans plusieurs repositories différents

- il n'y aucun test, ni aucune doc sur la partie front
  - solution : mettre en place des tests e2e et une bibliothèque de composants

- beaucoup de mal à analyser les erreurs rencontrées par nos utilisateurs
  - solution : 


___
### BESOINS EXPRIMES
- développement d'une application (pour configurer nos produits sur Android et iOS) sur mobile avec React Native et web avec Electron, tout en gardant nos ressources communes

- gérer les modifications des fonctionnalités de manière centralisée, et pouvoir les déployer de manière centralisée
  - Actuellement : pour chaque repository modifié, il faut faire une pull request, attendre la validation, puis faire une release, puis attendre la validation, puis déployer, puis attendre la validation.
  - Solution : faire un "monorepo" pour rassembler tous les répertoires dans un même répertoire, pour que 

-


___
## BENCHMARK DES OUTILS POUR CHAQUE BESOIN IDENTIFIE


___
## SHEMAS EXPLICATIFS A REALISER
- intégration continue
-


___
## QUESTIONS A POSER AU FORMATEUR