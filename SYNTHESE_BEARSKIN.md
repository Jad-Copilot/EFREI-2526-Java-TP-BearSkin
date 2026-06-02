# Synthèse BearSkin

## Tableau récapitulatif

| Groupe | Step 1 | Step 2 | IA | Notes |
|---|---:|---|---:|---|
| CrazyTeddyBears | 75% | En cours | 75% | Bonne intention architecturale, exécution incomplète |
| badol-caparros-moreno | 100% | Complet | 55% | Très solide, très proche de goldteam |
| bouzelouf-team | 100% | En cours | 45% | Socle correct, jumeaux absents |
| goldteam | 100% | Complet | 55% | Très solide, très proche de badol-caparros-moreno |
| jad-alone *(repo exemple)* | 25% | Non commencé | 10% | Squelette de référence, pas un vrai rendu final |
| kikou974 | 100% | En cours | 50% | Rendu sérieux mais plus orienté héritage que Strategy |
| les-egares | 100% | En cours | 35% | Très bonne architecture, citadin moins stabilisé |
| les-petits-pedestres | 100% | Complet | 60% | Complet, mais solution un peu sur-construite |
| maerma | 100% | Complet | 70% | Très bon rendu, finition élevée |
| martinantoninflorent | 100% | Complet | 45% | Beaucoup d’idées, architecture assez lourde |
| matias-bastien-tristan | 100% | En cours | 40% | Bonne conception, Step 2 inachevé |
| ouapanu | 75% | Complet | 55% | Structure intéressante, démonstration partielle |

## Observations par thème

### Points forts récurrents
- La majorité des groupes ont bien couvert le **Step 1** : prêt, équipement, chasse, vente et remboursement.
- Le **DP Strategy** est généralement compris, même lorsqu’il est mélangé avec héritage, Decorator, Observer ou des services de coordination.
- Plusieurs groupes ont fait un vrai effort sur la **concurrence** et la coordination entre chasseurs (files, état partagé, marchés de prêt, citadins intermédiaires).

### Problèmes récurrents
- **Aucun repo n’utilise Spring Data JDBC / JPA / JDBC custom** : tous s’appuient essentiellement sur `bear-ecosystem-core`, avec parfois `lombok` ou `datafaker`.
- **Pas de tests** observés dans les dépôts.
- Les builds Maven n’ont pas pu être validés proprement car la dépendance `bear-ecosystem-core` renvoie un **401 GitHub Packages** dans cet environnement ; ce point n’a donc pas été retenu contre les étudiants.
- Quelques rendus ont des **incohérences de pom** (`lombok` importé mais non déclaré) ou une démonstration incomplète au runtime.
- Le **citadin** et les **jumeaux** sont souvent les spécialisations les plus fragiles à stabiliser.

### Patterns IA / similitudes observées
- Vocabulaire très générique dans plusieurs repos : `BaseHunter`, `HunterCoordinator`, `Inventory`, `ClassicHunterStrategy`.
- Tendances “textbook” fréquentes : Strategy bien découpé, README très propre, justification très académique des patterns.
- Deux repos ressortent comme **très proches** : `badol-caparros-moreno` et `goldteam`.
- L’assistance IA semble surtout perceptible dans les README très lissés et dans les architectures extrêmement scolaires, plus que dans un code “parfait”.

## Recommandations pédagogiques
- Insister sur la différence entre **héritage** et **Strategy réellement interchangeable**.
- Demander une **preuve d’exécution minimale** ou quelques **tests ciblés** pour éviter les rendus bien documentés mais peu démontrés.
- Vérifier systématiquement la **cohérence `pom.xml` / imports**.
- Encourager des solutions **plus simples mais complètes** plutôt que des architectures ambitieuses inachevées.
- Pour les prochains TP, prévoir un point de contrôle intermédiaire sur les spécialisations difficiles (**jumeaux**, **citadin**).
