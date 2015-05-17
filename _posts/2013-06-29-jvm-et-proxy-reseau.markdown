---
layout: post
title:  "JVM et proxy réseau"
date:   2013-06-29
author: Eric Prunier
tags:
  - Technique
  - Java
  - Proxy
---

Paramètres de la JVM à positionner lorsque le traffic réseau doit passer par un proxy
<!--break-->
:

* http.proxyHost
* http.proxyPort
* https.proxyHost
* https.proxyPort
* http.nonProxyHosts : liste d’hôtes séparés par un "|" (les wildcards sont autorisés)

__Exemple :__ -Dhttp.proxyHost=example.com -Dhttp.proxyPort=8080 -Dhttp.nonProxyHosts=localhost|192.168.*
