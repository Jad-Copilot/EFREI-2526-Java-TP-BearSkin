# SYNTHÈSE FINALE v2.0 - EFREI 2526 BearSkin

**Réanalyse complète avec critères v2.0 (2026-10-20)**

## CLASSEMENT FINAL

| Rang | Groupe | Base/20 | +Hash | +Sort | %IA | Pen | Final/20 | Δ |
|------|--------|---------|-------|-------|-----|-----|----------|-----|
| 1 | goldteam | 20.0 | 0 | 0 | 4% | -0.0 | **20.0** | +0.0 |
| 2 | badol-caparros-moreno | 20.0 | 0 | 0 | 20% | -0.5 | **19.5** | -0.5 |
| 3 | matias-bastien-tristan | 20.0 | 0 | 0 | 32% | -0.5 | **19.5** | -0.5 |
| 4 | les-egares | 20.0 | 0 | 0 | 40% | -1.5 | **18.5** | -1.5 |
| 5 | maerma | 20.0 | 0 | 0 | 40% | -1.5 | **18.5** | -1.5 |
| 6 | bouzelouf-team | 18.0 | 0 | 0 | 28% | -0.5 | **17.5** | -0.5 |
| 7 | kikou974 | 18.7 | 0 | 0 | 44% | -1.5 | **17.2** | -1.5 |
| 8 | ouapanu | 17.3 | 1 | 0 | 52% | -1.5 | **16.8** | -0.5 |
| 9 | les-petits-pedestres | 14.3 | 1 | 0 | 40% | -1.5 | **13.8** | -0.5 |
| 10 | martinantoninflorent | 12.7 | 0 | 0 | 36% | -1.5 | **11.2** | -1.5 |
| 11 | CrazyTeddyBears | 9.3 | 0 | 0 | 40% | -1.5 | **7.8** | -1.5 |
| 12 | jad-alone | 0.0 | 0 | 0 | 20% | -0.5 | **0.0** | +0.0 |


## STATISTIQUES GLOBALES

### Scores

| Métrique | Valeur |
|----------|--------|
| **Score moyen** (base) | 15.86/20 |
| **Score moyen** (final v2) | 15.03/20 |
| **Impact moyen** | -0.83 pts |
| **Meilleur score** | 20.0/20 |
| **Pire score** | 0.0/20 |

### Bonus

| Bonus | Groupes | % |
|-------|---------|-----|
| HashMap Optimization | 2 | 17% |
| Insertion Sorting | 0 | 0% |
| Aucun bonus | 10 | 83% |

### Détection IA

| Taux IA | Groupes | Pénalité typique |
|---------|---------|------------------|
| < 15% | 1 | -0.0 pts |
| 15-35% | 4 | -0.5 pts |
| 35-55% | 7 | -1.5 pts |
| 55-75% | 0 | -3.0 pts |
| > 75% | 0 | -5.0 pts |

**Taux IA moyen détecté**: 33.0%

---

## OBSERVATIONS

### Très bon score (≥ 18/20)
Groupes avec score final ≥ 18 :
goldteam, badol-caparros-moreno, matias-bastien-tristan, les-egares, maerma

**Caractéristiques** :
- Score base très élevé
- Peu de détection IA (< 35%)
- Minimal ou pas de pénalité

### Bon score (15-17.9/20)
Groupes avec score 15-17.9 :
bouzelouf-team, kikou974, ouapanu

**Caractéristiques** :
- Score base bon à très bon
- Détection IA modérée (20-52%)
- Pénalité modérée

### Moyen score (10-14.9/20)
Groupes avec score 10-14.9 :
les-petits-pedestres, martinantoninflorent

**Caractéristiques** :
- Score base moyen
- Détection IA variable
- Pénalité impactante

### Faible score (< 10/20)
Groupes avec score < 10 :
CrazyTeddyBears, jad-alone

**Caractéristiques** :
- Score base très faible
- Forte détection IA ou bonus manquants
- Pénalité sévère

### Analyse IA par critère

#### A. Commentaires/Documentation
- Score 0/5 : 10 groupes (normal)
- Score > 0/5 : 2 groupes (signes IA)

#### B. Getters/Setters vs Diagramme
- Score 0/5 : 1 groupes (parfait)
- Score > 0/5 : 11 groupes (divergence)

#### C. Enums
- Score 0/5 : 12 groupes (correct)
- Score > 0/5 : 0 groupes (patterns suspects)

#### D. Lambdas
- 0 lambdas : 1 groupes
- 1-3 lambdas : 2 groupes
- 4-5 lambdas : 1 groupes
- 6-10 lambdas : 1 groupes
- > 10 lambdas : 7 groupes

#### E. Pattern Matching
- Aucune détection : 12 groupes (normal)
- Détecté : 0 groupes (suspect pour L2)

---

## RÉSUMÉ DES CHANGEMENTS v1 → v2

- **Introduction de bonus** : HashMap Optimization (+1), Insertion Sorting (+1)
- **Analyse IA structurée** : 5 critères, scoring /5 chacun, total /25
- **Pénalité progressive** : basée sur pourcentage IA détecté
- **Transparence** : détail complet pour chaque groupe

Tous les rapports détaillés sont disponibles dans les fichiers `RAPPORT_v2_*.md`

---

*Analyse générée le 2026-10-20*
*Critères v2.0 finalisés et appliqués à tous les 11 groupes*
