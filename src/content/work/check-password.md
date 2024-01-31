---
title: Plugin de vérification de la complexité des mots de passe
publishDate: 2023-05-25 00:00:00
img: /assets/password.jpg
img_alt: Pearls of silky soft white cotton, bubble up under vibrant lighting
description: |
tags:
  - Wordpress
  - Dev
  - Plugin
---


<h3>Contexte</h3>
Les sites WordPress accompagnés d’une boutique WooCommerce proposent la possibilité de créer un compte lors de la validation d'une commande. Pour ne pas entraver le processus de commande, WordPress vérifie partiellement la complexité du mot de passe entré (fonction JavaScript facilement contournable) sans aller plus loin (histoire de ne pas décourager l’utilisateur).
Le but du plugin est donc de mettre en place une procédure de vérification de mot de passe afin de renforcer la sécurité du site.

<h3>Problématique</h3>
Comment mettre en place une politique de complexité du mot de passe sans entraver le processus de commande ?

<h3>Comment ca marche ?</h3>
On sépare la procédure en deux cas bien distincts :

<ul>
<li>Cas 1 : L’utilisateur essaye de s’inscrire de son plein gré sur la page de création d’un compte</li>
<li>Cas 2 : L’utilisateur essaye de s’inscrire au moment de valider une commande</li>
</ul>

<h5> Cas 1 :</h5>
Dans le cas 1, le plugin bloque toute tentative d’inscription avec un mot de passe faible. 
Ici j'essaye de m'enregistré avec un mot de passe faible :

<img  src="/assets/capture-portfolio/CP/CP4.PNG">

En forçant le JavaScript il est possible de passer avec ce genre de mot de passe :

<img  src="/assets/capture-portfolio/CP/CP5.PNG">

Mais grâce au plugin, l'inscription avec ce genre de mot de passe est impossible :

<img  src="/assets/capture-portfolio/CP/CP6.PNG">

<h5> Cas 2 :</h5>
Dans le cas 2, le plugin accepte n’importe quel mot de passe. L’utilisateur va jusqu’au bout de sa commande sans contrainte :

<img  src="/assets/capture-portfolio/CP/CP1.PNG">

Sa commande est bien reçue et validée mais une fois sur la page de validation, un petit encadré s’affiche, lui expliquant qu’il sera déconnecté et obligé de modifier son mot de passe pour accéder de nouveau à son compte :

<img  src="/assets/capture-portfolio/CP/CP2.PNG">

Il sera donc impossible pour lui de se connecter sans changer son mot de passe :

<img  src="/assets/capture-portfolio/CP/CP3.PNG">

Cela permet de garder la facilité du processus de commande tout en renforçant la procédure de vérification du mot de passe.

