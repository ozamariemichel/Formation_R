# PLAN DE FORMATION R
---
**Notes:** Les notes explicatives de ce dépôt ont été rédigées avec l'assistance d'un modèle de langage. Les projets, scripts et analyses présentés sont le fruit d'un travail personnel de l'auteur.


## PHASE 1 — FONDATIONS DU LANGAGE R

### 1. Introduction à R et à l'environnement de travail
- Historique et philosophie de R
- R et RStudio
- Console, scripts et projets
- Objets et affectation
- Calculs simples
- Aide et documentation (`?`, `help()`, `help.search()`)

### 2. Types de données et coercition
- numeric, integer, character, logical, complex, raw
- Coercition implicite et explicite
- `as.numeric()`, `as.character()`, `as.logical()`, `as.integer()`
- `class()`, `typeof()`, `str()`, `mode()`
- Hiérarchie de coercition

### 3. Vecteurs
- Création (`c()`, `seq()`, `rep()`, `:`, `letters`, `LETTERS`)
- Opérations vectorisées
- Recyclage
- Fonctions statistiques de base (`sum()`, `mean()`, `sd()`, `var()`, `min()`, `max()`, `range()`)
- Indexation numérique, logique, par noms
- Indexation négative
- `which()`, `which.min()`, `which.max()`
- Vecteurs nommés
- Tri (`sort()`, `order()`, `rank()`, `rev()`)

### 4. Matrices et arrays
- Création (`matrix()`, `array()`, `cbind()`, `rbind()`)
- Dimensions (`dim()`, `nrow()`, `ncol()`)
- Noms de lignes et colonnes (`rownames()`, `colnames()`, `dimnames()`)
- Opérations matricielles (produit, transposée, inverse, déterminant)
- Indexation et extraction
- Modification
- Arrays multidimensionnels
- `apply()` sur matrices

### 5. Facteurs
- Variables qualitatives
- Facteurs ordonnés et non ordonnés
- Niveaux (`levels()`, `nlevels()`)
- Recodage (`factor()`, `relevel()`, `droplevels()`, `cut()`)
- Comparaisons
- Tableaux de fréquences (`table()`, `prop.table()`)
- Pièges des facteurs

### 6. Listes
- Création avec `list()`
- Objets hétérogènes
- Accès avec `[ ]`, `[[ ]]`, `$`
- Modification et ajout d'éléments
- Listes imbriquées
- `unlist()`, `rapply()`
- Listes comme conteneurs de résultats

### 7. Data frames
- Création
- Structure interne (liste de vecteurs)
- Variables et observations
- Accès aux colonnes (`$`, `[[ ]]`, `[ , ]`, `[ ]`)
- Indexation lignes/colonnes
- `subset()`
- Filtrage de base
- Tri
- Agrégation (`aggregate()`, `tapply()`, `split()`)
- Jointures (`merge()`)
- `rbind()`, `cbind()`
- Pièges (`drop`, `stringsAsFactors`, matching partiel)
- Row names
- Copy-on-modify

### 8. Tibbles
- Différences avec data.frame
- Création avec `tibble()`, `tribble()`
- Affichage intelligent
- Sous-ensemble sans drop
- Compatibilité avec data.frame
- `as_tibble()`, `as.data.frame()`

### 9. data.table (introduction)
- Philosophie et performance
- Syntaxe `DT[i, j, by]`
- Modification par référence (`:=`)
- `setkey()`, `setindex()`
- Jointures rapides
- `fread()`, `fwrite()`
- Comparaison avec data.frame et tibble

### 10. Valeurs manquantes (NA)
- Nature des NA
- NA vs NULL vs NaN vs Inf
- `is.na()`, `anyNA()`, `is.nan()`, `is.finite()`
- `na.omit()`, `complete.cases()`
- `na.rm = TRUE`
- Propagation des NA
- `NA` dans les comparaisons
- Stratégies de gestion

### 11. Fonctions
- Création avec `function()`
- Arguments positionnels et nommés
- Arguments par défaut
- `...` (arguments variadiques)
- `return()`
- Portée des variables (lexical scoping)
- Variables locales et globales
- Fonctions réutilisables
- Bonnes pratiques
- `match.arg()`, `missing()`, `stop()`, `warning()`

