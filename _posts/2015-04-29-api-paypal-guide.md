---
layout: post
title:  "Guide sur le design des APIs Paypal"
date: 2015-04-29
author: Eric Prunier
tags:
  - Technique
  - Bonnes pratiques
summary: |
  Paypal vient de mettre à disposition sur son compte GitHub un guide sur le design de ses APIs.
  
  Au delà de l'aspect purement documentaire, ce guide expose de façon simple et clair, bon nombre de bonnes pratiques en terme de design d'API RESTful.
---

Paypal vient de mettre à disposition sur son compte GitHub un [guide sur le design de ses APIs](https://github.com/paypal/api-standards/blob/master/api-style-guide.md).

Au delà de l'aspect purement documentaire, ce guide expose de façon simple et clair, bon nombre de bonnes pratiques en terme de design d'API RESTful.

On y trouve des sujets classiques comme :

- les verbes HTTP et leur utilisation
- les Statuts HTTP
- le templating d'URI
- le versionning
- le nommage des ressources

Ainsi que des sujets moins connus comme :

- [JSON patch](https://tools.ietf.org/html/rfc6902) pour définir la mise à jour partielle d'une ressource
- Les liens hypermédia
- les opérations complexes (ne pouvant être traitées comme des opérations de type CRUD)
- les ressources en lecture seul (pour permettre la mise en cache)

En conclusion, voici un guide qui constitue autant une source d'information concernant les principes sur lesquels sont basées les APIs Paypal, qu'une source d'inspiration pour tous les designers d'API.
