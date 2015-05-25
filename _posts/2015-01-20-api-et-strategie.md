---
layout: post
title:  "Publication d'API et stratégie"
date:   2015-01-20 22:50
author: Eric Prunier
tags:
  - Outils
  - Modélisation
summary: |
  En 2000 nous avons assisté au boom de l'Internet et depuis, plétore de services ont vu le jour, principalement sous la forme de sites Web. Depuis quelques années, nous voyons les éditeurs ouvrir de nouvelles voies d'accès à leurs services. En plus de l'exposition aux êtres humains via le Web, ces services peuvent maintenant être consommés par d'autres services via des APIs...
---

En 2000 nous avons assisté au _boom_ de l'Internet et depuis, plétore de services ont vu le jour, principalement sous la forme de sites Web. Depuis quelques années, nous voyons les éditeurs ouvrir de nouvelles voies d'accès à leurs services. En plus de l'exposition aux êtres humains via le Web, ces services peuvent maintenant être consommés par d'autres services via des APIs.

Dans son article _[Don’t API all the things … The downside of public APIs](http://softwareas.com/apis-considered-harmful-maybe/)_, Michael Mahemoff liste les inconvénients liés à la publication d'API. Cependant ces inconvénients sont également autant de facteurs de succès lors de l'_APIsation_ d'un service, considérons les alors comme des points d'attention sans leur donner de connotation positive ou négative. Comment ces points doivent-ils être traités et y a t'il une stratégie à mettre en oeuvre ?

La question stratégique a été abordée par Daniel Jacobson dans son article _[Why you probably don’t need an API strategy](http://thenextweb.com/entrepreneur/2013/09/15/why-you-probably-dont-need-an-api-strategy/)_ qui a créé la polémique et donné lieu à d'autres articles :

* [Why You Probably Need an API Strategy](http://blogs.intel.com/application-security/2013/09/18/why-you-probably-need-an-api-strategy/)
* [Why your API IS your Strategy](http://www.3scale.net/2014/02/why-your-api-is-your-strategy/)
* [API Strategy and API Tactic](https://www.linkedin.com/pulse/api-strategy-tactic-manfred-bortenschlager)

Dans ces articles, des sociétés comme Netflix et Twilio sont prisent en exemple pour étayer le débat : les APIs constituent-elles un produit à part entière ou n'est-ce qu'un moyen (une tactique) marketing pour développer un service via différents canaux de distribution ?

A cette question, il n'y a peut être pas de réponse unique et c'est peut être à chacun de déterminer quel importance accorder à la publication d'APIs : est-ce stratégique pour mon service ? pour mon activité ?
Voici un autre article pour apporter de l'eau au moulin... ou pas : [The Strategic Value of APIs](https://hbr.org/2015/01/the-strategic-value-of-apis).

Voici maintenant quelques points d'attention à l'usage des fournisseurs d'APIs.

## Gestion de versions
Contrairement à un site Web qui peut évoluer à tout moment sans que cela n'impact réellement l'utilisateur, une API publiée à une durée de vie qui peut être relativement longue (certains clients ne sont pas prèt à faire évoluer leur application à chaque évolution de l'API). Chaque version d'une API doit donc être traitée avec le même égard et considérée comme un coût à long terme.

## Qualité de service
L'utilisation d'une API génére une charge supplémentaire au niveau de l'infrastructure système et réseau. Cette infrastructure doit donc être prévue pour pouvoir gérer une montée en charge proportionnelle au succès de l'API, d'autant plus que le nombre [d'appels à l'API peut devenir plus important que le nombre de vues Web](http://www.programmableweb.com/news/does-open-data-demand-api-first-approach/analysis/2014/12/31).

## Fonctionnalités
Les fonctionnalités accessibles via l'API sont prioritaires. Le fait de ne pas en exposer certaines, pourtant disponible via d'autres canaux, peut générer une impression négative auprès des clients et les pousser vers un concurrent.

## Gestion de la communauté des développeurs
Un soin particulier doit être apporté à la communauté des développeurs qui représente un facteur clé quant à l'image de l'API. Un travail important est à prévoir autour du référencement de l'API ([ProgrammableWeb](http://programmableweb.com), [Mashape](http://mashape.com), [APIs.io](http://apis.io)) et de sa documentation (modélisation Swagger, API Blueprint ou RAML, exemples d'utilisation et toolkit via un dépôt GitHub...).
