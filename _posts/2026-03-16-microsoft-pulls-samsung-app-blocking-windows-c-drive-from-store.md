---
title: 'Microsoft pulls Samsung app blocking Windows C: drive from Store'
date: 2026-03-16
permalink: /posts/2026/03/16/microsoft-pulls-samsung-app-blocking-windows-c-drive-from-store/
tags:
- veille-cyber
- bleepingcomp
---
### Incident technique : Blocage d'accès au disque C: sur les PC Samsung

Microsoft a retiré l'application « Samsung Galaxy Connect » du Microsoft Store suite à un bug critique provoquant une erreur « Accès refusé » sur le lecteur C: des PC Samsung Galaxy Book 4 et certains modèles de bureau sous Windows 11.

**Points clés :**
*   **Symptômes :** Impossibilité d'accéder au disque système, blocage du lancement d'applications (Office, Outlook, navigateurs) et échec des tâches administratives.
*   **Cause identifiée :** Une mise à jour défectueuse de l'application Samsung Galaxy Connect, utilisée pour la synchronisation entre appareils.
*   **État actuel :** L'application a été supprimée du Store et remplacée par une version stable antérieure. Les solutions de récupération pour les systèmes déjà corrompus sont actuellement limitées.

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident spécifique (il s'agit d'un dysfonctionnement logiciel et non d'une faille de sécurité). 
*   *Note :* L'article mentionne brièvement une mise à jour hors bande (OOB) pour corriger une vulnérabilité RCE dans le service RRAS (Routing and Remote Access Service) sur Windows 11 Entreprise, sans préciser de CVE.

**Recommandations :**
*   **Utilisateurs impactés :** Contacter directement le support technique de Samsung pour obtenir une assistance spécifique à leur modèle.
*   **Administrateurs :** Surveiller les communications de Microsoft et de Samsung pour l'arrivée d'un correctif de réparation pour les machines déjà affectées.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-pulls-samsung-app-blocking-windows-c-drive-from-store/){:target="_blank"}
