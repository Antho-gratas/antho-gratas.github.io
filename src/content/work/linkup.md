---
title: LinkUp
publishDate: 2024-06-06 00:00:00
img: /assets/LU.png
img_alt: LinkUp
description: |  
tags:
  - Dev
  - C#
  - Backend
---

<h3>Contexte</h3>

L’application d’administration LinkUp est une application qui a pour but de modérer et d’administrer le client web 
LinkUp qui est un réseau social qui permet la mise en relation des étudiants du lycée Chevrollier. Ce réseau 
social leur permet de poster des demandes de services de différents types. Cela permet de créer du contact et 
de l’entraide entre les étudiants. 

L’application a donc été réalisée à destination de l’équipe d’administration du réseau LinkUp. Celle-ci comporte 6
grandes fonctionnalités :
- La visualisation de statistiques
- La modération des demandes de services
- La modération des utilisateurs
- La gestion des signalements 
- La visualisation de différents types d’action
- L’import et la création de nouvelles données

Avant de nous intéresser à l’application en elle-même, intéressons-nous au schéma de la base de données et 
ses déclencheurs associés.



<h3>L'application</h3>

Description des différentes fonctionnalités :
1. Statistiques :
- Visualisation de différentes statistiques
- Utilisation d’une librairie externe (LiveCharts) pour un affichage en diagramme 

<img  src="/assets/capture-portfolio/LU/LU1.png">

2. Utilisateurs (clic droit sur un utilisateur pour effectuer des actions) :
- Modification/ajout d’utilisateur
- Gestion/modération des utilisateurs (bannissement, archivage)
- Utilisation d’un service de mail pour la gestion des mots de passe

<img  src="/assets/capture-portfolio/LU/LU2.png">

3. Annonces (ou services) :
- Visualisation des annonces
- Modération des annonces 

<img  src="/assets/capture-portfolio/LU/LU3.png">
<img  src="/assets/capture-portfolio/LU/LU4.png">

4. Modération :
- Visualisation des signalements utilisateurs
- Possibilité d’effectuer des actions pour répondre à ces signalements

<img  src="/assets/capture-portfolio/LU/LU5.png">

5. Journalisation
- Visualisation des actions de gestion et de modération effectuées par d’autres utilisateurs

<img  src="/assets/capture-portfolio/LU/LU6.png">

6. Import :
- Import de nouvelles données avec de nouveaux utilisateurs (passage à une nouvelle année scolaire)
- Fichier csv de type :
 Email;Classe;Section;Nom;Prénom;DateNaiss
 etudiant1@example.com;1TSSIO1;SIO;Doe;John;1990-01-01
 etudiant2@example.com;2TSSAM;SAM;Smith;Jane;1988-05-15
 etudiant3@example.com;1TSSP3S;SP3S;Johnson;Robert;1992-11-30*

<img  src="/assets/capture-portfolio/LU/LU7.png">

L’application a été rendue dans les temps. Cette création m’a permis d’aller plus loin dans l’utilisation et dans le
développement en C#. J’ai pu appréhender l’utilisation d’API depuis un client lourd, utiliser des librairies externes
et essayer de rendre un applicatif beaucoup plus poussé visuellement que les précédents.