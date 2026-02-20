---
title: 'BeyondTrust Flaw Used for Web Shells, Backdoors, and Data Exfiltration'
date: 2026-02-20
permalink: /posts/2026/02/20/beyondtrust-flaw-used-for-web-shells-backdoors-and-data-exfiltration/
tags:
- veille-cyber
- hackernews
---
**Exploitation d'une faille critique dans les solutions BeyondTrust**

Une vulnérabilité de sécurité critique affectant les produits BeyondTrust Remote Support (RS) et Privileged Remote Access (PRA) est activement exploitée par des acteurs malveillants. Cette faille permet l'exécution de commandes système arbitraires dans le contexte de l'utilisateur du site, ouvrant la voie à diverses actions nuisibles.

**Points Clés :**

*   Des acteurs malveillants utilisent la vulnérabilité pour mener des activités allant de la reconnaissance réseau au déploiement de web shells, à l'établissement de canaux de commande et contrôle (C2), à l'installation de portes dérobées et d'outils de gestion à distance, au mouvement latéral au sein des réseaux et à l'exfiltration de données.
*   Les secteurs ciblés comprennent les services financiers, les services juridiques, la haute technologie, l'enseignement supérieur, le commerce de gros et de détail, ainsi que les soins de santé, dans plusieurs pays (États-Unis, France, Allemagne, Australie, Canada).
*   La campagne d'exploitation inclut l'installation de web shells persistants, le déploiement de malwares comme VShell et Spark RAT, et l'exfiltration de données sensibles telles que des fichiers de configuration, des bases de données internes et des dumps PostgreSQL vers des serveurs externes.
*   La vulnérabilité est similaire à une faille précédemment identifiée (CVE-2024-12356) concernant la validation des entrées, mais celle-ci affecte directement le code des solutions BeyondTrust.
*   La CISA a inclus cette vulnérabilité dans son catalogue des vulnérabilités connues et exploitées (KEV), confirmant son utilisation dans des campagnes de ransomware.

**Vulnérabilité :**

*   **CVE-2026-1731** (score CVSS : 9.9) : Permet l'exécution de commandes système arbitraires dans le contexte de l'utilisateur du site. La cause identifiée est un échec de sanitisation dans le script "thin-scc-wrapper", accessible via une interface WebSocket.

**Recommandations :**

Bien que l'article ne détaille pas spécifiquement les recommandations de mitigation pour cette CVE, la mention de la mise à jour du catalogue KEV par la CISA et la comparaison avec une vulnérabilité précédente suggèrent fortement la nécessité de :

*   Appliquer les correctifs de sécurité fournis par BeyondTrust pour les produits Remote Support (RS) et Privileged Remote Access (PRA).
*   Examiner et auditer les configurations des systèmes affectés.
*   Surveiller activement les journaux pour détecter toute activité suspecte indicative d'une exploitation.

---
[Source](https://thehackernews.com/2026/02/beyondtrust-flaw-used-for-web-shells.html){:target="_blank"}
