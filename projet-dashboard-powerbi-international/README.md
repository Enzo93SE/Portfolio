## Conception des tableaux de bord Power BI
https://github.com/user-attachments/assets/8a233f2a-f7f2-437c-9d8c-c10b8b2a41f1


La première étape du projet a consisté à étudier les différents jeux de données fournis afin de construire un modèle de données cohérent et exploitable dans Power BI.

Pour enrichir notre analyse, nous avons intégré **plus de cinq sources de données externes**, principalement issues d'Eurostat et de jeux de données complémentaires. Ces différentes sources ont été reliées entre elles grâce à un modèle relationnel permettant de croiser les indicateurs démographiques et socio-démographiques.

Une part importante du travail a été consacrée à la préparation des données avant leur exploitation dans les tableaux de bord.

---

## Préparation et nettoyage des données

Avant toute analyse, les données ont été préparées à l'aide de **Power Query**.

Les principales opérations réalisées sont les suivantes :

* importation de plusieurs fichiers provenant de différentes sources ;
* harmonisation des noms de colonnes et des formats de données ;
* suppression des valeurs nulles ou incohérentes ;
* transformation des types de données (dates, nombres, textes) ;
* filtrage des informations non pertinentes ;
* fusion (Merge) et ajout (Append) de plusieurs tables ;
* création de colonnes calculées facilitant l'analyse ;
* construction des relations entre les différentes tables du modèle de données.

Ce travail de préparation a permis d'obtenir un modèle fiable et cohérent, garantissant la qualité des analyses réalisées dans Power BI.

---

## Développement sous Power BI

Une fois les données préparées, nous avons développé un rapport interactif composé de deux tableaux de bord complémentaires.

Le modèle de données repose sur plusieurs tables reliées entre elles afin de permettre une navigation fluide entre les différents indicateurs.

Le développement du rapport a notamment nécessité :

* la création d'un modèle relationnel reliant plus de cinq sources de données ;
* la définition des relations entre les différentes tables ;
* la création de mesures et d'indicateurs avec **DAX** ;
* la réalisation de visualisations interactives adaptées aux données étudiées ;
* la mise en place de filtres et segments pour faciliter l'exploration des données ;
* la conception d'une navigation simple entre les différentes pages du rapport.

Une attention particulière a été portée aux bonnes pratiques de visualisation des données, notamment concernant la lisibilité, l'utilisation des couleurs, la cohérence graphique et l'expérience utilisateur.

---

## Analyse des tableaux de bord

Le rapport est organisé autour de deux tableaux de bord.

### Dashboard 1 – Analyse démographique

Ce premier tableau de bord compare les principaux indicateurs démographiques entre **la Serbie** et **les Pays-Bas** :

* évolution de la population ;
* taux de natalité ;
* taux de mortalité ;
* indice de fécondité ;
* comparaison avec la moyenne de l'Union européenne (EU27_2020).

<img width="1657" height="940" alt="Capture d&#39;écran 2026-07-31 143929" src="https://github.com/user-attachments/assets/670db9a7-de76-4f17-bd35-06f936115172" />



### Dashboard 2 – Analyse socio-démographique

Le second tableau de bord présente des indicateurs permettant d'étudier les aspects sociaux de la population :

* nombre de mariages ;
* nombre de divorces ;
* évolution des indicateurs sociaux disponibles ;
* comparaison entre les deux pays et la moyenne européenne.

L'ensemble des visualisations permet d'identifier rapidement les tendances, les écarts et les similitudes entre les pays étudiés.

<img width="1673" height="947" alt="Capture d&#39;écran 2026-07-31 144926" src="https://github.com/user-attachments/assets/93055e82-ad19-43b6-9726-eff7c5ce2aad" />


