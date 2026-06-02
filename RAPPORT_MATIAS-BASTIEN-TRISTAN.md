# Rapport BearSkin - matias-bastien-tristan

## Équipe
- Matias ZOCLI
- Bastien DUBILE
- Tristan PETIT

## Step 1 : Mécanique basique
**Complétion** : 100%
**Approche** : Strategy + comportements fins (`behavior`) + Observer pour la location + Decorator pour le faussaire.
**Points forts** : Le Step 1 est bien pensé et bien documenté. Le découpage des comportements est clair.
**Points faibles** : Le Step 2 n’est pas fini malgré une bonne base de conception.

## Step 2 : Spécialisations (Strategy)
**État** : En cours
**Spécialisations** : prêteur, faussaire, citadin
**Implémentation** : Strategy bien posé conceptuellement, mais les jumeaux manquent et le prêteur est annoncé comme peu validé.
**Problèmes** : README avoue explicitement l’absence des jumeaux et les difficultés de validation du prêteur.

## Dépendances
`bear-ecosystem-core` uniquement. Aucun Spring Data JDBC, JPA/Hibernate ou JDBC custom.

## Analyse IA
**Estimation** : 40%
**Indices** : Beaucoup d’honnêteté sur les limites, moins de vernis artificiel, malgré une terminologie de patterns assez scolaire.

## Notes globales
Bon socle de conception, mais rendu inachevé sur Step 2. Le groupe a mieux réussi l’architecture que la finalisation.
