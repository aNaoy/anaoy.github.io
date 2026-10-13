---
title: 'Attacker Chains Three Ivanti Connect Secure Zero-Days for Root Access, Only Two Patched So Far'
date: 2026-10-13
permalink: /posts/2026/10/13/attacker-chains-three-ivanti-connect-secure-zero-days-for-root-access-only-two-patched-so-far/
tags:
- veille-cyber
- hackernews
---
### Chaînage de vulnérabilités Zero-Day sur Ivanti Connect Secure

Des attaquants exploitent une chaîne de trois vulnérabilités Zero-Day dans les boîtiers VPN Ivanti Connect Secure pour obtenir un accès root sans authentification préalable. Bien qu'Ivanti ait publié des correctifs pour deux de ces failles, la vulnérabilité permettant l'élévation de privilèges reste, à ce jour, non corrigée.

**Points clés :**
* **Attaquant :** Le groupe suivi sous le nom de « UTA0576 » utilise ces failles pour dérober des identifiants (y compris LDAP) et effectuer des attaques par pulvérisation de mots de passe.
* **Complexité :** L'attaque est furtive ; les modifications sont effectuées en mémoire, ce qui permet de contourner l'outil d'intégrité (Integrity Checker Tool) d'Ivanti.
* **État actuel :** Ivanti confirme des exploitations limitées « dans la nature ». La CISA a classé cette menace comme active avec un impact total.

**Vulnérabilités :**
* **CVE-2026-104935 :** Regroupe une faille de contournement d'authentification et une exécution de code à distance (RCE), permettant une exécution sous l'utilisateur `cgi-server` (Score CVSS : 8.6/10).
* **Vulnérabilité d'élévation de privilèges (non CVE à ce jour) :** Permet à l'attaquant de passer de l'accès `cgi-server` à l'accès `root`.

**Recommandations :**
* **Mise à jour immédiate :** Appliquer les correctifs vers les versions sécurisées (ex: 25.1.3.1 ou 22.8R2.5 selon le modèle).
* **Analyse forensique :** En cas de suspicion de compromission, effectuer des analyses de mémoire et de réseau, car l'outil d'intégrité natif d'Ivanti est insuffisant pour détecter cette attaque spécifique.
* **Surveillance des indicateurs (IoC) :** Surveiller les accès suspects vers `/dana-na/auth/url_default/welcome.cgi`, la présence de l'en-tête `X-DSCGI-PATH` et toute activité inhabituelle dans le répertoire `/data/.icscap/`.

---
[Source](https://thehackernews.com/2026/10/attacker-chains-three-ivanti-connect.html){:target="_blank"}
