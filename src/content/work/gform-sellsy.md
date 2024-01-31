---
title: Plugin de transfert de formulaire de contact Gravity vers Sellsy
publishDate: 2023-06-24 00:00:00
img: /assets/sellsy.jpg
img_alt: Plugin de transfert de formulaire de contact Gravity vers Sellsy
description: |
tags:
  - Wordpress
  - Dev
  - API
---

<h3>Contexte</h3>

Le but de ce plugin est donc d'automatiser l'insertion de nouveaux contacts directement à partir d'un formulaire Gravity. Il faut aussi que le contact soit associé à son entreprise et que le formulaire relie le contact à un "pipe" en lui créant une opportunité.

<h3>Problématique</h3>
Comment inséré un nouveau contact sur la plateforme Sellsy par le biais de formulaire Gravity ?

<h3>Comment ca marche ?</h3>

Sellsy propose une API à ses clients. L'approche pour intégrer les formulaires Gravity Form à Sellsy est la suivante :

<ol>
<li>Création du contact : Les champs du formulaire Gravity Form sont liés aux propriétés de référence pour les contacts Sellsy.</li>
<li>Création de l'entreprise associée : Le formulaire permet également de créer une entreprise associée au contact.</li>
<li>Lien entre le contact et l'entreprise : Les informations du formulaire sont utilisées pour lier le contact à l'entreprise.</li>
<li>Création de l'opportunité associée au pipe : Une fois le contact et l'entreprise créés et liés, une opportunité est créée et associée au pipe spécifié.</li>
</ol>

Ainsi, chaque champ du formulaire est associé à une propriété de référence dans Sellsy, permettant de récupérer les données saisies et de les envoyer aux emplacements appropriés. En suivant ces étapes, les informations du formulaire peuvent être intégrées de manière automatique et structurée dans Sellsy, facilitant ainsi la gestion des contacts et des opportunités.

Le plugin ajoute des réglages supplémentaires pour Gravity Forms afin de faciliter l'intégration avec Sellsy :

<ul>
<li>Configuration des identifiants de compte Sellsy et des appels API :</li>

<img  src="/assets/capture-portfolio/GFS/GFS1.PNG">
<li>Association des formulaires à un pipe spécifique du compte Sellsy via les réglages :</li>

<img  src="/assets/capture-portfolio/GFS/GFS2.PNG">
</ul>

Pour chaque champ de formulaire, une méta-donnée est ajoutée, contenant la valeur saisie et la référence à la propriété associée dans l'API Sellsy :

<img src="/assets/capture-portfolio/GFS/GFS3.PNG">

Lors de l'envoi d'un formulaire, les valeurs saisies ainsi que les références des propriétés associées sont collectées et organisées dans des tableaux distincts.

Enfin, les données sont envoyées vers l'API de Sellsy pour créer le contact et effectuer les liaisons appropriées avec les autres entités.
