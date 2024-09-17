# Documentation Technique - Cyclistic Case Study

### Structure du Répertoire
Le projet est structuré comme suit :

- **README.md** : Ce fichier fournit une vue d'ensemble sur la structure du repo et sur la documentation technique du projet.

- **src/** : Ce dossier contient le code source, les datasets et les fichiers liés à l'analyse.
  - **data/** : Ce sous-dossier contient les fichiers de données.
    - **data.zip** : Contient les fichiers ZIP des différentes données utilisées pour le projet.
  - **notebook/** : Ce dossier contient les notebooks Jupyter pour l'analyse exploratoire et le prétraitement des données.
  - **Tableau Dashboard/** : Contient les tableaux de bord créés avec Tableau pour la visualisation des données.
  - **Reporting/** : Contient les rapports générés à partir des analyses.

## 1. Introduction
Ce document décrit en détail le processus de nettoyage et de prétraitement des données utilisé dans le projet d'analyse des données de Cyclistic. Il couvre les étapes de chargement, de nettoyage, de transformation, ainsi que les techniques utilisées pour préparer les données pour l'analyse.

## 2. Chargement et Inspection des Données
### 2.1 Chargement des Données
Les données ont été chargées à partir de plusieurs fichiers CSV représentant des périodes mensuelles sur une année. Chaque fichier a été importé dans un dataframe pour une première inspection des données.

### 2.2 Fusion des Données
Après avoir vérifié la conformité des données pour chaque mois, les fichiers ont été fusionnés en un seul ensemble de données. Cette étape a permis de regrouper les trajets sur une année entière.

### 2.3 Standardisation et Fusion Finale
Les données ont été standardisées et fusionnées en un seul dataframe couvrant l'année complète. Le jeu de données final contient plus de 14 millions de lignes et 12 colonnes, dont les colonnes clés sont : `start_time`, `end_time`, `start_station_name`, `end_station_name`, et `user_type`. Les colonnes comme `gender` et `birthyear` contiennent des valeurs manquantes pour les utilisateurs de type "Customer" car elles sont disponibles uniquement pour les "Subscribers".

## 3. Nettoyage des Données
### 3.1 Vérification des Types de Données
Les types de données de chaque colonne ont été vérifiés pour s'assurer de leur conformité. Les colonnes ont été ajustées en fonction des besoins de l'analyse.

### 3.2 Identification des Données Manquantes
Les données manquantes ont été identifiées et traitées. Les lignes avec des valeurs manquantes dans les colonnes essentielles (comme `start_station_name` ou `end_station_name`) ont été éliminées.

### 3.3 Identification et Suppression des Doublons
Les doublons ont été identifiés et supprimés pour éviter les biais dans l'analyse.

### 3.4 Suppression des Colonnes Non Pertinentes
Les colonnes non pertinentes pour l'analyse ont été supprimées pour simplifier le jeu de données.

### 3.5 Conversion des Types de Données
- **Conversion des dates** : Les colonnes `start_time` et `end_time` ont été converties en objets datetime pour faciliter leur manipulation.
- **Catégorisation** : Les colonnes `gender` et `user_type` ont été converties en objets de type catégorie pour optimiser l'utilisation de la mémoire.
- **Optimisation des entiers** : La colonne `birthyear` a été convertie de `int64` à `Int32` pour réduire la consommation de mémoire.

## 4. Ingénierie des Caractéristiques
### 4.1 Création de la Colonne `ride_length`
Une colonne `ride_length` a été créée pour stocker la durée du trajet au format HH:MM:SS.

### 4.2 Extraction du Jour de la Semaine
Une colonne `day_of_week` a été créée pour stocker le jour de la semaine où chaque trajet a commencé.

## 5. Suppression des Données Inadéquates
### 5.1 Suppression des Données Incohérentes
Les lignes avec des valeurs incohérentes pour les utilisateurs de type "Customer" (par exemple, présence d’un `birthyear` ou d’un `gender`) ont été supprimées.

### 5.2 Suppression des Données Incomplètes
Les lignes avec des informations manquantes pour les colonnes `birthyear` ou `gender` pour les utilisateurs de type "Customer" ont été supprimées.

## 6. Finalisation et Vérification de la Qualité des Données
### 6.1 Vérification des Colonnes Catégorielles
Les colonnes catégorielles (`gender` et `user_type`) ont été vérifiées et les catégories incohérentes ont été supprimées.

### 6.2 Suppression des Doublons
Les doublons restants ont été éliminés pour garantir la qualité des données.

## 7. Détection et Traitement des Valeurs Aberrantes (Outliers)
### 7.1 Identification des Outliers
Les valeurs aberrantes, notamment dans la colonne `birthyear`, ont été identifiées à l'aide de boxplots et de statistiques descriptives.

### 7.2 Suppression des Outliers
Les valeurs aberrantes ont été supprimées à l'aide d'une fonction dédiée.

## 8. Données Nettoyées Finales
Après avoir complété les étapes de nettoyage et de prétraitement, le jeu de données est désormais beaucoup plus structuré et prêt pour l'analyse.

### 8.1 Lignes Supprimées
Environ 7% des lignes ont été supprimées en raison de données manquantes ou non pertinentes.

### 8.2 Nouvelles Colonnes
Les colonnes `ride_length` et `day_of_week` ont été ajoutées pour faciliter l'analyse approfondie des comportements de trajet.
