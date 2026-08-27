---
title: 'Critical Avada WordPress theme flaw enables zero-click RCE'
date: 2026-08-27
permalink: /posts/2026/08/27/critical-avada-wordpress-theme-flaw-enables-zero-click-rce/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique RCE dans le thème WordPress Avada

Une chaîne de vulnérabilités critiques affecte le thème Avada pour WordPress ainsi que son plugin associé, Fusion Builder. Cette faille permet à un attaquant non authentifié d'exécuter du code PHP arbitraire sur le serveur (RCE) sans aucune interaction utilisateur (zero-click), offrant un contrôle total sur les sites compromis.

**Points clés :**
*   **Impact massif :** Plus d'un million de sites utilisant Avada sont potentiellement exposés, car le plugin Fusion Builder est systématiquement installé avec le thème.
*   **Complexité :** L'attaque repose sur une chaîne de six vulnérabilités distinctes (autorisation, validation d'entrée, détournement de contexte, etc.) exploitées en séquence.
*   **Détection automatisée :** La faille a été identifiée en seulement deux heures par "Argus", un système d'IA agentique développé par l'équipe Wordfence.

**Vulnérabilité :**
*   **CVE-2026-18431** : Score de sévérité critique de **9.8**.
*   **Versions affectées :** Avada jusqu'à la version 7.16 et Fusion Builder jusqu'à la version 3.16.

**Recommandations :**
*   **Mise à jour immédiate :** Mettre à jour le thème Avada vers la version **7.16.1** ou supérieure et le plugin Fusion Builder vers la version **3.16.1** ou supérieure.
*   **Vigilance :** Compte tenu de la criticité du score et de la facilité d'exploitation, l'application des correctifs est urgente pour prévenir l'installation de malwares ou la prise de contrôle administrative du site.

---
[Source](https://www.bleepingcomputer.com/news/security/critical-avada-wordpress-theme-flaw-enables-zero-click-rce/){:target="_blank"}
