# Rapport BearSkin - bouzelouf-team

## Équipe
- Rayane EL YOUNSI
- Julien VOUILLOZ
- Dorian POLICE

## Step 1 : Mécanique basique
**Complétion** : 100%
**Approche** : Hunter central (`HunterTest`/`AbstractHunter`) piloté par des stratégies concrètes et quelques services maison.
**Points forts** : Les bases du TP sont là et le repo tente de simuler plusieurs profils de chasseurs avec un main assez clair.
**Points faibles** : L’architecture reste monolithique, avec beaucoup de logique conservée dans les classes centrales.

## Step 2 : Spécialisations (Strategy)
**État** : En cours
**Spécialisations** : prêteur, faussaire, citadin
**Implémentation** : Le principe Strategy existe, mais l’abstraction est incomplète et la spécialisation “jumeaux” est absente.
**Problèmes** : Pas de jumeaux. Polymorphisme moyen. Dépendance `datafaker` ajoutée surtout pour l’habillage des logs.

## Dépendances
`bear-ecosystem-core` + `datafaker`. Aucun Spring Data JDBC, JPA/Hibernate ou JDBC custom.

## Analyse IA
**Estimation** : 45%
**Indices** : README générique, noms très standards, mais code assez spécifique et irrégulier, avec moins de perfection “IA” que d’autres rendus.

## Notes globales
Repo fonctionnel sur le socle, mais Step 2 reste partiel. Le rendu paraît plus artisanal et moins terminé que les meilleurs groupes.
