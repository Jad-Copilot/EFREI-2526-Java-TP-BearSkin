# Rapport BearSkin - les-petits-pedestres

## Équipe
- Aymeric MOREIRA
- Eliott SCHNEIDER
- Elouan LE MERLE

## Step 1 : Mécanique basique
**Complétion** : 100%
**Approche** : Architecture centrée sur `AbstractHunter` avec délégation comportementale et usage de lambdas/interfaces fonctionnelles.
**Points forts** : Step 1 complet et les 4 spécialisations sont bien représentées.
**Points faibles** : Le code mélange parfois logique métier et lambdas de spécialisation, ce qui nuit à la lisibilité.

## Step 2 : Spécialisations (Strategy)
**État** : Complet
**Spécialisations** : prêteur, jumeaux, faussaire, citadin
**Implémentation** : Strategy présent, mais sous une forme plus “fonctionnelle” que classique. C’est intéressant, même si moins lisible qu’une hiérarchie dédiée.
**Problèmes** : Le recours à Lombok en `compile` alourdit inutilement un TP aussi simple.

## Dépendances
`bear-ecosystem-core` + `lombok`. Aucun Spring Data JDBC, JPA/Hibernate ou JDBC custom.

## Analyse IA
**Estimation** : 60%
**Indices** : Code homogène, découpage assez générique, formulations et patterns très scolaires, avec une certaine “propreté de surface”.

## Notes globales
Le rendu est complet et plutôt sérieux. La solution est moins simple qu’elle ne devrait l’être, mais elle reste cohérente.
