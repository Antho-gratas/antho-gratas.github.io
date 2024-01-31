---
title: Plugin Api google place
publishDate: 2023-06-15 00:00:00
img: /assets/google-76517_640.jpg
img_alt: Plugin Api google place
description: |  
tags:
  - Dev
  - Wordpress
  - Backend
---

<h3>Contexte</h3>
Lorsque l'on recherche un lieu référencé sur Google, il est possible que celui-ci possède une note et des avis. Le but de ce plugin est de pouvoir récupérer cette note et ces avis afin de les réutiliser sur notre propre site. Par exemple pour les afficher.
Pour cela, Google met à disposition une API nommée Google Places API qui permet la récupération de ces données.

<h3>Problématique</h3>
Comment récupérer et utiliser les informations fournies par Google place API ?

<h3>Approche</h3>
L'approche est la suivante : Nous allons utiliser les "places ID" pour afficher les bonnes informations aux bons endroits.


Un Place ID (identifiant de lieu) est une chaîne de caractères alphanumériques unique qui identifie de manière spécifique un lieu donné dans la base de données de Google. Chaque lieu répertorié dans Google Maps et dans Google Places, possède un Place ID qui lui est attribué.


L'ID de lieu permet d'identifier de manière précise un établissement, une adresse, un point d'intérêt ou tout autre lieu géographique répertorié dans Google. Cela inclut des lieux tels que des restaurants, des hôtels, des magasins, des parcs, des monuments, des bureaux, etc.

<h3>Mise en place</h3>
Le plugin ajoute un champ "place ID" pour chaque type de publication WordPress où l'on souhaite afficher des informations :

<img src="/assets/capture-portfolio/GN/GN6.PNG">

Il ajoute également une section côté administrateur qui permet d'ajouter sa clé d'API pour utiliser Google Places:

<img src="/assets/capture-portfolio/GN/GN7.PNG">

Ensuite, plusieurs shortcodes (petites fonctions) sont ajoutés avec le plugin. Chacun permet différentes fonctionnalités :
<ul>
<li>[note_google] : affiche la note d'un endroit précis :</li>
<img src="/assets/capture-portfolio/GN/GN1.PNG">
<li>[note_global] : affiche la note globale liée à tous les place ID enregistrés dans la base de données du site :</li>
<img src="/assets/capture-portfolio/GN/GN3.PNG">
<li>[avis_google] : permet de récupérer les commentaires liés à un lieu spécifique :</li>
<img src="/assets/capture-portfolio/GN/GN2.PNG">
<li>[avis_global] : permet de récupérer les commentaires de tous les place ID enregistrés dans la la base de données du site :</li>
<img src="/assets/capture-portfolio/GN/GN4.PNG">
<li>[hours_google] : permet d'afficher les horaires d'un lieu spécifique :</li>
<img src="/assets/capture-portfolio/GN/GN5.PNG">
</ul>

Ainsi, en effectuant les bonnes requêtes sur l'API Google Places, il est possible de récupérer différentes données liés à un lieu et de les afficher sur son propre site.