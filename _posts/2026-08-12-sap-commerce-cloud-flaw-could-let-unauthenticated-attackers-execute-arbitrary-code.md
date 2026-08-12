---
title: 'SAP Commerce Cloud Flaw Could Let Unauthenticated Attackers Execute Arbitrary Code'
date: 2026-08-12
permalink: /posts/2026/08/12/sap-commerce-cloud-flaw-could-let-unauthenticated-attackers-execute-arbitrary-code/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans SAP Commerce Cloud et ses composants

SAP a publié des correctifs pour plusieurs vulnérabilités critiques, dont une faille majeure dans SAP Commerce Cloud permettant une exécution de code arbitraire (RCE) par des attaquants non authentifiés.

**Points clés :**
*   Les vulnérabilités touchent divers composants critiques, notamment Commerce Cloud, Manufacturing Integration and Intelligence (MII) et SAP NetWeaver.
*   Les failles identifiées permettent, dans les cas les plus graves, une prise de contrôle totale du système, une corruption mémoire ou l'exécution de commandes non autorisées.

**Vulnérabilités majeures :**
*   **CVE-2026-58231 (CVSS 10.0) :** Faille dans le *Data Hub Adapter* de SAP Commerce Cloud due à une validation insuffisante des entrées et une absence de contrôle d'autorisation, permettant une exécution de code arbitraire.
*   **CVE-2026-44772 (CVSS 9.9) :** Injection de code dans *Manufacturing Integration and Intelligence* permettant à un attaquant peu privilégié d'exécuter des commandes arbitraires sur l'hôte.
*   **CVE-2026-34265 (CVSS 9.8) :** Écriture hors limites dans *SAP NetWeaver (ABAP)* via le protocole DIAG, provoquant une corruption mémoire ou un crash système.
*   **CVE-2026-44758 (CVSS 9.1) :** Injection de code dans *Manufacturing Integration and Intelligence* (SSTI/SSRF) permettant l'exécution de commandes système.

**Recommandations :**
*   **Application des correctifs :** Appliquer immédiatement les mises à jour de sécurité publiées par SAP pour les versions impactées et procéder au redéploiement des composants mis à jour.
*   **Mesures temporaires :** Pour SAP Commerce Cloud, configurer un filtrage IP pour restreindre l'accès au point de terminaison vulnérable en attendant le patch.
*   **Configuration post-patch :** Pour la CVE-2026-44772, activer la propriété système "Secure Transformer" et définir une liste blanche d'hôtes autorisés pour le chargement des fichiers XSL.

---
[Source](https://thehackernews.com/2026/08/sap-commerce-cloud-flaw-could-let.html){:target="_blank"}
