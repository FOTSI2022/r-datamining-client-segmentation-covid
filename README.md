# Forage de données : segmentation client et analyse des flux COVID

## Problématique
Ce projet final de forage de données comporte deux volets : (1) la segmentation de clients à des fins marketing à partir de leurs comportements d'achat, et (2) l'analyse de flux de données liés à l'impact de la COVID-19, avec construction de modèles de classification (notamment KNN) sur les deux jeux de données.

## Données
- **Clients** : `Clients.xlsx` / `Dataset.xlsx`, données socio-démographiques et comportementales de clients (âge, revenu, durée d'adhésion, points de fidélité, engagement sur les réseaux sociaux, visites en ligne, dernier achat, valeur moyenne du panier).
- **Covid** : `Covid.csv`, données de flux liées à l'impact de la pandémie de COVID-19.
- Des flux de modélisation IBM SPSS Modeler (`.str`/`.gen`) ont été utilisés en complément de R pour certaines analyses (non inclus ici, volumineux et propriétaires ; les scripts R couvrent les analyses principales).

## Méthode
- Importation et nettoyage des données clients et covid
- Statistiques descriptives et visualisations (âge, revenu, durée d'adhésion, engagement, etc. — voir les graphiques `.png` du dossier `clients/`)
- Construction de modèles de classification (k plus proches voisins - KNN, analyse en composantes principales) pour la segmentation des clients
- Prédiction sur des observations incomplètes ou nouvelles (`Clients_null` dans le projet original)

## Résultats
Voir le rapport PDF inclus (`Rapport Projet final.pdf`) pour le détail des résultats des deux analyses (segmentation client et impact COVID). L'énoncé du projet est disponible dans `Projet Final A2024.pdf`.

## Reproduire
```bash
Ouvrir "clients/clients.Rmd" dans RStudio et faire Knit pour l'analyse de segmentation client.
Ouvrir "covid/Covid_final.Rmd" dans RStudio et faire Knit pour l'analyse des flux COVID.
(Packages requis : readxl, dplyr, tidyverse, caret, FNN, FactoMineR, e1071, klaR, ROCR, class, kknn, randomForest)
```
