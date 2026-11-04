---
title: 'China-Aligned Hackers Hijack Sogou Input Method DNS Requests to Deploy DarkVigil Backdoor'
date: 2026-11-04
permalink: /posts/2026/11/04/china-aligned-hackers-hijack-sogou-input-method-dns-requests-to-deploy-darkvigil-backdoor/
tags:
- veille-cyber
- hackernews
---
### Campagne de cyberespionnage via le détournement de Sogou Input Method

Le groupe de menace SlippyNunchucks, aligné sur les intérêts chinois, mène une campagne de surveillance active ciblant des organisations et des individus sinophones en Asie et en Europe. Les attaquants exploitent les communications HTTP non sécurisées de logiciels populaires, notamment Sogou Input Method, pour déployer le backdoor modulaire « DarkVigil » (alias FDMTP).

**Points clés :**
*   **Mode opératoire :** Les attaquants pratiquent le détournement DNS pour intercepter les requêtes HTTP légitimes d'applications vers leurs serveurs de mise à jour.
*   **Vecteur d'attaque :** Utilisation du composant `SGTool.exe` de Sogou pour télécharger des charges utiles malveillantes, suivies d'une technique de *DLL sideloading* (utilisant un exécutable Adobe légitime et une DLL malveillante).
*   **Ciblage :** Surveillance accrue d'organisations opérant dans le secteur des jeux d'argent en ligne, une activité strictement réglementée par la Chine.
*   **Outil malveillant :** DarkVigil utilise le protocole DMTP pour le contrôle et la commande (C2), permettant le déploiement de plus de 20 plugins pour le vol de données et la persistance.

**Vulnérabilités :**
*   **CVE-2026-120422 :** Vulnérabilité liée à l'utilisation du protocole HTTP non chiffré dans Sogou Input Method, permettant le détournement de configuration.
*   **CVE-2026-51990 :** Faille précédemment exploitée par le groupe UNC3569 pour déployer le backdoor GRAYRABBIT.
*   **CVE-2021-38003 :** Utilisation d'un moteur Chromium obsolète et non isolé dans les composants de Sogou.

**Recommandations :**
*   **Mise à jour immédiate :** Mettre à jour Sogou Input Method vers la version 16.10 ou supérieure, qui corrige le défaut de communication en imposant le HTTPS.
*   **Surveillance réseau :** Surveiller les requêtes DNS suspectes vers des domaines de mise à jour connus et bloquer le trafic vers les IP associées aux serveurs de staging identifiés (47.239.250.102 et 47.237.122.175).
*   **Durcissement :** Limiter l'utilisation de logiciels tiers dont les mécanismes de mise à jour ne garantissent pas l'intégrité des communications par TLS/HTTPS.

---
[Source](https://thehackernews.com/2026/11/china-aligned-hackers-hijack-sogou.html){:target="_blank"}
