# 🌍 Analyse des catastrophes climatiques avec PostgreSQL et Metabase

## Contexte

L'objectif de ce projet était de déployer un environnement complet d'analyse de données en utilisant **PostgreSQL** pour le stockage des données et **Metabase** pour la visualisation et le reporting, le tout conteneurisé avec **Docker**.

La base de données utilisée contient des informations sur les catastrophes climatiques à travers le monde entre **1980 et 2023**.

---

## 🎯 Objectifs

- Déployer un environnement d'analyse de données avec Docker.
- Interroger une base de données relationnelle avec PostgreSQL.
- Construire des requêtes SQL avancées utilisant des jointures et des agrégations.
- Préparer les données pour l'analyse.
- Créer des visualisations interactives avec Metabase.
- Analyser l'évolution des catastrophes climatiques selon différents axes.

---

## 🛠️ Technologies utilisées

- PostgreSQL
- Metabase
- Docker
- SQL
- Git & GitHub

---

## Analyse des données

Après avoir configuré l'environnement, j'ai réalisé plusieurs analyses exploratoires afin d'étudier :

- L'évolution temporelle des catastrophes naturelles de 1980 à 2023.
- La répartition géographique des événements.
- Les régions les plus vulnérables.
- Les tendances selon les différents types de catastrophes climatiques.

### Exemple d'analyse

Une analyse a été réalisée afin d'identifier les sous-régions les plus touchées par les catastrophes climatiques.

### Exemple de requête SQL

```sql
SELECT 
sub_region.name AS sub_region_name,
SUM(climate_disaster.number) AS total_disasters
FROM sub_region 
JOIN 
country ON sub_region.sub_region_code = country.sub_region_code
JOIN 
climate_disaster ON country.country_code = climate_disaster.country_code
GROUP BY 
sub_region.name
HAVING SUM
(climate_disaster.number) > 1000
ORDER BY
total_disasters DESC;

```

---

## 📈 Visualisations réalisées

Grâce à Metabase, plusieurs visualisations ont été construites :

- Courbes d'évolution annuelle des catastrophes.
- Diagrammes de répartition géographique.
- Classements des régions les plus exposées.
- Analyses comparatives entre différentes zones du monde.

### Exemple de visualisation



---

## 🚀 Compétences développées

Ce projet m'a permis de :

- Maîtriser l'utilisation d'une base de données relationnelle avec PostgreSQL.
- Écrire des requêtes SQL complexes utilisant des jointures et des fonctions d'agrégation.
- Préparer et nettoyer les données avant leur exploitation.
- Construire des indicateurs pertinents pour l'analyse.
- Concevoir des visualisations et tableaux de bord avec Metabase.
- Comprendre l'importance de la qualité des données dans un projet décisionnel.

Cette expérience m'a également montré qu'un reporting efficace repose avant tout sur un traitement rigoureux des données en amont.

---

## Axes d'amélioration

Afin de continuer à progresser, je souhaite :

- Réaliser de nouveaux projets à partir de jeux de données disponibles sur Kaggle.
- Optimiser davantage mes requêtes SQL.
- Approfondir les fonctionnalités avancées de Metabase.
- Concevoir des tableaux de bord plus interactifs.
- Développer mes compétences en data visualisation et en data storytelling.
- Mieux comprendre les besoins métiers afin de produire des analyses à forte valeur ajoutée.

---




## Résultat

Ce projet démontre la mise en place d'une chaîne complète d'analyse de données :

**Collecte → Stockage → Requêtage SQL → Préparation des données → Visualisation → Analyse décisionnelle**

avec PostgreSQL, Metabase et Docker.
