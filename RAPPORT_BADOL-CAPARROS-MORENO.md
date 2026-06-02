# Rapport BearSkin - badol-caparros-moreno

## Équipe
- Léo BADOL
- Alex MORENO
- Malo CAPARROS

## Step 1 : Mécanique basique
**Complétion** : 100%
**Approche** : Architecture propre autour de `BaseHunter`, `Inventory`, `HunterCoordinator` et stratégies dédiées.
**Points forts** : Step 1 complet : prêt, achat fusil, achat chien, chasse, vente/remboursement. Code lisible et bien factorisé.
**Points faibles** : Très proche de `goldteam`, ce qui affaiblit l’originalité du rendu.

## Step 2 : Spécialisations (Strategy)
**État** : Complet
**Spécialisations** : prêteur, jumeaux, faussaire, citadin
**Implémentation** : Le DP Strategy est bien appliqué : `BaseHunter.run()` délègue à des stratégies spécialisées, avec coordination centrale.
**Problèmes** : Faussaire limité par le JAR core, mais c’est documenté et non pénalisant ici.

## Dépendances
`bear-ecosystem-core` uniquement. Aucun Spring Data JDBC, JPA/Hibernate ou JDBC custom.

## Analyse IA
**Estimation** : 55%
**Indices** : Structure très propre, noms de classes textbook (`BaseHunter`, `HunterCoordinator`, `Inventory`), patterns appliqués de façon très scolaire.

## Notes globales
C’est l’un des rendus les plus solides du lot. Le principal point d’attention est la forte proximité avec `goldteam`.
