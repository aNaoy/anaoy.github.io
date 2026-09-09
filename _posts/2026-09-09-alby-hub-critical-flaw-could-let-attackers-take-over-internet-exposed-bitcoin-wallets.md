---
title: 'Alby Hub Critical Flaw Could Let Attackers Take Over Internet-Exposed Bitcoin Wallets'
date: 2026-09-09
permalink: /posts/2026/09/09/alby-hub-critical-flaw-could-let-attackers-take-over-internet-exposed-bitcoin-wallets/
tags:
- veille-cyber
- hackernews
---
### Faille Critique dans Alby Hub : Risque de Prise de Contrôle de Wallets Bitcoin

Alby a émis une alerte concernant une vulnérabilité critique affectant **Alby Hub**, un portefeuille Bitcoin auto-hébergé. Cette faille permettait à un attaquant de prendre le contrôle total d'un portefeuille et de détourner des fonds si l'instance était exposée sur Internet. À ce jour, au moins un cas d'exploitation confirmée a été rapporté.

**Points clés :**
*   La vulnérabilité touche les versions **v1.7.0 à v1.18.5**.
*   Le risque est limité aux instances accessibles publiquement via Internet.
*   Alby Hub est conçu pour fonctionner sur un réseau privé, mais certaines documentations d'installation (Cloud/Docker) encourageaient par erreur une exposition publique.
*   Un correctif a été déployé dans la version **v1.19.0** et ultérieures.

**Vulnérabilités :**
*   Aucun identifiant CVE spécifique n'a été publié à ce stade, la société ayant opté pour une divulgation responsable différée. La faille permet une prise de contrôle à distance (Remote Code/Account Takeover) sur les instances exposées.

**Recommandations de sécurité :**
1.  **Vérification :** Identifiez la version de votre Alby Hub.
2.  **Isolation immédiate :** Si vous utilisez une version vulnérable (v1.18.5 ou antérieure), restreignez immédiatement l'accès à l'interface de gestion (via pare-feu ou configuration Docker `127.0.0.1:8080` au lieu de `0.0.0.0:8080`).
3.  **Mise à jour :** Effectuez la mise à jour vers la version **v1.24.0** (la plus récente).
4.  **Assainissement :** Si votre instance a été exposée à Internet avant la mise à jour, changez impérativement votre mot de passe de déverrouillage et contactez le support de sécurité (`security@getalby.com`).

---
[Source](https://thehackernews.com/2026/09/alby-hub-critical-flaw-could-let.html){:target="_blank"}
