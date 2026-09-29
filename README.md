# FORMATION R — PLAN RÉVISÉ

## PHASE 1 — FONDATIONS DU LANGAGE R

### 1. Introduction à R et à l'environnement de travail

- [x] Historique et philosophie de R
- [x] R et RStudio
- [x] Console, scripts et projets
- [x] Objets et affectation
- [x] Calculs simples
- [x] Aide et documentation (`?`, `help()`, `help.search()`)

### 2. Types de données et coercition

- [x] numeric
- [x] integer
- [x] character
- [x] logical
- [x] Coercition implicite
- [x] Coercition explicite
- [x] `as.numeric()`
- [x] `as.character()`
- [x] `as.logical()`
- [x] `class()`
- [x] `typeof()`
- [x] `str()`

### 3. Vecteurs

- [x] Création
- [x] Opérations vectorisées
- [x] Recyclage
- [x] Fonctions statistiques de base
- [x] Indexation des vecteurs
- [x] Indexation logique
- [x] `which()`

### 4. Valeurs manquantes (NA)

- [ ] Nature des NA
- [ ] `is.na()`
- [ ] `anyNA()`
- [ ] `na.omit()`
- [ ] `complete.cases()`
- [ ] `na.rm = TRUE`
- [ ] Stratégies professionnelles de gestion des données manquantes

### 5. Matrices

- [ ] Création
- [ ] Dimensions
- [ ] Noms de lignes et colonnes
- [ ] Opérations matricielles
- [ ] Indexation
- [ ] Extraction et modification

### 6. Facteurs

- [ ] Variables qualitatives
- [ ] Facteurs ordonnés
- [ ] Facteurs non ordonnés
- [ ] Niveaux
- [ ] Recodage
- [ ] Comparaisons

### 7. Listes

- [ ] Création avec `list()`
- [ ] Objets hétérogènes
- [ ] Accès avec `[ ]`
- [ ] Accès avec `[[ ]]`
- [ ] Accès avec `$`
- [ ] Modification et ajout d'éléments

### 8. Data frames

- [ ] Création
- [ ] Structure
- [ ] Variables et observations
- [ ] Accès aux colonnes
- [ ] Indexation lignes/colonnes
- [ ] `$`
- [ ] `[[ ]]`
- [ ] `[ , ]`
- [ ] `subset()`
- [ ] Filtrage de base

### 9. Fonctions

- [ ] Création avec `function()`
- [ ] Arguments
- [ ] Arguments par défaut
- [ ] `return()`
- [ ] Portée des variables
- [ ] Fonctions réutilisables
- [ ] Bonnes pratiques

### 10. Programmation fonctionnelle

- [ ] Fonctions anonymes
- [ ] Closures
- [ ] Introduction aux fonctions d'ordre supérieur

### 11. Structures conditionnelles

- [ ] `if`
- [ ] `else`
- [ ] `else if`
- [ ] `switch`

### 12. Boucles

- [ ] `for`
- [ ] `while`
- [ ] `repeat`
- [ ] Contrôle des itérations

### 13. Famille apply

- [ ] `apply()`
- [ ] `lapply()`
- [ ] `sapply()`
- [ ] `vapply()`
- [ ] `tapply()`
- [ ] Comparaison avec les boucles

### 14. Workflow professionnel R

- [ ] Packages
- [ ] Installation et chargement
- [ ] Importation de données
- [ ] Exportation
- [ ] Répertoires de travail
- [ ] Projets RStudio
- [ ] Scripts professionnels
- [ ] Gestion des erreurs

---

## PHASE 2 — MANIPULATION PROFESSIONNELLE DES DONNÉES

### 15. Introduction au tidyverse

- [ ] Philosophie tidy data
- [ ] Pipelines `%>%`

### 16. Manipulation avec dplyr

- [ ] `select()`
- [ ] `filter()`
- [ ] `arrange()`
- [ ] `mutate()`
- [ ] `summarise()`
- [ ] `group_by()`
- [ ] `across()`
- [ ] `case_when()`

### 17. Jointures de tables

- [ ] `left_join()`
- [ ] `inner_join()`
- [ ] `right_join()`
- [ ] `full_join()`
- [ ] `anti_join()`

### 18. Restructuration avec tidyr

- [ ] `pivot_longer()`
- [ ] `pivot_wider()`
- [ ] `separate()`
- [ ] `unite()`
- [ ] `drop_na()`
- [ ] `fill()`

### 19. Manipulation avancée

- [ ] Pipelines complexes
- [ ] Nettoyage de données
- [ ] Contrôles qualité

### 20. Chaînes de caractères avec stringr

- [ ] Détection
- [ ] Extraction
- [ ] Remplacement
- [ ] Expressions régulières

### 21. Dates et temps avec lubridate

- [ ] Dates
- [ ] Heures
- [ ] Durées
- [ ] Calculs temporels

### 22. Gestion avancée des facteurs avec forcats

- [ ] Réorganisation
- [ ] Fusion
- [ ] Recodage

---

## PHASE 3 — VISUALISATION DES DONNÉES

### 23. Graphiques de base R

- [ ] Graphiques de base R

### 24. Fondamentaux ggplot2

- [ ] `ggplot()`
- [ ] `aes()`
- [ ] Layers
- [ ] Geoms

### 25. Visualisations univariées

- [ ] Histogrammes
- [ ] Densités
- [ ] Barplots

### 26. Visualisations bivariées

- [ ] Scatterplots
- [ ] Boxplots
- [ ] Courbes

### 27. Personnalisation ggplot2

