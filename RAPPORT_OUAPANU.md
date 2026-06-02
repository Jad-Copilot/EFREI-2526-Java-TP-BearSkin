# Rapport BearSkin - ouapanu

## Équipe
- AMARAL SARAIVA Paulo
- MOREIRA RIBEIRO Nuno
- NAIB Oualid

## Step 1 : Mécanique basique
**Complétion** : 75%
**Approche** : Ville/forêt encapsulées en singletons, avec chasseurs spécialisés et comportements dédiés.
**Points forts** : Les spécialisations sont bien identifiables et la séparation ville/forêt est lisible.
**Points faibles** : Le `Main` ne lance que des `TwinsHunter`, ce qui limite la démonstration réelle des autres profils.

## Step 2 : Spécialisations (Strategy)
**État** : Complet
**Spécialisations** : prêteur, jumeaux, faussaire, citadin
**Implémentation** : Le polymorphisme existe, mais l’architecture repose sur plusieurs singletons et sur une démonstration d’exécution assez orientée “jumeaux”.
**Problèmes** : Imports Lombok dans le code alors que le `pom.xml` ne déclare pas Lombok ; cohérence de build douteuse même hors 401.

## Dépendances
`bear-ecosystem-core` uniquement déclaré. Aucun Spring Data JDBC, JPA/Hibernate ou JDBC custom. Imports Lombok non déclarés dans le pom.

## Analyse IA
**Estimation** : 55%
**Indices** : Architecture très cadrée, noms très génériques, découpage assez scolaire, mais avec des incohérences concrètes qui limitent l’impression “100% IA”.

## Notes globales
Repo intéressant sur la structure, moins convaincant sur la démonstration globale. Il y a de bonnes idées, mais l’exécution semble partielle.
