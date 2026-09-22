---
title: 'WordPress Comment2Shell Flaw Can Turn Anonymous Comment XSS Into RCE via Admin Session'
date: 2026-09-22
permalink: /posts/2026/09/22/wordpress-comment2shell-flaw-can-turn-anonymous-comment-xss-into-rce-via-admin-session/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "Comment2Shell" dans WordPress

Une faille de sécurité majeure, identifiée sous le nom de **Comment2Shell**, permet à un visiteur anonyme de compromettre un site WordPress en injectant un script malveillant via un commentaire.

**Points clés :**
*   **Mécanisme :** L'attaque exploite une faille XSS (Cross-Site Scripting) causée par une mauvaise gestion des balises HTML lors de l'affichage des commentaires.
*   **Chaîne d'exploitation :** Lorsqu'un administrateur connecté consulte la page contenant le commentaire piégé, le script s'exécute automatiquement. Il utilise alors les privilèges de session de l'administrateur pour télécharger un plugin malveillant, permettant l'exécution de code à distance (RCE) sur le serveur.
*   **Conditions :** La faille affecte principalement les thèmes utilisant le système de blocs de WordPress, bien que certains thèmes classiques soient également vulnérables. Bien que soumise à la modération, la faille peut être exploitée si le commentaire est approuvé ou contourné par des méthodes spécifiques.

**Vulnérabilité :**
*   **CVE-2026-93485** : Score CVSS de 7.1/10.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer la version 7.1.1 de WordPress (ou la version spécifique à votre branche, disponible depuis la version 4.7).
*   **Mesures temporaires :** En cas d'impossibilité de mise à jour, désactiver les commentaires sur le site ou utiliser un pare-feu applicatif (WAF) pour bloquer les tentatives d'injection.
*   **Audit post-incident :** Si une compromission est suspectée, inspecter minutieusement les fichiers et les plugins installés sur le site, car la mise à jour ne nettoie pas les charges utiles déjà introduites par un attaquant.

---
[Source](https://thehackernews.com/2026/09/wordpress-comment2shell-flaw-can-turn.html){:target="_blank"}
