---
title: 'Amazon Links Debug and Chalk npm Hijack to North Korea’s Sapphire Sleet'
date: 2026-07-30
permalink: /posts/2026/07/30/amazon-links-debug-and-chalk-npm-hijack-to-north-koreas-sapphire-sleet/
tags:
- veille-cyber
- hackernews
---
### Attribution des cyberattaques sur la chaîne d'approvisionnement npm à la Corée du Nord

Amazon Threat Intelligence a formellement attribué le piratage des paquets npm `debug` et `chalk` (survenu en septembre 2025) au groupe nord-coréen **Sapphire Sleet** (également identifié sous les noms UNC1069 ou Stardust Chollima). Cette campagne de compromission de mainteneurs, visant à détourner des cryptomonnaies, est désormais liée à d'autres attaques sur la chaîne d'approvisionnement, notamment celles visant les paquets `axios` et `typo-crypto`.

**Points clés :**
*   **Mode opératoire :** Les attaquants utilisent l'ingénierie sociale pour compromettre des comptes de mainteneurs légitimes, permettant la publication de mises à jour malveillantes.
*   **Techniques variées :** Les attaques utilisent soit des scripts d'installation (hook post-install), soit des intercepteurs côté navigateur (injection dans `fetch`/`XMLHttpRequest`) pour subtiliser des portefeuilles numériques.
*   **Évolution des menaces :** Le paquet `typo-crypto` est considéré par Amazon comme une phase de test pour affiner les tactiques utilisées ultérieurement sur des paquets à plus fort trafic.
*   **Preuves :** L'attribution repose sur le recoupement d'infrastructures de commande et de contrôle (C2), le réemploi de code malveillant et des méthodes d'obfuscation communes.

**Vulnérabilités identifiées :**
*   **MAL-2026-3400 :** Compromission du paquet `typo-crypto@4.3.0`.
*   **Non répertorié (CVE en attente/ouvert) :** Compromission des paquets `debug` et `chalk` (septembre 2025).

**Recommandations et mesures de sécurité :**
*   **Mise à jour de npm :** Utiliser npm v12 ou supérieur, qui désactive par défaut les scripts de cycle de vie des dépendances, limitant ainsi l'exécution automatique de code malveillant lors de l'installation.
*   **Vigilance sur les paquets :** Bien que npm ait introduit une analyse automatique des nouveaux paquets à la publication, cette mesure ne couvre pas le code déjà présent dans le registre. Il est conseillé de vérifier systématiquement l'authenticité des auteurs de dépendances.
*   **Audit de dépendances :** Surveiller les comportements suspects lors de l'exécution, notamment les tentatives d'accès à des APIs de portefeuilles ou des appels réseau vers des domaines inconnus, car ces attaques peuvent contourner les protections statiques.

---
[Source](https://thehackernews.com/2026/07/amazon-links-debug-and-chalk-npm-hijack.html){:target="_blank"}
