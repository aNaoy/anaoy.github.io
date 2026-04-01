---
title: 'TeamPCP Supply Chain Campaign: Update 005 - First Confirmed Victim Disclosure, Post-Compromise Cloud Enumeration Documented, and Axios Attribution Narrows, (Wed, Apr 1st)'
date: 2026-04-01
permalink: /posts/2026/04/01/teampcp-supply-chain-campaign-update-005-first-confirmed-victim-disclosure-post-compromise-cloud-enumeration-documented-and-axios-attribution-narrows-wed-apr-1st/
tags:
- veille-cyber
- sans-isc
---
### Évolution de la campagne TeamPCP : Victimes confirmées et cyberespionnage d'État

**Points clés**
*   **Première victime officielle :** Mercor AI a confirmé une violation de données massive (4 To exfiltrés) via la compromission de LiteLLM, prouvant l'impact réel et destructeur de la chaîne d'approvisionnement TeamPCP.
*   **Tactiques cloud exposées :** Le groupe utilise l'outil *TruffleHog* pour valider les secrets volés, puis effectue une énumération rapide (en moins de 24h) des environnements AWS/Azure (IAM, EC2, S3) avec des noms de ressources explicites (« pawn », « massive-exfil »).
*   **Incident Axios :** L'attaque via le paquet npm Axios a été formellement attribuée au groupe nord-coréen **UNC1069**. Bien que TeamPCP ne soit pas l'auteur direct, il est probable que le groupe UNC1069 exploite les mêmes réservoirs de jetons d'accès volés.
*   **Stabilisation de LiteLLM :** BerriAI a repris ses publications après un audit forensique par Mandiant, confirmant que seules les versions 1.82.7 et 1.82.8 étaient malveillantes.

**Vulnérabilités**
*   **CVE-2026-33634 :** Compromission de l'infrastructure de build liée à Trivy. ownCloud a confirmé une exposition de sa chaîne de production, illustrant les risques de la supply chain logicielle.

**Recommandations**
*   **Gestion des accès :** Procéder à une rotation immédiate des jetons d'accès, clés API et identifiants VPN pour tout environnement ayant utilisé les versions vulnérables de LiteLLM (v1.82.7 et v1.82.8).
*   **Détection cloud :** Analyser les journaux d'audit à la recherche de requêtes inhabituelles d'énumération IAM/EC2/S3. Rechercher spécifiquement des ressources nommées « pawn » ou « massive-exfil ».
*   **Remédiation Axios :** Si les versions 1.14.1 ou 0.30.4 d'Axios ont été déployées, vérifier la présence d'IOC spécifiques :
    *   macOS : `/Library/Caches/com.apple.act.mond`
    *   Windows : `%PROGRAMDATA%\wt.exe`
    *   Linux : `/tmp/ld.py`
    *   Bloquer le domaine `sfrclak[.]com` et l'IP `142.11.206[.]73`.
*   **Transparence :** Suivre l'exemple d'ownCloud en pratiquant une divulgation proactive en cas de suspicion d'exposition de la chaîne de compilation.

---
[Source](https://isc.sans.edu/diary/rss/32856){:target="_blank"}
