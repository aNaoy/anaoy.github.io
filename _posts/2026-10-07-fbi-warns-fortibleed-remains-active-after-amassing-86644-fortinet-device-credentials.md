---
title: 'FBI Warns FortiBleed Remains Active After Amassing 86,644 Fortinet Device Credentials'
date: 2026-10-07
permalink: /posts/2026/10/07/fbi-warns-fortibleed-remains-active-after-amassing-86644-fortinet-device-credentials/
tags:
- veille-cyber
- hackernews
---
### Campagne FortiBleed : alerte sur le vol massif d'identifiants Fortinet

La campagne « FortiBleed » constitue une menace active persistante visant les pare-feu FortiGate et les passerelles VPN SSL exposés sur Internet. Cette opération, attribuée à des groupes russophones, utilise le bourrage d'identifiants (*credential stuffing*) pour compromettre des équipements à grande échelle. À ce jour, plus de 86 644 identifiants ont été dérobés dans 194 pays. Les accès obtenus servent ensuite d'étape initiale pour des attaques de ransomwares (notamment liées aux groupes INC et Lynx).

**Points clés :**
* **Mode opératoire :** Une campagne en cinq étapes allant de la reconnaissance à l'exfiltration de données, en passant par l'utilisation de l'outil *FortigateSniffer* pour intercepter le trafic d'authentification.
* **Persistance :** Les attaquants créent de nouveaux comptes administratifs et suppriment parfois les comptes légitimes pour verrouiller l'accès aux administrateurs réseau.
* **Exploitation :** Utilisation de clusters GPU pour craquer hors ligne les hashs SHA-256 faibles et faciliter les mouvements latéraux et l'énumération Active Directory.

**Vulnérabilités :**
* Pas de CVE spécifique identifiée : l'attaque repose sur l'exploitation d'identifiants faibles ou compromis, facilitée par l'utilisation de l'algorithme de stockage de mots de passe obsolète (SHA-256) au lieu du standard robuste PBKDF2.

**Recommandations :**
* **Sécurité des accès :** Activer une authentification résistante au phishing pour tous les accès VPN et administratifs.
* **Hygiène des mots de passe :** Réinitialiser immédiatement les mots de passe des comptes VPN et administratifs, et configurer le stockage des identifiants via l'algorithme **PBKDF2**.
* **Audit et surveillance :** Passer en revue les journaux d'activité pour détecter des connexions suspectes ou la création de comptes non autorisés.
* **Maintenance :** Terminer toutes les sessions VPN SSL et administratives actives après la réinitialisation.
* **Réponse à incident :** En cas de compromission, isoler l'appareil, collecter les preuves et signaler l'incident aux autorités compétentes (FBI/USSS).

---
[Source](https://thehackernews.com/2026/10/fbi-warns-fortibleed-remains-active.html){:target="_blank"}
