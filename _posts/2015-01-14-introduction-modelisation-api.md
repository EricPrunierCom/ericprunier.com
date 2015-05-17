---
layout: post
title:  "Introduction aux outils de modélisation d'API RESTful"
date:   2015-01-14 00:23
author: Eric Prunier
tags:
  - Outils
  - Modélisation
  - Swagger
  - RAML
  - Api Blueprint
---
Ces dernières années différentes initiatives ont été lancées dans le domaine de la modélisation et de la documentation d'API RESTful :

* Swagger
* API Blueprint
* RAML

Chacune est née d'un besoin spécifique et bien que ces initiatives tendent à se rejoindre en terme de fonctionnalités, leurs approches différent.
<!--break-->

Ces trois solutions sont open source. Swagger est la plus ancienne et beaucoup d'outils la supportent. RAML est la plus récente mais attire déjà l'attention de bon nombre d'acteurs du marché.

## Swagger
[Swagger](http://swagger.io) a été créé en juillet 2011 par la société *Reverb* afin de documenter l'API de leur application *Wordnik* de façon plus souple qu'avec de simples pages statiques.

Swagger adopte une approche bottom-up permettant la génération de documentation à partir du code et ceci pour différents langages. Une modelisation top-down est également possible, notamment via Swagger Editor qui a vu le jour en 2014.

La spécification Swagger définit un format de description d'API basé sur JSON, destiné à être exposé de façon interactive via Swagger UI, une console Web autonome pouvant être intégrée dans n'importe quel site Web ou utilisée de façon standalone.

Spécifications [2.0](https://github.com/swagger-api/swagger-spec/blob/master/versions/2.0.md), [1.2](https://github.com/swagger-api/swagger-spec/blob/master/versions/1.2.md), [1.1](https://groups.google.com/forum/#!topic/swagger-swaggersocket/mHdR9u0utH4)

## API Blueprint
[API Blueprint](http://apiblueprint.org) a été créé en mai 2013 par la société [Apiary](http://apiary.io) pour leur service de modélisation d'API en ligne.

Contrairement à Swagger, API Blueprint adopte une approche top-town avec un langage orienté documentation basé sur le format Markdown permettant aux utilisateurs de modéliser leurs APIs sans passer par un format technique comme JSON. *Snow Crash*, le parseur de référence permet, quant à lui, de générer un modèle JSON à partir de la description Markdown.

Le site d'API Blueprint référence différents outils à commencer par Apiary.io. On y trouve également des plugins pour les éditeurs [Atom](http://atom.io) et Sublime Text, des serveurs de mocks, des générateurs de documentation...

[Spécifications](https://github.com/apiaryio/api-blueprint/blob/master/API%20Blueprint%20Specification.md)

## RAML
[RAML](http://raml.org) (RESTful API Modeling Language) a été créé en octobre 2013 par la société MuleSoft. RAML est une spécification ouverte gérée par un groupe de travail incluant AngularJS, Intuit, Box, Paypal, API Evangelist, Programmable Web, SOA Software et Cisco.

RAML adopte la même approche top-down que API Blueprint, mais en utilisant YAML comme format de description. Il est également possible de générer une description RAML à partir de code Java/JAX-RS via un projet spécifique développé par MuleSoft.

Bien que RAML soit l'initiative la plus récente, la page [projet](http://raml.org/projects.html) du site référence un bon nombre d'outils. On y trouve API Designer et API Console développé par MuleSoft, Restlet Studio développé par [Restlet](http://restlet.com) ainsi que d'autres outils comme des convertisseurs ou des générateurs de code mis à disposition par d'autres contributeurs.

[Spécifications](http://raml.org/spec.html)
