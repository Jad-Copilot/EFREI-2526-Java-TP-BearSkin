# Grille de notation BearSkin - EFREI 2526

> Méthode: les sous-critères Step 1 totalisent 17 points bruts et ceux du Step 2 totalisent 13 points bruts. J'ai normalisé ces scores sur **/15** et **/10** pour respecter la grille demandée.  
> Compilation: les `mvn package`/`mvn test` des 11 dépôts échouent dans cet environnement à cause d'une dépendance privée inaccessible (`com.jad:bear-ecosystem-core:1.0.0`, GitHub Packages, **401 Unauthorized**). J'ai donc mis **0/1** au critère compilation pour tout le monde, de manière uniforme et explicite.

## Résumé des notes

| Groupe | Step1 (/15) | Step2 (/10) | Qualité (/5) | Bonus | Note/20 | Tentative Exploit |
|--------|-------------:|------------:|-------------:|------:|--------:|------------------|
| CrazyTeddyBears | 3.0 | 5.0 | 3.0 | +2 | 9.3 | ✓ Documentée |
| badol-caparros-moreno | 15.0 | 10.0 | 3.0 | +2 | 20.0* | ✓ Documentée |
| bouzelouf-team | 13.0 | 8.0 | 3.0 | +2 | 18.0 | ✓ Tentée |
| goldteam | 15.0 | 10.0 | 3.0 | +2 | 20.0* | ✓ Tentée |
| kikou974 | 13.0 | 10.0 | 2.0 | +2 | 18.7 | ✓ Tentée |
| les-egares | 15.0 | 10.0 | 3.0 | +2 | 20.0* | ✓ Documentée |
| les-petits-pedestres | 9.0 | 9.0 | 2.0 | +1 | 14.3 | ✓ Documentée |
| maerma | 15.0 | 10.0 | 3.0 | +2 | 20.0* | ✓ Documentée |
| martinantoninflorent | 9.0 | 7.0 | 3.0 | +0 | 12.7 | ✗ Aucune claire |
| matias-bastien-tristan | 15.0 | 9.2 | 3.0 | +2 | 20.0* | ✓ Documentée |
| ouapanu | 12.9 | 8.5 | 3.0 | +1 | 17.3 | ✓ Échec assumé |

\* note plafonnée à 20.

## Analyse détaillée par groupe

### 1. CrazyTeddyBears
**Équipe** : Marie TASSEL, Maël GADOU, Cassiopée GHIZELLAOUI

**État du développement** : bonne intention d'architecture et README excellent, mais beaucoup de logique reste au stade squelette/commentaires.

**Step 1** : **3.0/15**
- Prêt : **1/3** — spécialisation présente, logique très partielle
- Fusil + Chien : **1/3** — structures prévues, peu actives
- Chasse fonctionnelle : **0/3** — flux réel peu exploitable
- Vente peaux + remboursement : **1/3** — intention visible, exécution faible
- Objectif 50 brouzoufs : **0/2** — surtout documenté
- Code structuré : **1/3** — classes séparées, mais beaucoup de code inachevé

**Step 2** : **5.0/10**
- Strategy : **1/3** — `ISpecialisation`, `AbstractSpecialisation`
- Prêteur : **1/2** — rôle dédié
- Jumeaux : **1/2** — partage/synchronisation esquissés
- Faussaire / exploit : **2/2** — très bien expliqué
- Citadin : **1/2** — spécialisation prévue
- Polymorphisme : **1/2** — base correcte mais peu aboutie

**DP utilisés**
- Strategy : **Oui** — `ISpecialisation`
- Decorator : **Oui** — `BehaviorDecorator`, `ForgerSpecialisation`
- Singleton : **Non**
- Factory : **Non**
- Observer : **Non**
- Template Method : **Non**
- Autres : verrou global / partage d'état rudimentaire

**Tentative faussaire / exploit** : **Oui**
- Stratégie : double dépense / aliasing de paiement + faussaire
- Résultat : concept intéressant, pas vraiment validé par le code visible
- Documentation : **excellente**

**Qualité** : **3/5** — README 2/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- Très bon README
- DP explicités proprement

**Faiblesses**
- Implémentation réelle trop incomplète
- Peu de comportement vérifiable en Step 1

**Total** : **9.3/20**

---

### 2. badol-caparros-moreno
**Équipe** : BADOL Léo, CAPARROS Malo, MORENO Alex

