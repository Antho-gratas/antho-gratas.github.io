---
title: Plugin d'amélioration de Wordfence et MainWp
publishDate: 2024-01-20 00:00:00
img: /assets/wordfence.jpg
img_alt: Plugin d'amélioration de Wordfence et MainWp
description: |
tags:
  - Dev
  - Wordpress
  - Back-end
  - API
---

<h3>Contexte</h3>

Wordfence est un plugin de sécurité pour les sites web WordPress. Il offre plusieurs fonctionnalités visant à protéger votre site contre les attaques, les logiciels malveillants et d'autres menaces potentielles.
MainWP Client Reports est une extension pour le plugin MainWP, qui est conçu pour la gestion centralisée de plusieurs sites WordPress. L'extension Client Reports ajoute des fonctionnalités spécifiques liées à la génération de rapports pour les clients.

Les rapports sont donc générés automatiquement chaque mois pour ensuite être envoyés au client à qui appartient le site.
Les différentes données qu’il est possible de récupérer sont gérées par le biais de différents tokens qui sont associés à différents bouts de codes qui sont exécuté au moment où le token est mis sur la page de rapport.

L’extension MainWp client report propose de nombreux tokens qui répertorie des stats associés à différentes extensions qui pourraient être présentes sur le site enfant. On voudrait rajouter des données personnalisées sur les rapports, mais celles-ci ne sont pas disponibles avec l’extension de base.

Les données en question sont :
<ul>
<li>Le nombre d’attaques bloquées par Wordfence sur le mois</li>
<li>Le top 5 des sources des différentes attaques</li>
<li>Les différents types d’attaques et leur nombre (brute force...)</li>
</ul>

Le but de la mission est donc de créer un plugin qui permettrait l’ajout de tokens personnalisés pour récupérer les données voulues.

<h3>Problématique</h3>
Comment récupérer les données d’un site enfant depuis le site maître pour les traiter et les utiliser sur les rapports MainWp ?
<h3>Comment ca marche ?</h3>

On va créer 2 plugins. L’un pour le site enfant, l’autre pour le site maître.

Le plugin du site enfant va ajouter une route qui va permettre de récupérer de nouvelles données à chaque synchronisation de site depuis le site maître.

Le plugin du site maître va ajouter 3 nouveau tokens : 

<img  src="/assets/capture-portfolio/WMP/WMP4.png">

Les données sont maintenant utilisables dans les rapports générés par MainWp Client report :

<img  src="/assets/capture-portfolio/WMP/WMP3.png">
<img  src="/assets/capture-portfolio/WMP/WMP2.png">