### 12. Debugging
- `traceback()`
- `browser()`
- `debug()`, `debugonce()`, `undebug()`
- `recover()`
- `options(error = ...)`
- `try()`, `tryCatch()`, `withCallingHandlers()`
- `stopifnot()`
- `print()`, `cat()`, `message()` pour le débogage
- `trace()`

### 13. Programmation fonctionnelle
- Fonctions anonymes
- Closures
- Fonctions d'ordre supérieur
- Fonctions pures vs impures
- Récursivité
- `Reduce()`, `Filter()`, `Map()`, `Find()`, `Position()`
- `Negate()`, `Compose()`

### 14. Structures conditionnelles
- `if`
- `else`
- `else if`
- `ifelse()` (vectorisé)
- `switch()`
- `stopifnot()`
- Opérateurs logiques (`&`, `|`, `!`, `&&`, `||`)
- Différence `&` vs `&&`

### 15. Boucles
- `for`
- `while`
- `repeat`
- `break`, `next`
- Contrôle des itérations
- Pré-allocation
- Coût des boucles en R
- Quand utiliser une boucle vs une fonction vectorisée

### 16. Famille apply
- `apply()`
- `lapply()`
- `sapply()`
- `vapply()`
- `tapply()`
- `mapply()`
- `rapply()`
- Comparaison avec les boucles
- Avantages et pièges
- `simplify2array()`

### 17. purrr (introduction)
- Philosophie
- `map()`, `map_dbl()`, `map_chr()`, `map_lgl()`, `map_int()`
- `map_df()`, `map_dfr()`, `map_dfc()`
- `walk()`
- `pmap()`
- `reduce()`, `accumulate()`
- `keep()`, `discard()`, `some()`, `every()`
- `possibly()`, `safely()`, `quietly()`
- `compose()`, `partial()`
- Comparaison avec la famille apply

### 18. Workflow professionnel R
- Packages (installation, chargement, mise à jour)
- `library()`, `require()`, `::`
- Importation de données
- Exportation
- Répertoires de travail (`getwd()`, `setwd()`)
- Projets RStudio
- Scripts professionnels
- Gestion des erreurs
- `renv` pour la reproductibilité
- Organisation de projet
- Documentation

---

## PHASE 2 — MANIPULATION PROFESSIONNELLE DES DONNÉES

### 19. Introduction au tidyverse
- Philosophie tidy data
- Pipelines `%>%` et `|>`
- Packages du tidyverse
- Bonnes pratiques

### 20. Importation de données
- `readr` pour CSV et TSV
- `readxl` pour Excel
- `haven` pour SPSS, Stata, SAS
- `jsonlite` pour JSON
- `readr::read_delim()` et formats spéciaux
- Encodage et caractères spéciaux
- `colClasses`, `col_types`
- Importation de gros fichiers

### 21. Nettoyage avec janitor
- `clean_names()`
- `remove_empty()`, `remove_empty_rows()`, `remove_empty_cols()`
- `get_dupes()`
- `tabyl()`, `adorn_totals()`, `adorn_percentages()`
- `row_to_names()`
- `excel_numeric_to_date()`

### 22. Manipulation avec dplyr
- `select()`, `pull()`, `rename()`
- `filter()`, `slice()`, `distinct()`
- `arrange()`
- `mutate()`, `transmute()`
- `summarise()`, `reframe()`
- `group_by()`, `ungroup()`
- `across()`, `where()`, `if_any()`, `if_all()`
- `case_when()`, `if_else()`, `coalesce()`, `na_if()`
- `row_number()`, `ntile()`, `cumsum()`
- `relocate()`
- `bind_rows()`, `bind_cols()`

### 23. Jointures de tables
- `left_join()`, `right_join()`, `inner_join()`, `full_join()`
- `anti_join()`, `semi_join()`
- `cross_join()`
- Clés simples et composites
- Suffixes
- Gestion des doublons de clés
- `nest_join()`
- Jointures sur inégalités (`join_by()`)

### 24. Restructuration avec tidyr
- `pivot_longer()`
- `pivot_wider()`
- `separate()`, `separate_wider_delim()`, `separate_wider_position()`
- `unite()`
- `drop_na()`, `fill()`
- `complete()`, `expand()`
- `nest()`, `unnest()`
- `hoist()`

