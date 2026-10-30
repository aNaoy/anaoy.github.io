---
title: 'WordPress RCE Flaw Draws Nearly 63,000 Attack Attempts in Just 24 Hours'
date: 2026-10-30
permalink: /posts/2026/10/30/wordpress-rce-flaw-draws-nearly-63000-attack-attempts-in-just-24-hours/
tags:
- veille-cyber
- hackernews
---
### Recrudescence d'attaques RCE contre WordPress Core

Une vulnérabilité critique affectant le noyau WordPress (versions 4.7 à 7.1.3) fait l'objet d'une campagne d'exploitation massive, avec près de 63 000 tentatives d'attaques enregistrées en seulement 24 heures.

**Points clés :**
*   **Nature de la faille :** Exécution de code à distance (RCE) via une condition de concurrence (*race condition*).
*   **Mécanisme :** Lors d'une mise à jour complète, WordPress décompresse les fichiers dans un répertoire temporaire prévisible (`wp-content/upgrade`). Si ce répertoire est accessible via le web, un attaquant peut interagir avec l'installeur durant la courte fenêtre de mise à jour pour exécuter du code PHP arbitraire.
*   **Gravité :** Score CVSS de 8.1.
*   **Vulnérabilité :** Identifiant CVE non attribué (vulnérabilité propre au noyau WordPress).
*   **Mode opératoire :** Les attaquants effectuent un sondage automatisé et intensif sur les chemins d'accès aux fichiers d'installation pour tenter de capturer la fenêtre de mise à jour, qui ne dure que quelques secondes.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à la version **7.1.4**, qui corrige spécifiquement ce problème.
*   **Surveillance :** Inspecter les journaux d'accès à la recherche de requêtes suspectes visant le répertoire `wp-content/upgrade`.
*   **Audit de sécurité :** Rechercher tout signe de compromission, tel que l'apparition de nouveaux comptes administrateurs, de plugins inconnus ou de fichiers PHP suspects.

---
[Source](https://thehackernews.com/2026/10/wordpress-rce-flaw-draws-nearly-63000.html){:target="_blank"}
