---
title: 'SAP fixes critical vulnerabilities in Commerce Cloud and S/4HANA'
date: 2026-05-12
permalink: /posts/2026/05/12/sap-fixes-critical-vulnerabilities-in-commerce-cloud-and-s4hana/
tags:
- veille-cyber
- bleepingcomp
---
### Correctifs critiques pour SAP Commerce Cloud et S/4HANA

SAP a publié ses mises à jour de sécurité de mai 2026, corrigeant 15 vulnérabilités affectant ses solutions phares, Commerce Cloud et S/4HANA. Bien qu'aucune exploitation active n'ait été détectée pour ces failles spécifiques, leur gravité impose une intervention rapide.

**Points clés :**
*   Le déploiement concerne 15 correctifs au total, incluant deux failles critiques, une de sévérité élevée et 11 de sévérité moyenne.
*   Les vulnérabilités touchent l'intégrité, la confidentialité et la disponibilité des données.
*   Parmi les autres risques identifiés figurent des injections de commandes, du XSS (Cross-Site Scripting), du CSRF (Cross-Site Request Forgery) et des dénis de service (DoS).

**Vulnérabilités critiques identifiées :**
*   **CVE-2026-34263 (SAP Commerce Cloud) :** Absence de vérification d'authentification due à une mauvaise configuration de *Spring Security*. Elle permet à un attaquant non authentifié d'exécuter du code arbitraire sur le serveur via le chargement de configurations malveillantes.
*   **CVE-2026-34260 (S/4HANA) :** Faille d'injection SQL permettant à un utilisateur disposant de privilèges de base d'accéder à des informations sensibles ou de provoquer l'arrêt de l'application.

**Recommandations :**
*   Appliquer immédiatement les correctifs fournis par le bulletin de sécurité SAP de mai 2026.
*   Prioriser la mise à jour des instances exposées en ligne, notamment Commerce Cloud, en raison de la facilité d'exploitation de la vulnérabilité CVE-2026-34263.
*   Assurer une veille continue sur les correctifs SAP, la CISA ayant déjà répertorié 14 failles SAP dans son catalogue d'exploitations connues, dont certaines ont été utilisées dans des attaques par ransomware.

---
[Source](https://www.bleepingcomputer.com/news/security/sap-fixes-critical-vulnerabilities-in-commerce-cloud-and-s-4hana/){:target="_blank"}
