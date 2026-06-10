# Étude et segmentation des comportements financiers par carte de crédit

## Présentation du projet

**Équipe :** 2 étudiants  
**Cadre :** SAE S4 Datamining BUT Science des Données

**Note :** 19,5/20

Ce projet mobilise nos compétences en **Science des Données** : nettoyage, analyse exploratoire, modélisation mathématique et classification.

Nous avons travaillé sur un jeu de données (récupéré sur Kaggle) regroupant les comportements financiers de **8 950 détenteurs de cartes de crédit** sur une période de 6 mois.  
`lien : https://www.kaggle.com/datasets/arjunbhasin2013/ccdata`
L’institution bancaire est anonymisée, mais les données décrivent les habitudes de dépenses, la gestion du solde et les comportements de remboursement des clients.

L’objectif est de transformer ces données brutes en **profils de comportements** afin de mieux comprendre et classifier les clients.

---

## Objectif de l’étude

Problématique :

> Comment la banque peut-elle adapter ses stratégies, notamment la gestion des risques, en fonction des profils de consommation et d’endettement de ses clients ?

### Missions :
- Nettoyage et préparation du dataset (valeurs manquantes, valeurs aberrantes)
- Analyse exploratoire (EDA)
- Analyse en composantes principales (ACP)
- Régression linéaire pour la limite de crédit
- Segmentation via clustering (K-Means, CAH)

---

## Technologies utilisées

- Pandas & NumPy : manipulation des données
- Scikit-Learn : Machine Learning (KMeans, PCA, LinearRegression)
- Matplotlib & Seaborn : visualisation
- SciPy : tests statistiques

---

## Préparation et nettoyage des données

- Renommage des variables et suppression des colonnes inutiles
- Traitement des valeurs manquantes (ex : paiement minimum = 0 si aucun paiement)
- Normalisation des données pour le Machine Learning

---

## Analyses et modélisation

### 1. Analyse exploratoire (EDA)

- Matrices de corrélation
- Histogrammes
- Forte disparité entre clients (présence de valeurs extrêmes)

---

### 2. Régression linéaire multiple

Objectif : prédire la limite de crédit.

Résultat :
- Le **solde du client** a un poids environ 3x plus important que le remboursement

Interprétation :
Les clients endettés génèrent des revenus via les intérêts.

---

### 3. Analyse en composantes principales (ACP)

- Réduction de 17 variables à 2 axes principaux
- Environ 50% de variance expliquée
- Deux dimensions :
  - Intensité de consommation
  - Endettement

---

## Segmentation (K-Means)

### 🟡 Acheteurs actifs
- Forte consommation
- Risque faible  
→ Fidélisation et offres premium

### 🟢 Endettés rentables
- Solde élevé
- Utilisation du crédit revolving  
→ Surveillance + rentabilité via intérêts

### 🟣 Peu actifs
- Faible activité  
→ Marketing ciblé

---

## Compétences développées

### Data Science
- Nettoyage et structuration des données
- Normalisation et préparation ML

### Machine Learning
- ACP
- K-Means / CAH
- Régression linéaire

### Business Intelligence
- Traduction des résultats en stratégie bancaire

### Data visualisation
- Matplotlib
- Seaborn

---

## Axes d’amélioration

- Automatiser le travail en amont (pipelines sklearn)
- Tester Random Forest / XGBoost
- Améliorer les performances de prédiction

---

## Conclusion

Ce projet suit le cycle complet de la data :

**Importation → Nettoyage → Analyse → Modélisation → Interprétation métier**
