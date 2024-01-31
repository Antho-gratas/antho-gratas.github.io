---
title: Plugin de gestion de license et vente de modules
publishDate: 2023-06-10 00:00:00
img: /assets/wordpress-1863504_1280.jpg
img_alt: Plugin de gestion de license et vente de modules
description: |
tags:
  - Dev
  - Wordpress
  - Back-end
  - API
---

<h3>Contexte</h3>
Dans le cadre de cette mission, l'objectif était de mettre en place une boutique de modules fonctionnant avec un système de licences.

Le processus est le suivant :

<ol>
<li>L'utilisateur achète un produit sur la boutique.</li>
<li>En plus du produit, l'utilisateur reçoit une clé de licence correspondante.</li>
<li>La licence permet aux utilisateurs d'utiliser le module et de recevoir des notifications en cas de mises à jour.</li>
<li>Les utilisateurs peuvent ensuite installer directement les mises à jour sur leur propre site où le module est actif, en utilisant leur clé de licence.</li>
</ol>

Ce système de licence facilite la gestion des mises à jour pour les utilisateurs et garantit qu'ils bénéficient des dernières fonctionnalités et correctifs de sécurité pour les modules qu'ils ont achetés.

<h3>Problématique</h3>
Comment vérifier une licence provenant d'un autre site et autoriser ou non son utilisation ?
<h3>Comment ca marche ?</h3>

Le moyen de vérifier les licences qui semble le plus adapté est d'utiliser une API pour communiquer entre le site du client et le site où les licences sont stockées.

Voici l'approche proposée :

<ol>
<li>Créer un site WordPress avec une boutique utilisant WooCommerce et répertorier tous les modules disponibles à la vente dans la boutique :</li>
<img  src="/assets/capture-portfolio/LM/LM1.PNG">
<li>Ajouter un gestionnaire de licences dans la section d'administration du site pour répertorier toutes les licences créées suite à un achat :</li>
<img  src="/assets/capture-portfolio/LM/LM7.PNG">
<li>Une fois qu'un client a acheté une licence, il peut consulté sa clé et télécharger le module via la rubrique "Mes licences" :</li>
<img  src="/assets/capture-portfolio/LM/LM2.PNG">
<li>Une fois qu'un client a installé le module correspondant sur son site, il peut entrer ses informations et sa clé de licence :</li>
<img  src="/assets/capture-portfolio/LM/LM3.PNG">
<li>Si la clé est non valide :</li>
<img  src="/assets/capture-portfolio/LM/LM4.PNG">
<li>Si la clé est valide :</li>
<img  src="/assets/capture-portfolio/LM/LM5.PNG">
<li>Une fois la licence validée, le client a accès au module et à ses mises à jour grace à l'API :</li>
<img  src="/assets/capture-portfolio/LM/LM6.PNG">
</ol>

Ici, pour créer la base j'ai utilisé un WordPress plugin boilerplate qui permet la création de plugin de base et de structuré son code.

Ensuite j'ai ajouté de nouvelles données personnalisées, nécessaire pour l'API, aux produits de ma boutiques :

<img  src="/assets/capture-portfolio/LM/LM8.PNG">

J'ai ensuite créé une nouvelle table dans la base de données WordPress pour y stocker les licences. De ce fait à chaque fois qu'un client achète un module, sa licence est générée et disponible sur son compte (seulement une fois le paiement réalisé).

Pour finir, grâce à une classe incluse dans chaque module, le client peut, depuis son propre site, entrer son mail et sa clé de licence associée au module. L'API vérifiera la validité de la clé et renverra des mises à jour s'il y en a de disponibles.
