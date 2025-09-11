---
title: 'September Patch Tuesday handles 81 CVEs'
date: 2025-09-11
permalink: /posts/2025/09/11/september-patch-tuesday-handles-81-cves/
tags:
- veille-cyber
- sophos
---
### Mises à jour de sécurité de septembre : 81 vulnérabilités corrigées

Microsoft a publié 81 correctifs couvrant 15 familles de produits. Parmi ceux-ci, 9 sont considérés comme critiques et 9 ont un score CVSS de base de 8.0 ou plus. Aucune des vulnérabilités corrigées n'est connue pour être exploitée activement, bien qu'une vulnérabilité affectant le protocole SMB (CVE-2025-55234) ait été divulguée publiquement.

**Points clés :**

*   **Nombre total de CVE corrigées :** 81
*   **Vulnérabilités divulguées publiquement :** 1
*   **Vulnérabilités exploitées activement :** 0
*   **Gravité :** 9 critiques, 72 importantes
*   **Types d'impact :** Élévation de privilèges (38), Exécution de code à distance (22), Divulgation d'informations (15), Déni de service (3), Contournement de fonctionnalités de sécurité (2), Usurpation d'identité (1).
*   **Scores CVSS :** 1 avec un score de base de 9.0 ou plus, 9 avec un score de base de 8.0 ou plus.
*   **Produits les plus touchés :** Windows (58), Office 365 (13), Office (13).

**Vulnérabilités notables :**

*   **CVE-2025-55234 :** Vulnérabilité d'élévation de privilèges dans le protocole SMB de Windows. Divulguée publiquement et jugée susceptible d'exploitation.
*   **CVE-2025-55232 :** Vulnérabilité d'exécution de code à distance dans Microsoft High Performance Compute (HPC) Pack. Gravité importante mais score CVSS de base élevé (9.8), potentiellement exploitable sans interaction utilisateur.
*   **CVE-2025-53799 :** Vulnérabilité de divulgation d'informations dans le composant d'imagerie Windows, affectant également Office pour Android. Gravité critique, pourrait servir de petite partie d'une chaîne d'attaque plus large.
*   **CVE-2025-54897 :** Vulnérabilité d'exécution de code à distance dans Microsoft SharePoint. Gravité importante avec un score CVSS de base de 8.8.
*   **CVE-2025-54107 et CVE-2025-54917 :** Deux vulnérabilités de contournement de fonctionnalités de sécurité liées à `MapUrlToZone`. Gravité importante, affectant notamment Windows 10.

**Recommandations :**

*   Appliquer les mises à jour de sécurité publiées par Microsoft dès que possible.
*   Pour les utilisateurs de Windows, utiliser l'outil `winver.exe` pour identifier la version du système d'exploitation et télécharger le package de mise à jour cumulative approprié depuis le catalogue Windows Update.
*   Pour les environnements utilisant Microsoft HPC Pack, s'assurer qu'ils s'exécutent sur un réseau de confiance protégé par des règles de pare-feu spécifiques pour le port TCP 5999.
*   Pour les administrateurs, utiliser les informations fournies dans l'article pour prioriser le déploiement des correctifs, en particulier pour les vulnérabilités critiques et celles jugées plus susceptibles d'être exploitées.

---
[Source](https://news.sophos.com/en-us/2025/09/10/september-patch-tuesday-handles-81-cves/){:target="_blank"}
