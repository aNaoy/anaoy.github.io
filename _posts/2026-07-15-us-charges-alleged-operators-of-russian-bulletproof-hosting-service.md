---
title: 'US charges alleged operators of Russian bulletproof hosting service'
date: 2026-07-15
permalink: /posts/2026/07/15/us-charges-alleged-operators-of-russian-bulletproof-hosting-service/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement d'un réseau d'hébergement "bulletproof" russe

La justice américaine a inculpé trois ressortissants russes — Aleksandr Volosovik, Yulia Pankova et Kirill Zatolokin — pour avoir exploité les services d'hébergement "bulletproof" (BPH) **Media Land** et **ML.Cloud**. Ces plateformes ont facilité des cyberattaques mondiales, notamment des déploiements de rançongiciels (Lockbit, Blacksuit, Play) et des attaques DDoS contre des infrastructures critiques, engendrant plus de 62 millions de dollars de préjudices.

**Points clés :**
* **Nature du service :** Le BPH consiste à louer des serveurs en ignorant délibérément les signalements d'abus et les requêtes de démantèlement des autorités.
* **Infrastructure globale :** Le réseau opérait depuis la Russie tout en exploitant des serveurs situés aux États-Unis, en Chine, aux Pays-Bas et en Finlande.
* **Sanctions internationales :** Les États-Unis, le Royaume-Uni, l'Australie et l'Union européenne ont imposé des sanctions coordonnées contre les individus et les entités impliqués.
* **Prime :** Le programme *Rewards for Justice* offre jusqu'à 10 millions de dollars pour toute information sur les liens entre ces opérateurs et des gouvernements étrangers.

**Vulnérabilités :**
* Bien qu'aucune CVE spécifique ne soit liée à l'infrastructure elle-même, ces services ont permis l'exploitation active de vulnérabilités logicielles non patchées pour déployer des malwares et des outils de commande et contrôle (C2).

**Recommandations :**
* **Renforcement de la surveillance :** Utiliser des outils de simulation d'attaques (BAS) pour tester l'efficacité des solutions EDR/SIEM face aux infrastructures de serveurs connues pour héberger des activités malveillantes.
* **Veille sur les menaces :** Surveiller les communications réseau sortantes vers des plages IP identifiées comme "bulletproof" ou à haut risque.
* **Protection des infrastructures critiques :** Appliquer une politique de patching rigoureuse pour limiter l'impact des exploitations initiales souvent hébergées par ces fournisseurs.

---
[Source](https://www.bleepingcomputer.com/news/security/us-charges-alleged-russian-bulletproof-hosting-service-operators/){:target="_blank"}
