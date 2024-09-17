# Rapport d'Analyse - Cyclistic Bike-Share Project

## 1. Introduction
Dans le cadre de l'analyse des données de *Cyclistic*, une entreprise de partage de vélos à Chicago, nous avons exploré les habitudes d’utilisation des vélos par deux segments clés : les **Customers** (utilisateurs occasionnels) et les **Subscribers** (membres annuels). L'objectif était de comprendre leurs comportements distincts et de proposer des recommandations afin d'améliorer les services et d'augmenter les conversions de Customers en Subscribers.

## 2. Objectifs du Projet
L’analyse vise à répondre aux questions suivantes :
- Quelle est la différence de comportement entre les Customers et les Subscribers en termes de durée de trajet, jours et heures d'utilisation ?
- Comment optimiser les services pour chaque groupe d’utilisateurs ?
- Quelles stations sont les plus populaires et comment ajuster l’offre de vélos en fonction des pics d'utilisation ?

## 3. Méthodologie
Les données couvrent une année complète de trajets, et les étapes suivantes ont été menées :
- **Nettoyage des données** : correction des incohérences et suppression des données incorrectes (durée de trajets négative, trajets hors de la plage normale).
- **Analyse exploratoire** : segmentation des utilisateurs, identification des périodes de pointe, et analyse des stations les plus fréquentées.
- **Visualisation** : utilisation d'outils tels que R et Tableau pour créer des visualisations graphiques facilitant l'interprétation des résultats.

## 4. Analyse des Données

### Capture d'écran du Tableau de Bord
![Tableau de Bord Cyclistic](C:\Users\bad\Pictures\Screenshots\Capture d'écran 2024-09-17 090436.png)

### Lien vers le Tableau de Bord sur Tableau Public
Pour explorer le tableau de bord interactif, veuillez visiter le lien suivant :  
[Tableau de Bord Cyclistic sur Tableau Public](https://public.tableau.com/app/profile/alseiny.diallo/viz/CyclisticCaseStudy_17265589409460/DivvyDashboard?publish=yes)

### 4.1 Durée moyenne des trajets
- **Customers** : Effectuent des trajets plus longs, en moyenne **2153 secondes** (soit environ **36 minutes**). Cela suggère une utilisation à des fins récréatives, comme des excursions touristiques ou des randonnées.
- **Subscribers** : Effectuent des trajets plus courts, en moyenne **753 secondes** (environ **13 minutes**), ce qui indique une utilisation plus fonctionnelle, probablement pour des trajets domicile-travail.

  _**Visualisation** : Graphique comparant la durée moyenne des trajets des deux groupes._

### 4.2 Jours les plus actifs
- **Subscribers** : Utilisent majoritairement les vélos en **semaine** (du lundi au vendredi), renforçant l’idée d’une utilisation professionnelle ou routinière.
- **Customers** : Préfèrent les **week-ends**, avec un pic notable le **samedi** et le **dimanche**, ce qui suggère une utilisation à titre récréatif.

  _**Visualisation** : Graphique illustrant l’activité quotidienne des deux segments._

### 4.3 Heures de pointe
- Les **Customers** utilisent principalement les vélos entre **10h et 19h**, avec un pic autour de **15h**, ce qui correspond à une utilisation pour les activités touristiques ou récréatives.
  
  _**Visualisation** : Courbe représentant le volume d’utilisation horaire des vélos par les Customers._

### 4.4 Stations les plus fréquentées
- **Customers** : Se concentrent autour des stations touristiques, telles que **Streeter Dr & Grand Ave**, près de Navy Pier, une zone touristique populaire à Chicago.
- **Subscribers** : Utilisent principalement les stations proches des centres d’affaires, comme **Canal St & Adams St**, située dans le quartier financier de Chicago.

  _**Visualisation** : Carte des stations les plus fréquentées par chaque type d'utilisateur._


## 5. Recommandations
Sur la base des insights dégagés de l'analyse des données, nous proposons les recommandations suivantes :

1. **Instaurer une réduction sur les longs trajets pour les Customers** :  
   Les **Customers** effectuant des trajets plus longs que les **Subscribers**, offrir des réductions ou des promotions pour ces trajets pourrait encourager un usage accru et augmenter leur fidélisation.

2. **Développer des promotions en semaine pour les Subscribers** :  
   Les **Subscribers** étant plus actifs en semaine, proposer des offres exclusives pourrait accroître l'utilisation quotidienne et renforcer leur engagement avec l'entreprise.

3. **Créer des offres attractives pour les Customers les week-ends** :  
   En raison de l’activité accrue des **Customers** pendant le week-end, des offres ciblées pourraient capitaliser sur cette tendance, notamment des forfaits "week-end" ou des réductions spéciales.

4. **Assurer une disponibilité suffisante des vélos aux heures de pointe pour les Customers** :  
   Pour améliorer l'expérience utilisateur, il est crucial d'optimiser la disponibilité des vélos autour des **zones touristiques** entre **10h et 19h**, en particulier autour de 15h.

5. **Optimiser la répartition des vélos selon les stations populaires** :  
   En semaine, prioriser la disponibilité des vélos dans les **zones d'affaires** pour les **Subscribers** et concentrer les vélos dans les **zones touristiques** le week-end pour les **Customers** permettrait de mieux répondre aux pics de demande.

## 6. Conclusion
Cette analyse a permis d'identifier des différences significatives entre les habitudes d’utilisation des **Customers** et des **Subscribers**. Les insights recueillis permettent de proposer des actions stratégiques visant à optimiser l'expérience utilisateur et à encourager la conversion des utilisateurs occasionnels en membres annuels, tout en maximisant l'efficacité opérationnelle de Cyclistic.