**État du développement** : dépôt très solide, complet sur Step 1 et Step 2, avec bonne structuration et bonne explication des choix.

**Step 1** : **15.0/15**
- Prêt : **3/3** — prêt et dette bien gérés
- Fusil + Chien : **3/3** — achat/location propres
- Chasse fonctionnelle : **3/3** — boucle opérationnelle
- Vente peaux + remboursement : **3/3** — workflow complet
- Objectif 50 brouzoufs : **2/2** — objectif explicite
- Code structuré : **3/3** — packages `hunter/strategy/shared`

**Step 2** : **10.0/10**
- Strategy : **3/3** — cœur du design
- Prêteur : **2/2**
- Jumeaux : **2/2**
- Faussaire / exploit : **2/2** — tentative reconnue et argumentée
- Citadin : **2/2**
- Polymorphisme : **2/2**

**DP utilisés**
- Strategy : **Oui** — `HunterStrategy`, `BasicHunterStrategy`
- Decorator : **Oui** — `ForgedBearSkin`
- Singleton : **Non**
- Factory : **Non**
- Observer : **Non**
- Template Method : **Non**
- Autres : coordinator / producer-consumer

**Tentative faussaire / exploit** : **Oui**
- Stratégie : wrapper `ForgedBearSkin`
- Résultat : **échoue** face aux vérifications de la lib
- Documentation : **très bonne**

**Qualité** : **3/5** — README 2/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- Très bonne architecture
- Step 2 complet et cohérent

**Faiblesses**
- Pas de tests
- Exploit bloqué par la lib

**Total** : **20.0/20** (plafonné)

---

### 3. bouzelouf-team
**Équipe** : Rayane EL YOUNSI, Julien VOUILLOZ, Dorian POLICE

**État du développement** : projet bien avancé, bon coverage fonctionnel, un peu moins propre sur certains choix de nommage et sans vraie gestion des jumeaux.

**Step 1** : **13.0/15**
- Prêt : **3/3**
- Fusil + Chien : **3/3**
- Chasse fonctionnelle : **3/3**
- Vente peaux + remboursement : **3/3**
- Objectif 50 brouzoufs : **2/2**
- Code structuré : **2/3** — structure correcte, un peu confuse par endroits

**Step 2** : **8.0/10**
- Strategy : **3/3**
- Prêteur : **2/2**
- Jumeaux : **0/2** — absent ou non abouti
- Faussaire / exploit : **2/2**
- Citadin : **2/2**
- Polymorphisme : **2/2**

**DP utilisés**
- Strategy : **Oui** — `ClassicHunterStrategy`, `LenderStrategy`, `UrbanStrategy`
- Decorator : **Oui** — faux skin/wrapper implicite
- Singleton : **Non**
- Factory : **Non**
- Observer : **Non**
- Template Method : **Non**
- Autres : `BlockingQueue`, `CompletableFuture`, contrat de location

**Tentative faussaire / exploit** : **Oui**
- Stratégie : peau falsifiée en mémoire
- Résultat : tentative crédible mais fragile
- Documentation : présente

**Qualité** : **3/5** — README 2/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- Fonctionnellement riche
- Bon traitement prêteur/citadin

**Faiblesses**
- Pas de jumeaux aboutis
- Design un peu moins net que les meilleurs groupes

**Total** : **18.0/20**

---

### 4. goldteam
**Équipe** : Elias KHALLOUK, Wissam SHAABAN, Yiannis LEBLANC

**État du développement** : dépôt très complet, modulaire et lisible, bonne couverture de tous les profils demandés.

**Step 1** : **15.0/15**
- Prêt : **3/3**
- Fusil + Chien : **3/3**
- Chasse fonctionnelle : **3/3**
- Vente peaux + remboursement : **3/3**
- Objectif 50 brouzoufs : **2/2**
- Code structuré : **3/3**

**Step 2** : **10.0/10**
- Strategy : **3/3**
- Prêteur : **2/2**
- Jumeaux : **2/2**
- Faussaire / exploit : **2/2**
- Citadin : **2/2**
- Polymorphisme : **2/2**

**DP utilisés**
- Strategy : **Oui**
- Decorator : **Non** (faussaire présent, mais pas sous forme de décorateur net)
- Singleton : **Non**
- Factory : **Non**
- Observer : **Non**
- Template Method : **Non**
- Autres : coordinator/service central

