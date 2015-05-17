---
layout: post
title:  "Variables d’environnement et proxy réseau"
date:   2013-06-20
author: Eric Prunier
tags:
  - Technique
  - Système
  - Proxy
---

Variables d’environnement pour l’utilisation d’un proxy réseau
<!--break-->
:

* http_proxy
* ftp_proxy
* https_proxy
* http\_no\_proxy : liste d’hôtes séparés par "|" (les wildcards sont autorisés)
* no_proxy : liste d’hôtes séparés par "|" (les wildcards ne sont pas autorisés)

Exemples :

* http_proxy=http://example.com:8080
* http\_no\_proxy=localhost|192.168.*
* no_proxy=localhost|192.168.1.1