### 25. Chaînes de caractères avec stringr
- `str_detect()`, `str_which()`
- `str_extract()`, `str_extract_all()`
- `str_match()`, `str_match_all()`
- `str_replace()`, `str_replace_all()`
- `str_split()`, `str_split_fixed()`
- `str_sub()`
- `str_trim()`, `str_squish()`
- `str_pad()`
- `str_to_lower()`, `str_to_upper()`, `str_to_title()`
- Expressions régulières : classes de caractères, quantificateurs, ancres, groupes, backreferences, lookahead, lookbehind
- Bonnes pratiques regex

### 26. Dates et temps avec lubridate
- Dates, heures, datetime
- `ymd()`, `dmy()`, `mdy()`, `ymd_hms()`
- `year()`, `month()`, `day()`, `hour()`, `minute()`, `second()`
- `wday()`, `yday()`, `week()`
- `floor_date()`, `ceiling_date()`, `round_date()`
- `duration()`, `period()`, `interval()`
- Arithmétique sur les dates
- Fuseaux horaires
- Formats d'affichage

### 27. Gestion avancée des facteurs avec forcats
- `fct_reorder()`
- `fct_infreq()`, `fct_inorder()`
- `fct_relevel()`
- `fct_lump()`, `fct_lump_min()`, `fct_lump_prop()`
- `fct_collapse()`
- `fct_other()`
- `fct_recode()`
- `fct_expand()`, `fct_drop()`
- `fct_na_value_to_level()`

### 28. Web scraping et APIs
- `rvest` : `read_html()`, `html_elements()`, `html_text()`, `html_attr()`, `html_table()`
- Sélecteurs CSS et XPath
- `httr2` : `request()`, `req_url()`, `req_headers()`, `req_perform()`, `resp_body_json()`
- Authentification (clés API, OAuth)
- Rate limiting
- Bonnes pratiques et éthique

### 29. Pipelines complexes et contrôles qualité
- Pipelines dplyr enchaînés
- `group_by()` + `across()` pour les transformations en masse
- Validation de données (`validate`, `pointblank`)
- Assertions (`assertthat`, `checkmate`)
- Logging
- Documentation de pipeline

---

## PHASE 3 — VISUALISATION DES DONNÉES

### 30. Graphiques de base R
- `plot()`, `hist()`, `boxplot()`, `barplot()`, `pie()`
- `lines()`, `points()`, `abline()`, `segments()`
- `par()` et les paramètres graphiques
- `legend()`, `title()`, `axis()`
- `image()`, `contour()`, `persp()`
- Sauvegarde (`pdf()`, `png()`, `dev.off()`)

### 31. Fondamentaux ggplot2
- Grammaire des graphiques
- `ggplot()`, `aes()`, `+`
- Layers, geoms, stats
- `geom_point()`, `geom_line()`, `geom_bar()`, `geom_histogram()`
- Groupes et couleurs
- Données et mappings

### 32. Visualisations univariées
- Histogrammes et densités
- Barplots et diagrammes en secteurs
- QQ-plots
- Diagrammes en violon
- Ridge plots
- Diagrammes en points (dotplots)

### 33. Visualisations bivariées
- Scatterplots
- Boxplots
- Courbes
- Graphiques en aires
- Heatmaps
- Graphiques en barres empilées et groupées
- Graphiques en coordonnées parallèles

### 34. Personnalisation ggplot2
- `scale_*()` (couleurs, axes, tailles)
- `theme()` et thèmes prédéfinis
- `labs()`, titres, sous-titres, légendes
- `facet_wrap()`, `facet_grid()`
- Annotations (`annotate()`, `geom_text()`, `geom_label()`)
- Repères (`geom_hline()`, `geom_vline()`)
- Flèches et segments

### 35. Extensions ggplot2
- `patchwork` : composition multi-graphiques
- `ggrepel` : étiquettes non chevauchantes
- `gganimate` : animations
- `plotly` : interactivité
- `ggforce` : formes avancées
- `ggdist` : distributions
- `ggpubr` : graphiques prêts pour publication
- `corrplot`, `GGally` : graphiques multivariés

