---
title: 'China-Linked Hackers Target Asian Governments, NATO State, Journalists, and Activists'
date: 2026-05-01
permalink: /posts/2026/05/01/china-linked-hackers-target-asian-governments-nato-state-journalists-and-activists/
tags:
- veille-cyber
- hackernews
---
### Campagnes d'espionnage et cyber-harcèlement liés à la Chine

Des groupes de pirates informatiques alignés sur les intérêts chinois mènent actuellement des campagnes d'espionnage sophistiquées ciblant les secteurs gouvernementaux et de la défense en Asie et en Europe, ainsi que des journalistes et militants de la société civile.

**Points clés :**
* **SHADOW-EARTH-053 :** Groupe actif depuis décembre 2024, spécialisé dans l'exploitation de serveurs Microsoft Exchange et IIS pour infiltrer des institutions gouvernementales (Pakistan, Thaïlande, Malaisie, Inde, Myanmar, Sri Lanka, Taiwan et Pologne).
* **GLITTER CARP et SEQUIN CARP :** Acteurs ciblant des journalistes (notamment du consortium ICIJ) et des militants (ouïghours, tibétains, hongkongais) via des techniques d'ingénierie sociale et de hameçonnage (phishing).
* **Méthodes :** Utilisation de logiciels malveillants comme *ShadowPad* et *Noodle RAT*, déploiement de web shells (*Godzilla*), détournement de DLL, et utilisation d'outils de tunnelisation open-source pour maintenir l'accès.
* **Transnationalisme :** Les attaques contre les journalistes et activistes s'inscrivent dans une stratégie de répression numérique transnationale, potentiellement menée par des prestataires contractuels pour le compte de l'État chinois.

**Vulnérabilités exploitées :**
* Exploitation généralisée de vulnérabilités « N-day » sur les serveurs **Microsoft Exchange** et **IIS**.
* **CVE-2025-55182 (React2Shell) :** Utilisée pour distribuer des versions Linux de malwares comme *Noodle RAT*.

**Recommandations :**
* **Mises à jour critiques :** Appliquer immédiatement les derniers correctifs de sécurité et mises à jour cumulatives pour Microsoft Exchange et toutes les applications hébergées sur IIS.
* **Filtrage périmétrique :** En cas d'impossibilité de patching immédiat, déployer des systèmes de prévention d'intrusion (IPS) ou des pare-feu d'application web (WAF) avec des règles de « patch virtuel » pour bloquer les tentatives d'exploitation connues.
* **Sécurité des comptes :** Sensibiliser les utilisateurs (notamment les cibles à haut risque) aux tactiques d'impersonation et à la vigilance face aux jetons OAuth et aux e-mails de phishing sophistiqués.

---
[Source](https://thehackernews.com/2026/05/china-linked-hackers-target-asian.html){:target="_blank"}