**Tentative faussaire / exploit** : **Oui**
- Stratégie : `ForgerStrategy` + `ForgedBearSkin`
- Résultat : plausible dans leur code
- Documentation : correcte

**Qualité** : **3/5** — README 2/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- Très bon découpage
- Step 1 et Step 2 quasi complets

**Faiblesses**
- Peu de tests
- Peu d'autres patterns explicites hors Strategy

**Total** : **20.0/20** (plafonné)

---

### 5. kikou974
**Équipe** : David CHOCHO, Alexis BRYON, Manon AUBRY

**État du développement** : projet très fonctionnel, bon coverage Step 2, mais structure Step 1 plus monolithique.

**Step 1** : **13.0/15**
- Prêt : **3/3**
- Fusil + Chien : **3/3**
- Chasse fonctionnelle : **3/3**
- Vente peaux + remboursement : **3/3**
- Objectif 50 brouzoufs : **2/2**
- Code structuré : **1/3** — assez procédural / classes lourdes

**Step 2** : **10.0/10**
- Strategy : **3/3**
- Prêteur : **2/2**
- Jumeaux : **2/2**
- Faussaire / exploit : **2/2**
- Citadin : **2/2**
- Polymorphisme : **2/2**

**DP utilisés**
- Strategy : **Oui** — `BehaviourStrategy`
- Decorator : **Non**
- Singleton : **Oui** — `BehaviourFactory.getInstance()`
- Factory : **Oui** — `BehaviourFactory`
- Observer : **Non**
- Template Method : **Non**
- Autres : Mediator annoncé / file d'attente côté citadin

**Tentative faussaire / exploit** : **Oui**
- Stratégie : `ForgerHunter`, amélioration de peau avant vente
- Résultat : tentative bien intégrée
- Documentation : correcte

**Qualité** : **2/5** — README 1/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- DP très visibles
- Step 2 complet

**Faiblesses**
- Architecture moins élégante
- `HunterTest` est trompeur (pas un vrai test)

**Total** : **18.7/20**

---

### 6. les-egares
**Équipe** : Théo LUGAGNE, Tom BOUDEVILLE-REQUIER

**État du développement** : architecture riche et bien pensée, probablement l'une des plus ambitieuses, malgré un faussaire qui semble bogué.

**Step 1** : **15.0/15**
- Prêt : **3/3**
- Fusil + Chien : **3/3**
- Chasse fonctionnelle : **3/3**
- Vente peaux + remboursement : **3/3**
- Objectif 50 brouzoufs : **2/2**
- Code structuré : **3/3**

**Step 2** : **10.0/10**
- Strategy : **3/3**
- Prêteur : **2/2**
- Jumeaux : **2/2**
- Faussaire / exploit : **2/2**
- Citadin : **2/2**
- Polymorphisme : **2/2**

**DP utilisés**
- Strategy : **Oui**
- Decorator : **Non**
- Singleton : **Oui** — `BehaviourFactory`
- Factory : **Oui** — `BehaviourFactory`
- Observer : **Non**
- Template Method : **Non**
- Autres : Mediator (`HunterDialog`, `HuntersInteractionService`)

**Tentative faussaire / exploit** : **Oui**
- Stratégie : `FakerHunter` / `FakerBehaviour`
- Résultat : idée présente, implémentation probablement inefficace
- Documentation : bonne

**Qualité** : **3/5** — README 2/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- Très bon niveau architectural
- Variantes complètes et bien isolées

**Faiblesses**
- Faussaire fragile
- Complexité concurrente plus risquée

**Total** : **20.0/20** (plafonné)

---

### 7. les-petits-pedestres
**Équipe** : Elouan LE MERLE, Eliott SCHNEIDER, Aymeric MOREIRA

**État du développement** : bonne idée de séparation par comportements, mais projet moins robuste et moins documenté que les meilleurs.

**Step 1** : **9.0/15**
- Prêt : **2/3**
- Fusil + Chien : **2/3**
- Chasse fonctionnelle : **2/3**
- Vente peaux + remboursement : **2/3**
- Objectif 50 brouzoufs : **1/2**
- Code structuré : **2/3**

**Step 2** : **9.0/10**
- Strategy : **3/3** — interfaces `IBehavior*`
- Prêteur : **2/2**
- Jumeaux : **2/2**
- Faussaire / exploit : **2/2**
- Citadin : **2/2**
- Polymorphisme : **2/2**