### 36. Visualisation avancée et publication
- Storytelling statistique
- Choix du graphique selon la question
- Palette de couleurs accessibles (`viridis`, `RColorBrewer`)
- Hiérarchie visuelle
- Ratio données/encre
- `ggsave()` et export haute résolution
- Formats vectoriels vs raster
- Typographie et mise en page

### 37. Visualisation spatiale
- `sf` : objets spatiaux, importation shapefile/GeoJSON
- `tmap` : cartes thématiques
- `leaflet` : cartes interactives
- `ggplot2` + `sf` : cartes statiques
- Projections et systèmes de coordonnées
- Choroplèthes, cartogrammes, cartes de points
- Jointures spatiales

---

## PHASE 4 — STATISTIQUE DESCRIPTIVE

### 38. Statistiques descriptives
- Moyenne, médiane, mode
- Moyenne géométrique, harmonique
- Variance, écart-type
- Quantiles, IQR, déciles
- Étendue, MAD
- Coefficient de variation
- Skewness, kurtosis
- Tableaux de fréquences
- Résumés par groupe

### 39. Analyse exploratoire des données (EDA)
- Distributions
- Relations bivariées
- Matrices de corrélation et heatmaps
- Patterns et structures
- Détection de tendances
- Analyses multivariées préliminaires

### 40. Détection d'anomalies
- Outliers univariés (Z-score, IQR, MAD)
- Outliers multivariés (Mahalanobis)
- Isolation Forest
- LOF (Local Outlier Factor)
- DBSCAN pour la détection
- Traitement des outliers
- Documentation des décisions

### 41. Reporting descriptif
- Rapports professionnels
- Tableaux statistiques de qualité
- Synthèses automatiques
- Note de synthèse pour décideurs
- Structure d'un rapport statistique

---

## PHASE 5 — PROBABILITÉS

### 42. Variables aléatoires et distributions
- Variables aléatoires discrètes
- Variables aléatoires continues
- Fonction de masse, densité, répartition
- Espérance, variance, moments
- Transformations de variables

### 43. Lois usuelles
- Loi binomiale
- Loi de Poisson
- Loi normale
- Loi uniforme
- Loi exponentielle

### 44. Autres lois
- Loi gamma
- Loi bêta
- Loi khi-deux
- Loi de Student
- Loi de Fisher
- Loi log-normale
- Loi de Weibull
- Loi hypergéométrique
- Loi binomiale négative
- Loi multinomiale
- Loi de Dirichlet

### 45. Simulation statistique
- Génération aléatoire (`rnorm`, `runif`, `rbinom`, etc.)
- `set.seed()` et reproductibilité
- Monte Carlo
- Bootstrap
- Tests de randomisation
- Simulations de puissance
- Simulations de systèmes complexes

---

## PHASE 6 — INFÉRENCE STATISTIQUE

### 46. Estimation et intervalles de confiance
- Estimateurs et propriétés (biais, variance, MSE)
- Maximum de vraisemblance
- Méthode des moments
- Intervalles de confiance
- Bootstrap pour les IC
- Intervalles de prédiction
- Intervalles de tolérance

### 47. Tests d'hypothèses
- H0 et H1
- Erreurs Type I et II
- p-valeur et interprétation correcte
- Tests unilatéraux et bilatéraux
- Tests sur une moyenne
- Tests sur deux moyennes
- Tests sur proportions
- Tests appariés
- Test de Welch

### 48. Comparaison de groupes
- Khi-deux d'indépendance et d'ajustement
- Test exact de Fisher
- ANOVA à un facteur
- ANOVA à deux facteurs
- ANCOVA
- MANOVA
- Tests post-hoc (Tukey, Bonferroni, Scheffé)
- Tests non paramétriques (Mann-Whitney, Wilcoxon, Kruskal-Wallis, Friedman)

### 49. Puissance statistique et taille d'échantillon
- Puissance et effet
- Taille d'effet (Cohen's d, η², OR)
- Calcul de taille d'échantillon
- Analyse de puissance a priori et post hoc
- Courbes de puissance
- Facteurs influençant la puissance

### 50. Corrections pour tests multiples
- Problème des tests multiples
- Bonferroni
- Holm-Bonferroni
- Benjamini-Hochberg (FDR)
- FDR local
- Approches bayésiennes

---

## PHASE 7 — MODÉLISATION STATISTIQUE

