# Conception et implémentation d'une base de données relationnelle

## 📖 Présentation du projet

**Durée :** 2 mois
**Équipe :** 2 étudiants
**Note obtenue :** 16/20

Dans le cadre de la SAÉ 2.01, nous avons conçu et implémenté une base de données relationnelle dédiée au commerce international des technologies à faible empreinte carbone.

L'objectif était de maîtriser l'ensemble du cycle de conception d'une base de données, depuis la modélisation jusqu'à l'exploitation des données pour l'aide à la décision.

---

## Objectifs

* Concevoir un modèle de données adapté à une problématique réelle.
* Réaliser un schéma Entité-Association (MEA).
* Traduire le modèle conceptuel en schéma relationnel.
* Normaliser la base de données jusqu'à la forme BCNF.
* Implémenter la base de données en SQL.
* Alimenter et nettoyer les données.
* Exploiter les données via des requêtes analytiques et des tableaux de bord.

---

## 🛠️ Technologies utilisées

* SQL
* PostgreSQL
* Metabase
* Modélisation Entité-Association (MEA)
* Normalisation BCNF

---

## Conception de la base de données

La première étape du projet a consisté à modéliser les données à l'aide d'un **Modèle Entité-Association (MEA)**.

Ce modèle a ensuite été traduit en un schéma relationnel normalisé jusqu'à la **forme normale de Boyce-Codd (BCNF)** afin de garantir :

* la cohérence des données ;
* la réduction des redondances ;
* une meilleure maintenabilité de la base.

### Modèle Entité-Association



<img src="Modèle MEA.png" alt="MEA" width="50%">

---

## 🗄️ Implémentation SQL

Une fois le modèle validé, nous avons développé les scripts SQL permettant :

* la création des tables ;
* la définition des clés primaires et étrangères ;
* l'intégration des contraintes d'intégrité ;
* l'alimentation automatique de la base de données.

Nous avons également réalisé des opérations de :

* nettoyage des données ;
* transformation des fichiers sources ;
* dépivotage de données tabulaires complexes.

### Exemple de création de table

```sql
SELECT   
c1.name AS exporter_country,  
c2.name AS partner_country,  
SUM(tb.valeur) AS total_exports_usd  
FROM tradebalance_bilateral tb  
JOIN Country c1 ON  
tb.idCountry1 = c1.idCountry  -- Exportateur  
JOIN Country c2 ON  
tb.idCountry2 = c2.idCountry  -- importateur  
JOIN Annee a ON tb.idAnnee = a.idAnnee  
WHERE a.annee = 2009  
AND tb.idIndicator = 5  -- Exports of low carbon technology products  
AND tb.idUnit = (SELECT idUnit FROM Unit WHERE name = 'US Dollars')  
GROUP BY c1.name, c2.name  
ORDER BY total_exports_usd DESC  
LIMIT 10; 
```

---

## Analyse et visualisation des données

Après l'implémentation de la base, les données ont été exploitées avec Metabase afin de produire des indicateurs décisionnels.

Les analyses réalisées ont notamment porté sur :

* les échanges commerciaux internationaux ;
* les flux d'importation et d'exportation ;
* la balance commerciale des différents pays ;
* les technologies à faible empreinte carbone.

### Exemple de visualisation

Une carte interactive a été créée afin de représenter la balance commerciale mondiale.

> Ajouter ici une capture d'écran du dashboard Metabase.

```text
/images/balance-commerciale.png
```

---

## ompétences développées

Ce projet m'a permis de renforcer mes compétences dans plusieurs domaines :

### Base de données

* Conception de modèles Entité-Association.
* Traduction d'un modèle conceptuel en schéma relationnel.
* Normalisation jusqu'à la BCNF.

### SQL

* Création et administration de bases de données.
* Écriture de requêtes complexes.
* Gestion des contraintes et des relations entre tables.

### Préparation des données

* Nettoyage des données.
* Transformation et intégration de fichiers plats.
* Dépivotage de données.

### Business Intelligence

* Création de requêtes analytiques.
* Construction de tableaux de bord.
* Production d'indicateurs décisionnels avec Metabase.

---

## 📈 Axes d'amélioration

Pour continuer à progresser, je souhaite :

* approfondir mes connaissances en modélisation de données ;
* concevoir des modèles MEA plus optimisés ;
* développer mes compétences SQL avancées ;
* améliorer mes méthodes de nettoyage et de préparation des données ;
* explorer davantage les fonctionnalités de Metabase ;
* réaliser de nouveaux projets de bases de données sur des jeux de données réels.

---



## Résultat

Ce projet valide notre capacité à concevoir, implémenter et exploiter une base de données relationnelle complète dans un contexte professionnel.

De la modélisation des données jusqu'à la création d'indicateurs décisionnels, nous avons mis en œuvre les principales étapes d'un projet de gestion et d'analyse de données.

## ⚖️ Droits d’auteur et confidentialité

© Enzo Selvaratnam – Tous droits réservés.  
  Elles ne peuvent pas être diffusées ou réutilisées en dehors du cadre pédagogique initial. Le dépôt ne contient que des éléments dérivés (structure du fichier, explications, exemples anonymisés) et pas les données sensibles d’origine. 