**DP utilisés**
- Strategy : **Oui**
- Decorator : **Non**
- Singleton : **Non**
- Factory : **Non**
- Observer : **Non**
- Template Method : **Oui, partiel** — `AbstractHunter.run()` impose un squelette
- Autres : composition par comportements / lambdas

**Tentative faussaire / exploit** : **Oui**
- Stratégie : réflexion sur `BearSkinRecord`
- Résultat : probablement en échec, mais démarche clairement tentée
- Documentation : présente

**Qualité** : **2/5** — README 1/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- Step 2 bien couvert
- Bonne utilisation de comportements injectés

**Faiblesses**
- Step 1 plus faible
- Faussaire très fragile

**Total** : **14.3/20**

---

### 8. maerma
**Équipe** : Maxime DESCHAMPS, Erwan GODELLE, Mathis TOCQUES

**État du développement** : l'un des dépôts les plus propres et les plus convaincants, avec très bonne lisibilité et Step 2 complet.

**Step 1** : **15.0/15**
- Prêt : **3/3**
- Fusil + Chien : **3/3**
- Chasse fonctionnelle : **3/3**
- Vente peaux + remboursement : **3/3**
- Objectif 50 brouzoufs : **2/2**
- Code structuré : **3/3**

**Step 2** : **10.0/10**
- Strategy : **3/3**
- Prêteur : **2/2**
- Jumeaux : **2/2**
- Faussaire / exploit : **2/2**
- Citadin : **2/2**
- Polymorphisme : **2/2**

**DP utilisés**
- Strategy : **Oui** — `HunterStrategy` + stratégies dédiées
- Decorator : **Oui** — `ForgedBearSkin`
- Singleton : **Non**
- Factory : **Non**
- Observer : **Non**
- Template Method : **Oui, partiel** — squelette dans `BasicHuntingStrategy`
- Autres : état partagé / coordination

**Tentative faussaire / exploit** : **Oui**
- Stratégie : `ForgedBearSkin`
- Résultat : tentative propre mais bloquée par la lib
- Documentation : **très bonne**

**Qualité** : **3/5** — README 2/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- Très bonne qualité de code
- README complet

**Faiblesses**
- Pas de tests visibles
- Faussaire limité par les protections du JAR

**Total** : **20.0/20** (plafonné)

---

### 9. martinantoninflorent
**Équipe** : Martin PINEAU, Florent DEBAUF, Antonin DAS NEVES

**État du développement** : bonne documentation et bon travail sur les jumeaux, mais Step 2 moins complet faute de faussaire clair.

**Step 1** : **9.0/15**
- Prêt : **2/3**
- Fusil + Chien : **2/3**
- Chasse fonctionnelle : **2/3**
- Vente peaux + remboursement : **2/3**
- Objectif 50 brouzoufs : **1/2**
- Code structuré : **2/3**

**Step 2** : **7.0/10**
- Strategy : **3/3**
- Prêteur : **2/2**
- Jumeaux : **2/2**
- Faussaire / exploit : **0/2** — pas trouvé
- Citadin : **2/2**
- Polymorphisme : **2/2**

**DP utilisés**
- Strategy : **Oui**
- Decorator : **Non**
- Singleton : **Non**
- Factory : **Oui** — `TwinFactory`
- Observer : **Non**
- Template Method : **Non**
- Autres : état partagé / sémaphore

**Tentative faussaire / exploit** : **Non**
- Pas de tentative claire repérée dans README ou code

**Qualité** : **3/5** — README 2/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- Très bon traitement des jumeaux
- README pédagogique

**Faiblesses**
- Pas de faussaire
- Coverage Step 2 incomplet

**Total** : **12.7/20**

---

### 10. matias-bastien-tristan
**Équipe** : Matias ZOCLI, Bastien DUBILE, Tristan PETIT

**État du développement** : dépôt très solide, bien structuré, très bon usage des patterns; seul vrai manque: pas de jumeaux.

**Step 1** : **15.0/15**
- Prêt : **3/3**
- Fusil + Chien : **3/3**
- Chasse fonctionnelle : **3/3**
- Vente peaux + remboursement : **3/3**
- Objectif 50 brouzoufs : **2/2**
- Code structuré : **3/3**

**Step 2** : **9.2/10**
- Strategy : **3/3**
- Prêteur : **2/2**
- Jumeaux : **0/2** — absent
- Faussaire / exploit : **2/2**
- Citadin : **2/2**
- Polymorphisme : **2/2**

