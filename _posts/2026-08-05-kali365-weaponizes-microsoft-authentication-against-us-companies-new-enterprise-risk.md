---
title: 'Kali365 Weaponizes Microsoft Authentication Against US Companies: New Enterprise Risk'
date: 2026-08-05
permalink: /posts/2026/08/05/kali365-weaponizes-microsoft-authentication-against-us-companies-new-enterprise-risk/
tags:
- veille-cyber
- hackernews
---
### Kali365 : Une menace émergente par détournement de jetons Microsoft

Kali365 est un kit de phishing sophistiqué qui exploite le processus d'authentification légitime de Microsoft 365 pour compromettre les accès en entreprise, ciblant principalement les organisations américaines.

**Points clés :**
* **Mécanisme d'attaque :** Le kit utilise des leurres (SharePoint, OneDrive, DocuSign) pour inciter la victime à s'authentifier sur le portail Microsoft légitime via un code d'appareil fourni par l'attaquant.
* **Conséquences :** Une fois le code approuvé par l'utilisateur, les attaquants obtiennent des jetons d'accès et de rafraîchissement (OAuth), leur permettant de persister durablement sur les comptes mails, documents et ressources cloud.
* **Impact métier :** Risques élevés de fraude financière (BEC), exfiltration de données sensibles, perturbations opérationnelles et coûts de remédiation accrus.
* **Vulnérabilités :** L'attaque repose sur l'abus de fonctionnalités légitimes de Microsoft (Device Code Flow) plutôt que sur une faille logicielle spécifique (CVE). Il n'y a donc pas de CVE associée, car il s'agit d'une exploitation de la confiance accordée au processus d'authentification.

**Recommandations :**
* **Intelligence sur les menaces :** Intégrer des flux d'indicateurs de compromission (IOC) dynamiques dans les outils de sécurité (SIEM, SOAR, pare-feu) pour bloquer les domaines et infrastructures malveillantes en rotation constante.
* **Analyse comportementale :** Utiliser des bacs à sable (sandboxes) interactifs pour examiner non seulement les URL, mais aussi les redirections, les scripts et les comportements suspects lors du processus d'authentification.
* **Surveillance proactive :** Effectuer des recherches régulières sur les campagnes actives (via des outils de Threat Intelligence) pour identifier les motifs de ciblage spécifiques à son secteur d'activité.
* **Sensibilisation et visibilité :** Améliorer la capacité des équipes de niveau 1 (Tier 1) à détecter les anomalies dans le flux de connexion et à révoquer rapidement les jetons compromis pour limiter la durée de l'exposition.

---
[Source](https://thehackernews.com/2026/08/kali365-weaponizes-microsoft.html){:target="_blank"}
