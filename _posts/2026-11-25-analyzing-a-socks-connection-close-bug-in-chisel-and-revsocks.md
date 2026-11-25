---
title: 'Analyzing a SOCKS connection close bug in chisel and revsocks'
date: 2026-11-25
permalink: /posts/2026/11/25/analyzing-a-socks-connection-close-bug-in-chisel-and-revsocks/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse d'un bug de terminaison SOCKS dans Chisel et Revsocks

Des chercheurs de Synacktiv ont identifié un défaut de fonctionnement dans les outils de tunneling **Chisel** et **revsocks**, compromettant la fiabilité des connexions SOCKS5. Le bug empêche la propagation correcte d'une fermeture de connexion initiée par la cible (envoi d'un paquet FIN), laissant la session TCP dans un état *CLOSE_WAIT* indéfini côté serveur de proxy.

#### Points clés
* **Origine du problème :** Le bug réside dans l'utilisation de la bibliothèque `go-socks5`. La fonction de transfert (`proxy`) tente d'effectuer un `CloseWrite()` pour propager la fermeture, mais si l'interface utilisée pour le tunnel (le flux de données) ne supporte pas cette méthode, l'échec est silencieux.
* **Comportement constaté :** Le tunnel ne propage pas le FIN reçu de la cible vers le client SOCKS. Par conséquent, le client croit que la connexion est toujours ouverte et n'émet jamais de signal de fermeture, ce qui bloque le processus et empêche le nettoyage des ressources.
* **Différence avec SSH :** Contrairement à Chisel et revsocks, les tunnels SSH gèrent correctement la propagation de la fermeture, assurant une terminaison propre des deux côtés.

#### Vulnérabilités
Bien qu'il s'agisse d'un bug fonctionnel de gestion de protocole et non d'une faille de sécurité exploitée par un attaquant externe, le comportement peut entraîner :
* **Déni de service (DoS) par épuisement des ressources :** L'accumulation de connexions fantômes en attente (`CLOSE_WAIT`) peut saturer les descripteurs de fichiers et la mémoire du serveur proxy.
* **CVE :** Aucune CVE n'est associée à cette découverte, car il s'agit d'une correction d'implémentation logicielle.

#### Recommandations
* **Mise à jour des outils :**
    * Pour **Chisel** : Mettre à jour vers la version **1.12.0** ou supérieure, qui inclut le correctif officiel ajoutant la méthode `CloseWrite` au flux du tunnel.
    * Pour **revsocks** : Le correctif nécessite une mise à jour de la bibliothèque `yamux`. Il est conseillé de surveiller les mises à jour du projet ou d'appliquer manuellement un remplacement par une version implémentant `CloseWrite` (comme `libp2p/yamux` v1).
* **Développement :** Intégrer des tests d'automatisation qui vérifient la terminaison naturelle des processus (avec timeout) pour détecter rapidement les blocages de flux réseau.

---
[Source](https://www.synacktiv.com/en/publications/analyzing-a-socks-connection-close-bug-in-chisel-and-revsocks){:target="_blank"}
