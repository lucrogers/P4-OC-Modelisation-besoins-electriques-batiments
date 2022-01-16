# Projet 4 - OpenClassrooms
Parcours Data Science

Projet n°4 : "Anticipez les besoins en consommation électrique de bâtiments"

- Source des données : https://www.kaggle.com/city-of-seattle/sea-building-energy-benchmarking#2015-building-energy-benchmarking.csv

## Introduction du projet
La ville de Seattle s'est fixée comme objectif d'être une ville neutre en émissions carbone d'ici 2050. A ce titre elle souhaiterait créer un modèle qui permette de prédire les besoins énergétiques et les émissions de CO2 engendrés par les bâtiments à venir.

Le jeu de données met en relation les caractéristiques du permis d'exploitation de divers bâtiments avec leurs consommations énergétiques.

Dans ce notebook, 4 modèles de régression sont successivement entraînés, du plus simple au plus complexe:
- k-NN
- Régression Lasso
- Random Forest
- Réseau de neurones (keras)

Il nous est également demandé d'évaluer la pertinence de l'ENERGY STAR Score, un indice censé évaluer l'efficacité énergétique du bâtiment mais fastidieux à calculer.

**Conclusions:** le modèle retenu diffère selon la cible étudiée:
- Random Forest pour la consommation électrique (score R² = 0,672)
- Réseau de neurones pour les émissions de CO2 (score R² = 0,674)
- La variable ENERGY STAR Score a une influence positive non négligeable sur la prédiction des émissions de CO2

## Travail réalisé
- Préparation du jeu de données (nettoyage, jointures)
- Analyse exploratoire
- Feature engineering
  - Création de nouvelles variables
  - Transformation des variables asymétriques
  - Encodage des variables catégorielles
  - Scaling si nécessaire
  - Réduction de dimensions (ACP ou propre au modèle choisi)
- Entraînement des différents modèles de régression
  - Split train/test
  - Validation croisée 5 folds
  - Grille de recherche d'hyperparamètres
  - Visualisation des scores optimaux
  - Mise en avant des variables significatives
- Comparaison et conclusions

## Compétences évaluées
- Mettre en place le modèle d'apprentissage supervisé adapté au problème métier
- Adapter les hyperparamètres d'un algorithme d'apprentissage supervisé afin de l'améliorer
- Transformer les variables pertinentes d'un modèle d'apprentissage supervisé
- Évaluer les performances d’un modèle d'apprentissage supervisé
