---
layout: post
title:  "Requêtes HTTPS en Java via un proxy et sans vérification du hostname"
date:   2013-06-05
author: Eric Prunier
tags:
  - Technique
  - Réseau
  - Java
summary: |
  Création d’un client permettant d’effectuer des requêtes HTTP/HTTPS via un proxy.
  Pour les requête HTTPS, ce client autorise la connection même si le hostname du
  serveur ne correspond pas aux données du certificat SSL (par exemple dans le cas
  d’un certificat de test)...
---

Création d’un client permettant d’effectuer des requêtes HTTP/HTTPS via un proxy.
Pour les requête HTTPS, ce client autorise la connection même si le hostname du
serveur ne correspond pas aux données du certificat SSL (par exemple dans le cas
d’un certificat de test).

Ce code utilise Apache HttpComponents.

``` java
import javax.net.ssl.SSLContext;

import org.apache.http.HttpHost;
import org.apache.http.client.HttpClient;
import org.apache.http.conn.params.ConnRoutePNames;
import org.apache.http.conn.scheme.PlainSocketFactory;
import org.apache.http.conn.scheme.Scheme;
import org.apache.http.conn.scheme.SchemeRegistry;
import org.apache.http.conn.ssl.SSLSocketFactory;
import org.apache.http.impl.client.DefaultHttpClient;
import org.apache.http.impl.conn.tsccm.ThreadSafeClientConnManager;

public class SSLUtils {

  public static void main(String[] args) throws Exception {
    // Setup HTTP scheme
    Scheme httpScheme = new Scheme("http", 80, PlainSocketFactory.getSocketFactory());

    // Setup HTTPS scheme
    SSLContext sslcontext = SSLContext.getInstance("TLS");
    sslcontext.init(null, null, null);
    SSLSocketFactory sf = new SSLSocketFactory(sslcontext, SSLSocketFactory.ALLOW_ALL_HOSTNAME_VERIFIER);
    Scheme httpsScheme = new Scheme("https", 443, sf);

    // Create registry and add schemes
    SchemeRegistry schemeRegistry = new SchemeRegistry();
    schemeRegistry.register(httpScheme);
    schemeRegistry.register(httpsScheme);

    // Create HTTP client
    final ThreadSafeClientConnManager cm = new ThreadSafeClientConnManager(schemeRegistry);
    final HttpClient client = new DefaultHttpClient(cm);

    // Setup HTTP proxy
    final String proxyHost = "http://proxy.example.com";
    final int proxyPort = 12345;
    final HttpHost proxy = new HttpHost(proxyHost, proxyPort);
    client.getParams().setParameter(ConnRoutePNames.DEFAULT_PROXY, proxy);

    // Now we can use client to send requests....
  }
}
```
