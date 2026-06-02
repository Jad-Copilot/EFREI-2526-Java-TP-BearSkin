# Rapport BearSkin - martinantoninflorent

## Équipe
- Martin PINEAU
- Florent DEBAUF
- Antonin DAS NEVES

## Step 1 : Mécanique basique
**Complétion** : 100%
**Approche** : Comportements séparés (`*Behaviour`) avec état partagé, marché de prêt dédié et mécanismes de concurrence plus poussés.
**Points forts** : Les mécaniques de base sont couvertes et l’équipe a réfléchi aux cas concurrents (jumeaux, citadins, prêts).
**Points faibles** : La solution est assez lourde pour le sujet et multiplie les mécanismes annexes.

## Step 2 : Spécialisations (Strategy)
**État** : Complet
**Spécialisations** : prêteur, jumeaux, faussaire, citadin
**Implémentation** : Le polymorphisme est réel, mais il ne passe pas par une Strategy “pure” ; on a davantage une famille de comportements coordonnés.
**Problèmes** : Conception plus complexe que nécessaire ; risque de sur-ingénierie.

## Dépendances
`bear-ecosystem-core` uniquement. Aucun Spring Data JDBC, JPA/Hibernate ou JDBC custom.

## Analyse IA
**Estimation** : 45%
**Indices** : README détaillé mais pas “parfait”, présence d’arbitrages concrets et de choix techniques moins lisses qu’un rendu purement généré.

## Notes globales
Le groupe a clairement travaillé les aspects concurrence et coordination. C’est riche, mais parfois trop ambitieux pour rester simple.
