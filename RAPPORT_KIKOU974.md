# Rapport BearSkin - kikou974

## Équipe
- David CHOCHO
- Alexis BRYON
- Manon AUBRY

## Step 1 : Mécanique basique
**Complétion** : 100%
**Approche** : Approche orientée héritage avec plusieurs sous-classes concrètes de chasseurs.
**Points forts** : Step 1 bien couvert et les 4 rôles de Step 2 sont présents dans le code.
**Points faibles** : Le polymorphisme repose plus sur des sous-classes spécialisées que sur une vraie Strategy interchangeable.

## Step 2 : Spécialisations (Strategy)
**État** : En cours
**Spécialisations** : prêteur, jumeaux, faussaire, citadin
**Implémentation** : Les spécialisations existent, mais la conception est plus rigide qu’attendu et certaines parties ressemblent à des contournements.
**Problèmes** : Import Lombok dans le code sans dépendance Lombok dans le `pom.xml` ; risque de build cassé même hors problème 401.

## Dépendances
`bear-ecosystem-core` uniquement déclaré. Aucun Spring Data JDBC, JPA/Hibernate ou JDBC custom. Import Lombok non déclaré dans le pom.

## Analyse IA
**Estimation** : 50%
**Indices** : Code assez propre et pédagogique, mais avec des incohérences concrètes (dépendances, rigidité des classes) qui cassent l’effet “généré parfait”.

## Notes globales
Le rendu est sérieux et couvre bien le sujet. Le principal défaut est un design plus orienté héritage que Strategy, avec quelques soucis de cohérence technique.