- [ ] Scales
- [ ] Themes
- [ ] Labels
- [ ] Facettes

### 28. Visualisation avancée et publication

- [ ] Graphiques multivariés
- [ ] Storytelling
- [ ] Communication visuelle
- [ ] `ggsave()`

---

## PHASE 4 — STATISTIQUE DESCRIPTIVE

### 29. Statistiques descriptives

- [ ] Moyenne
- [ ] Médiane
- [ ] Mode
- [ ] Variance
- [ ] Écart-type
- [ ] Quantiles
- [ ] IQR

### 30. Analyse exploratoire des données (EDA)

- [ ] Distributions
- [ ] Détection d'anomalies
- [ ] Résumés statistiques

### 31. Reporting descriptif

- [ ] Rapports professionnels
- [ ] Synthèses automatiques

---

## PHASE 5 — PROBABILITÉS

### 32. Variables aléatoires et distributions

- [ ] Discrètes
- [ ] Continues

### 33. Lois usuelles

- [ ] Binomiale
- [ ] Poisson
- [ ] Normale

### 34. Simulation statistique

- [ ] Génération aléatoire
- [ ] Monte Carlo

---

## PHASE 6 — INFÉRENCE STATISTIQUE

### 35. Estimation et intervalles de confiance

- [ ] Estimation et intervalles de confiance

### 36. Tests d'hypothèses

- [ ] Une moyenne
- [ ] Deux moyennes
- [ ] Proportions

### 37. Comparaison de groupes

- [ ] Khi-deux
- [ ] ANOVA
- [ ] Tests non paramétriques

---

## PHASE 7 — MODÉLISATION STATISTIQUE

### 38. Régression linéaire

- [ ] Simple
- [ ] Multiple
- [ ] Diagnostics
- [ ] Sélection de variables

### 39. Régression logistique et GLM

- [ ] Régression logistique et GLM

---

## PHASE 8 — ANALYSE MULTIVARIÉE

### 40. Analyse en composantes principales (ACP)

- [ ] Analyse en composantes principales (ACP)

### 41. Analyse factorielle des correspondances (AFC)

- [ ] Analyse factorielle des correspondances (AFC)

### 42. Analyse des correspondances multiples (ACM)

- [ ] Analyse des correspondances multiples (ACM)

### 43. Classification et segmentation (HCPC)

- [ ] Classification et segmentation (HCPC)

---

## PHASE 9 — ENQUÊTES COMPLEXES

### 44. Plans de sondage

- [ ] Plans de sondage

### 45. Analyse avec le package survey

- [ ] `svydesign()`
- [ ] `svymean()`
- [ ] `svytotal()`
- [ ] `svyglm()`
- [ ] `svychisq()`

### 46. Applications EDS, MICS et enquêtes nationales

- [ ] Applications EDS, MICS et enquêtes nationales

---

## PHASE 10 — ANALYSE DE SURVIE

### 47. Fondamentaux de la survie

- [ ] `Surv()`
- [ ] Kaplan-Meier
- [ ] Log-Rank

### 48. Modèle de Cox

- [ ] `coxph()`

---

## PHASE 11 — SÉRIES TEMPORELLES

### 49. Fondamentaux des séries temporelles

- [ ] Décomposition
- [ ] Stationnarité

### 50. Modélisation temporelle

- [ ] `adf.test()`
- [ ] `kpss.test()`
- [ ] `ets()`
- [ ] `auto.arima()`
- [ ] `forecast()`

---

## PHASE 12 — MODÈLES MIXTES

### 51. Modèles linéaires mixtes

- [ ] `lmer()`

### 52. Modèles généralisés mixtes

- [ ] `glmer()`

### 53. Structures hiérarchiques

- [ ] Structures hiérarchiques

---

## PHASE 13 — DONNÉES MANQUANTES AVANCÉES

### 54. Imputation multiple avec mice

- [ ] Création
- [ ] Analyse
- [ ] Pooling
- [ ] Règles de Rubin

---

## PHASE 14 — MACHINE LEARNING

### 55. Préparation des données

- [ ] Préparation des données

### 56. Validation des modèles

- [ ] Validation des modèles

### 57. Méthodes supervisées

- [ ] Classification
- [ ] Régression
- [ ] Arbres
- [ ] Random Forest
- [ ] Gradient Boosting

### 58. Méthodes non supervisées

- [ ] Clustering

### 59. Évaluation des performances

- [ ] Évaluation des performances

---

## PHASE 15 — REPRODUCTIBILITÉ

### 60. R Markdown et Quarto

- [ ] R Markdown et Quarto

### 61. Rapports paramétrés et automatisés

- [ ] Rapports paramétrés et automatisés

### 62. Documentation de projets

- [ ] Documentation de projets

### 63. Git et GitHub

- [ ] Git et GitHub

---

## PHASE 16 — NIVEAU EXPERT

### 64. Développement de packages R

- [ ] Développement de packages R

### 65. Tests automatisés

- [ ] Tests automatisés

### 66. Optimisation et profiling

- [ ] Optimisation et profiling

### 67. Programmation orientée objet (S3, S4, R6)

- [ ] S3
- [ ] S4
- [ ] R6

### 68. Shiny

- [ ] Shiny

### 69. APIs et intégration de services

- [ ] APIs et intégration de services

### 70. SQL et bases de données relationnelles

- [ ] SQL et bases de données relationnelles

### 71. Big Data avec R

- [ ] Big Data avec R

### 72. Pipelines de production et déploiement

- [ ] Pipelines de production et déploiement
