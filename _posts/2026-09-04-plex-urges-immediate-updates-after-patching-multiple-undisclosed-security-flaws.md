---
title: 'Plex Urges Immediate Updates After Patching Multiple Undisclosed Security Flaws'
date: 2026-09-04
permalink: /posts/2026/09/04/plex-urges-immediate-updates-after-patching-multiple-undisclosed-security-flaws/
tags:
- veille-cyber
- hackernews
---
### Urgence de mise à jour pour Plex : Correction de vulnérabilités critiques

Plex a publié des correctifs de sécurité pour ses solutions Plex Media Server et Plex Desktop. Bien que les détails techniques précis des failles corrigées n'aient pas été divulgués pour le moment, l'éditeur insiste sur l'importance d'une mise à jour immédiate pour protéger les infrastructures.

**Points clés :**
*   **Versions corrigées :** Plex Media Server 1.43.3 et Plex Desktop 1.115.0.
*   **Indisponibilité potentielle :** Les utilisateurs de serveurs NAS peuvent ne pas trouver la mise à jour directement dans leur gestionnaire de paquets ; une installation manuelle est recommandée dans ce cas.
*   **Historique :** Plex est régulièrement une cible pour les attaquants. Par le passé, des vulnérabilités critiques (comme CVE-2025-34158 ou CVE-2020-5741) ont permis l'exfiltration de jetons d'accès administrateur ou l'installation de malwares sur les systèmes des utilisateurs.

**Vulnérabilités mentionnées :**
*   **CVE-2025-34158 (Score CVSS 8.5) :** Bug d'authentification lié aux points de terminaison `/myplex/account` et `/api/resources`, permettant à un utilisateur non privilégié d'accéder aux détails du compte propriétaire et de découvrir l'infrastructure du serveur.
*   **CVE-2020-5741 (Score CVSS 7.2) :** Faille exploitée historiquement pour implanter des malwares (utilisée notamment dans l'incident LastPass de 2022).

**Recommandations :**
*   Mettre à jour vers les versions **1.43.3 (Serveur)** et **1.115.0 (Desktop)** sans délai.
*   Procéder à une installation manuelle si la mise à jour automatique n'est pas encore proposée par le système d'exploitation du NAS.
*   Surveiller les prochaines annonces de sécurité de l'éditeur, car des identifiants CVE sont en cours d'attribution pour les vulnérabilités récemment corrigées.

---
[Source](https://thehackernews.com/2026/09/plex-urges-immediate-updates-after.html){:target="_blank"}