### 51. Régression linéaire
- Régression linéaire simple
- Régression linéaire multiple
- Formulation matricielle
- MCO et propriétés
- Théorème de Gauss-Markov
- Interprétation des coefficients
- Variables qualitatives (dummy coding)
- Interactions
- Transformations
- R² et R² ajusté

### 52. Diagnostics de régression
- Analyse des résidus
- Normalité des résidus
- Homoscédasticité
- Linéarité
- Indépendance
- Multicolinéarité (VIF)
- Points influents (Cook, leverage)
- Durbin-Watson
- Breusch-Pagan, White
- Graphiques diagnostiques

### 53. Sélection de variables
- Forward, backward, stepwise
- AIC, BIC, Cp de Mallows
- Validation croisée
- LASSO, ridge, elastic net
- Approches bayésiennes

### 54. Régression régularisée
- Ridge (L2)
- LASSO (L1)
- Elastic net
- Choix de λ par validation croisée
- Interprétation des coefficients
- `glmnet`

### 55. Régression logistique et GLM
- Régression logistique binaire
- Interprétation des OR
- Multinomiale, ordinale
- Modèles linéaires généralisés
- Familles exponentielle
- Fonctions de lien
- Déviance
- Pseudo-R²
- Courbes ROC et AUC
- Calibration

### 56. Modèles de comptage
- Poisson
- Surdispersion
- Binomiale négative
- Zero-inflated
- Hurdle models
- Interprétation des IRR

### 57. Modèles de survie
- Fonction de survie et de risque
- Censure
- Kaplan-Meier
- Test du log-rank
- Modèle de Cox
- Hazard Ratio
- Hypothèse de proportionnalité
- Modèles paramétriques (exponentiel, Weibull, log-normal)
- Risques concurrents

### 58. Modèles mixtes
- Modèles linéaires mixtes
- Effets fixes et aléatoires
- Structures de covariance
- REML
- ICC
- Modèles linéaires généralisés mixtes
- Diagnostics
- `lme4`, `nlme`, `glmmTMB`

---

## PHASE 8 — ANALYSE MULTIVARIÉE

### 59. Analyse en composantes principales (ACP)
- Principe et objectifs
- Standardisation
- Valeurs et vecteurs propres
- Choix du nombre d'axes
- Cercle des corrélations
- Contributions
- Interprétation des axes
- Scores et visualisation

### 60. Analyse factorielle des correspondances (AFC)
- Tableaux de contingence
- Profils lignes et colonnes
- Inertie
- Représentation factorielle
- Interprétation
- `FactoMineR`

### 61. Analyse des correspondances multiples (ACM)
- Variables qualitatives multiples
- Tableau disjonctif complet
- Inertie corrigée
- Interprétation
- Applications aux enquêtes

### 62. Classification et segmentation
- Classification ascendante hiérarchique (CAH)
- Critères de liaison (Ward, average, complete)
- Dendrogrammes
- Choix du nombre de classes
- K-means
- K-medoids
- DBSCAN
- Gaussian Mixture Models
- Profils des classes

### 63. Analyse discriminante
- LDA (Linear Discriminant Analysis)
- QDA (Quadratic Discriminant Analysis)
- Frontières de décision
- Évaluation
- Validation croisée

### 64. Réduction de dimension non linéaire
- t-SNE
- UMAP
- Isomap
- LLE
- Autoencodeurs
- Interprétation et limites

---

## PHASE 9 — ENQUÊTES COMPLEXES

### 65. Plans de sondage
- Population finie
- Probabilités d'inclusion
- Sondage aléatoire simple
- Sondage systématique
- Sondage stratifié
- Sondage par grappes
- Sondage à plusieurs degrés
- PPS
- Effet de plan (DEFF)
- Corrélation intraclasse

### 66. Analyse avec survey
- `svydesign()`
- `svymean()`, `svytotal()`, `svyratio()`
- `svyglm()`, `svychisq()`, `svyttest()`
- `svyby()`
- Sous-populations
- Domaines d'étude
- Variance et intervalles de confiance
- Tests d'hypothèses

### 67. Pondération et calage
- Poids de base
- Ajustement pour non-réponse
- Post-stratification
- Calage (raking)
- Troncature des poids extrêmes
- Diagnostics de pondération

