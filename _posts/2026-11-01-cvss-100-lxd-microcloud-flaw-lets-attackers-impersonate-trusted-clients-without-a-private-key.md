---
title: 'CVSS 10.0 LXD, MicroCloud Flaw Lets Attackers Impersonate Trusted Clients Without a Private Key'
date: 2026-11-01
permalink: /posts/2026/11/01/cvss-100-lxd-microcloud-flaw-lets-attackers-impersonate-trusted-clients-without-a-private-key/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans LXD et MicroCloud : usurpation d'identité

Une faille de sécurité critique affectant LXD et MicroCloud permet à un attaquant distant d'usurper l'identité d'un client de confiance sans posséder sa clé privée. En exploitant une mauvaise vérification de la chaîne de certificats TLS, un attaquant disposant d'un certificat public légitime peut tromper le serveur et obtenir des accès privilégiés, incluant potentiellement un accès « root » sur la machine hôte.

**Points clés :**
*   **Mécanisme :** Le serveur vérifie mal la chaîne de certificats TLS. Un attaquant peut joindre un certificat public de confiance (non secret) à sa propre chaîne de connexion ; le serveur valide alors l'identité usurpée.
*   **Conditions d'exploitation :** Nécessite un accès réseau à l'API HTTPS du serveur et la possession du certificat public d'un client déjà autorisé.
*   **Impact :** Accès complet au cluster, aux machines virtuelles et privilèges élevés sur l'hôte.
*   **Origine :** La vulnérabilité a été initialement identifiée par le projet Incus, qui a également corrigé le problème.

**Vulnérabilité :**
*   **CVE-2026-112816** (Score CVSS : 10.0)

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs via les commandes `sudo snap refresh lxd` et `sudo snap refresh microcloud`. Vérifier après la mise à jour que la version installée correspond aux versions corrigées (ex: LXD 6.10.1, MicroCloud 3.4.1).
*   **Restreindre l'accès :** En attendant la mise à jour, limiter strictement l'accès réseau aux API de LXD et MicroCloud pour réduire la surface d'attaque.
*   **Utilisateurs Incus :** Migrer vers la version 7.6.0 ou supérieure.

---
[Source](https://thehackernews.com/2026/11/critical-lxd-and-microcloud-flaw-cvss.html){:target="_blank"}