**DP utilisés**
- Strategy : **Oui** — `HunterStrategy`, `ClassicHunterStrategy`, `LenderStrategy`, `CityTraderStrategy`
- Decorator : **Oui** — `FakeQualitySellBehavior`, `FakeHighBearSkinQuality`
- Singleton : **Oui** — `RentalDesk.getInstance()`
- Factory : **Non**
- Observer : **Oui** — `EquipmentSubject`, `EquipmentObserver`
- Template Method : **Non**
- Autres : composition de behaviors

**Tentative faussaire / exploit** : **Oui**
- Stratégie : fausse qualité HIGH via décorateur
- Résultat : plausible localement, bien intégré
- Documentation : **très bonne**

**Qualité** : **3/5** — README 2/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- DP nombreux et lisibles
- Très bonne architecture

**Faiblesses**
- Pas de jumeaux
- Pas de tests visibles

**Total** : **20.0/20** (plafonné)

---

### 11. ouapanu
**Équipe** : Paulo AMARAL SARAIVA, Nuno MOREIRA RIBEIRO, Oualid NAIB

**État du développement** : projet sérieux et assez complet, avec bonne honnêteté sur l'échec du faussaire.

**Step 1** : **12.9/15**
- Prêt : **3/3**
- Fusil + Chien : **3/3**
- Chasse fonctionnelle : **2/3** — `HunterTest` peu convaincant
- Vente peaux + remboursement : **2/3**
- Objectif 50 brouzoufs : **2/2**
- Code structuré : **2/3**

**Step 2** : **8.5/10**
- Strategy : **2/3** — comportements présents mais moins homogènes
- Prêteur : **2/2**
- Jumeaux : **2/2**
- Faussaire / exploit : **2/2**
- Citadin : **2/2**
- Polymorphisme : **2/2**

**DP utilisés**
- Strategy : **Oui** — `IHuntBehaviour`, `ISellBehaviour`, `IBuyBehaviour`
- Decorator : **Non**
- Singleton : **Oui** — `City`, `Forest`
- Factory : **Non**
- Observer : **Non**
- Template Method : **Non**
- Autres : state côté prêteur

**Tentative faussaire / exploit** : **Oui**
- Stratégie : cast vers `FakeHighQualityBearSkin`
- Résultat : **échoue** (`ClassCastException` / rejet du JAR)
- Documentation : **oui, honnête**

**Qualité** : **3/5** — README 2/2, doc 1/1, tests 0/1, compilation 0/1

**Points forts**
- README clair
- Jumeaux + prêteur bien traités

**Faiblesses**
- Faussaire cassé
- Architecture moins homogène que les meilleurs

**Total** : **17.3/20**

---

## Synthèse pédagogique

### Points forts généraux
- La majorité des groupes ont **bien compris le pattern Strategy** pour spécialiser les chasseurs.
- Les meilleurs dépôts sont ceux qui ont séparé **état partagé / orchestration / comportements**.
- Les groupes qui ont documenté leur raisonnement obtiennent un vrai bonus pédagogique, même quand le faussaire échoue.

### Exploits / stratagèmes observés
- **Faussaire documenté ou tenté** : CrazyTeddyBears, badol-caparros-moreno, bouzelouf-team, goldteam, kikou974, les-egares, les-petits-pedestres, maerma, matias-bastien-tristan, ouapanu
- **Pas de tentative claire** : martinantoninflorent
- **Échec assumé et bien expliqué** : badol-caparros-moreno, maerma, ouapanu, probablement les-petits-pedestres et les-egares

### Patterns les plus fréquents
- **Très fréquent** : Strategy
- **Assez fréquent** : Factory, Singleton, Decorator (mais plus rare que prévu)
- **Peu vu** : Observer, Template Method
- **Autres patterns repérés** : Mediator, State, Coordinator / Producer-Consumer, partage d'état synchronisé

### Recommandations d'évaluation
1. **Valoriser les tentatives d'exploit** même échouées quand elles sont argumentées.
2. Vérifier particulièrement les **jumeaux** : c'est souvent là que la concurrence devient fragile.
3. Distinguer les dépôts avec vrai **code exécutable** de ceux qui ont surtout une bonne **intention d'architecture**.
4. Garder en tête que le critère compilation est ici **biaisé par l'accès au package privé**, pas forcément par la qualité intrinsèque du code.