### 68. Calcul de taille d'échantillon
- Pour une proportion
- Pour une moyenne
- Pour une différence
- Correction pour population finie
- Prise en compte du DEFF
- Prise en compte de la non-réponse
- Logiciels et packages

### 69. Applications EDS, MICS et enquêtes nationales
- Structure des données EDS
- Pondération EDS
- Indicateurs EDS
- Analyse avec `survey`
- MICS
- Enquêtes nationales (EHCVM, EMICoV)
- Reproductibilité des analyses

---

## PHASE 10 — SÉRIES TEMPORELLES

### 70. Fondamentaux
- Composantes (tendance, saisonnalité, cycle, irrégulier)
- Décomposition
- Stationnarité
- ACF et PACF
- Tests de racine unitaire (ADF, KPSS, PP)
- Différenciation

### 71. Modélisation
- AR, MA, ARMA
- ARIMA
- SARIMA
- Box-Jenkins
- `forecast`, `auto.arima()`, `ets()`
- Diagnostics
- Prévisions et intervalles

### 72. VAR, coïntégration, espace-état
- VAR (Vector Autoregression)
- Fonctions de réponse impulsionnelle
- Causalité de Granger
- Coïntégration
- Modèles à correction d'erreur (ECM)
- Modèles espace-état
- Filtre de Kalman

### 73. Prophet
- Philosophie
- Décomposition additive
- Détection automatique de points de rupture
- Effets de jours fériés
- Prévisions
- Diagnostic

---

## PHASE 11 — DONNÉES MANQUANTES AVANCÉES

### 74. Mécanismes
- MCAR (Missing Completely At Random)
- MAR (Missing At Random)
- MNAR (Missing Not At Random)
- Diagnostic du mécanisme
- Impact sur les analyses

### 75. Imputation simple
- Par la moyenne, la médiane, le mode
- Par régression
- Par la dernière valeur observée (LOCF)
- Hot-deck, cold-deck
- Limites

### 76. Imputation multiple avec mice
- Principe
- Création des jeux imputés
- Analyse des jeux imputés
- Pooling des résultats
- Règles de Rubin
- Choix de m
- Méthodes d'imputation (PMM, CART, etc.)

### 77. Diagnostics d'imputation et analyses de sensibilité
- Diagnostics visuels
- Comparaison de stratégies
- Analyse de sensibilité
- Modèles de non-réponse
- Rapporter les résultats d'imputation

---

## PHASE 12 — INFÉRENCE CAUSALE

### 78. Graphes causaux
- DAGs (Directed Acyclic Graphs)
- Confoundeurs, médiateurs, colliders
- Backdoor criterion
- Frontdoor criterion
- Identification
- `dagitty`

### 79. Matching et Propensity Score
- Propensity Score
- PSM (Propensity Score Matching)
- IPTW (Inverse Probability Treatment Weighting)
- Balance des covariables
- Diagnostics
- `MatchIt`, `WeightIt`, `cobalt`

### 80. Difference-in-differences
- Principe
- Hypothèse des tendances parallèles
- Test des pré-tendances
- DiD avec covariables
- DiD avec plusieurs périodes
- `did`

### 81. Regression discontinuity
- Sharp RD
- Fuzzy RD
- Estimation locale
- Choix de la fenêtre
- Diagnostics
- `rdrobust`

### 82. Variables instrumentales
- Conditions d'un bon instrument
- IV en 2SLS
- Test de faiblesse de l'instrument
- Test de suridentification
- `AER`, `ivreg`

### 83. Effets fixes et modèles de panel
- Structure des données de panel
- Effets fixes (within)
- Effets aléatoires (GLS)
- Test de Hausman
- Panel dynamique (Arellano-Bond)
- `plm`, `fixest`

### 84. Expérimentation et A/B testing
- RCT (Randomized Controlled Trials)
- A/B testing
- Tests séquentiels
- Taille d'échantillon
- Validité interne et externe
- Éthique

---

## PHASE 13 — MACHINE LEARNING

### 85. Préparation des données
- Nettoyage
- Encodage des variables catégorielles
- Normalisation et standardisation
- Gestion des valeurs manquantes
- Feature engineering
- Éviter le data leakage

