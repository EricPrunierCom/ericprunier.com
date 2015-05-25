---
layout: post
title:  "Introduction au machine learning - 1ère partie"
date:   2013-06-04
author: Eric Prunier
tags:
  - Présentation
  - Machine learning
summary: |
  Ce type d’apprentissage permet de “prédire” la classe ou la valeur d’un nouvel élément
  en fonction d’éléments déjà connus. La prédiction d’une valeur continue (ex: détermination
  d’un prix) donne lieu à un problème de régression, tandis que la prédiction d’une valeur
  discrète (ex: classification en tant que spam ou non spam d’un email) donne lieu à un problème
  de classification...
---

##Présentation de l’apprentissage supervisé

Ce type d’apprentissage permet de “prédire” la classe ou la valeur d’un nouvel élément
en fonction d’éléments déjà connus. La prédiction d’une valeur continue (ex: détermination
d’un prix) donne lieu à un problème de régression, tandis que la prédiction d’une valeur
discrète (ex: classification en tant que spam ou non spam d’un email) donne lieu à un problème
de classification.

La mise en oeuvre de l’apprentissage supervisé s’effectue en deux temps :

1. la phase d’apprentissage durant laquelle l’algorithme est “entraîné” à partir des
   éléments connus.
2. la phase de prédiction durant laquelle l’algorithme est appliqué à de nouveaux éléments
   afin d’en déduire la valeur de sortie.