### 86. Validation croisée
- k-fold CV
- LOOCV
- Stratified k-fold
- Validation croisée imbriquée
- Time series CV
- Group CV

### 87. Méthodes supervisées
- Arbres de décision
- Random Forest
- Gradient Boosting (XGBoost, LightGBM, CatBoost)
- SVM
- Réseaux de neurones
- KNN
- Naive Bayes

### 88. Méthodes non supervisées
- K-means
- Clustering hiérarchique
- DBSCAN
- Gaussian Mixture Models
- ACP, t-SNE, UMAP
- Autoencodeurs

### 89. Évaluation des performances
- Classification : accuracy, precision, recall, F1, AUC
- Régression : MSE, RMSE, MAE, R²
- Matrice de confusion
- Courbes ROC et PR
- Calibration
- Bootstrap pour l'incertitude

### 90. Interprétabilité
- SHAP
- LIME
- Partial Dependence Plots (PDP)
- ICE plots
- Feature importance
- `iml`, `DALEX`, `shapviz`

### 91. Équité algorithmique
- Biais dans les données
- Biais dans les prédictions
- Métriques de fairness
- Mitigation
- Éthique
- `fairness`, `fairmodels`

---

## PHASE 14 — REPRODUCTIBILITÉ

### 92. R Markdown
- Structure d'un document
- Chunks de code
- Options de chunks
- Paramétrage
- Output PDF, HTML, Word
- `knitr`

### 93. Quarto
- Philosophie
- Documents, présentations, sites web
- Multi-langages
- Paramétrage
- Output

### 94. Rapports paramétrés et automatisés
- Paramètres
- Boucles sur les rapports
- Génération en lot
- Templates

### 95. Documentation de projets
- README.md
- Documentation de fonctions (roxygen2)
- Dictionnaire de données
- Structure de projet

### 96. Git et GitHub
- Git : init, add, commit, push, pull, clone, branch, merge, rebase, stash
- GitHub : pull requests, issues, actions
- Bonnes pratiques
- Collaboration

### 97. targets
- Philosophie
- Pipelines reproductibles
- Dépendances
- Parallélisation
- `_targets.R`

### 98. renv
- Philosophie
- Capture de l'environnement
- `renv.lock`
- Restauration
- Bonnes pratiques

---

## PHASE 15 — NIVEAU EXPERT

### 99. Développement de packages R
- Structure d'un package
- `DESCRIPTION`, `NAMESPACE`
- Documentation avec roxygen2
- Tests
- Vignettes
- Soumission à CRAN
- Packages internes

### 100. Tests automatisés
- `testthat`
- Tests unitaires
- Tests d'intégration
- Tests de régression
- Couverture de code
- Bonnes pratiques

### 101. Optimisation et profiling
- `profvis`
- `Rprof`
- `bench`
- `microbenchmark`
- Identification des goulots
- Optimisation algorithmique
- Vectorisation
- Pré-allocation

### 102. Parallel computing
- `parallel`
- `future`
- `furrr`
- Parallélisation sur CPU
- Parallélisation sur GPU (concepts)
- Bonnes pratiques

### 103. Programmation orientée objet
- S3
- S4
- R6
- Choisir le bon système
- Bonnes pratiques

### 104. Shiny
- Philosophie
- UI et Server
- Réactivité
- Inputs et outputs
- Layouts
- Modules
- Déploiement
- `bslib`, `thematic`

### 105. APIs et intégration de services
- Créer une API avec `plumber`
- Consommer une API avec `httr2`
- Authentification
- Rate limiting
- Bonnes pratiques

### 106. SQL et bases de données relationnelles
- SQL de base
- Connexion à une base (DBI, RPostgres, RSQLite)
- Requêtes
- Manipulation
- Bonnes pratiques

### 107. Big Data avec R
- `arrow`
- `disk.frame`
- `sparklyr`
- Intégration avec les bases de données
- Bonnes pratiques

### 108. Rcpp et intégration C++
- Philosophie
- `cppFunction()`
- `sourceCpp()`
- Types et conversions
- Optimisation
- Cas d'usage

### 109. Pipelines de production et déploiement
- Docker
- CI/CD
- Déploiement de modèles
- Monitoring
- Bonnes pratiques
- `targets` en production
