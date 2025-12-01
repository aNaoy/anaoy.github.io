---
title: 'SmartTube YouTube app for Android TV breached to push malicious update'
date: 2025-12-01
permalink: /posts/2025/12/01/smarttube-youtube-app-for-android-tv-breached-to-push-malicious-update/
tags:
- veille-cyber
- bleepingcomp
---
**Compromission de SmartTube : Mise à jour malveillante distribuée via les clés du développeur**

L'application populaire SmartTube pour Android TV a été compromise suite au vol des clés de signature numériques de son développeur. Cette brèche a permis l'injection d'un code malveillant dans une mise à jour de l'application, détectée par le module antivirus Android Play Protect.

Un composant non autorisé, une bibliothèque native nommée `libalphasdk.so`, a été trouvé dans la version compromises (30.51). Cette librairie s'exécute en arrière-plan, collecte des informations sur l'appareil, les enregistre auprès d'un serveur distant et communique via un canal crypté, sans aucune indication visible pour l'utilisateur. Bien qu'aucune activité malveillante concrète comme le vol de compte n'ait été prouvée, le potentiel de telles actions est élevé.

Le développeur a révoqué l'ancienne signature et travaille à publier une nouvelle version avec un identifiant d'application distinct. Cependant, la communauté déplore un manque de transparence concernant l'incident et les versions sûres.

**Points Clés :**

*   Compromission des clés de signature du développeur de SmartTube.
*   Distribution d'une mise à jour malveillante contenant une librairie inconnue (`libalphasdk.so`).
*   La librairie collecte des informations sur l'appareil et communique avec un serveur distant.
*   Le risque d'activités malveillantes futures est élevé.
*   Le développeur prévoit une nouvelle version sécurisée, mais la confiance est ébranlée.

**Vulnérabilités :**

*   **CVE :** Aucune CVE spécifique n'est mentionnée dans l'article pour cet incident. La vulnérabilité principale réside dans la compromission des clés de signature du développeur, permettant la distribution d'un logiciel malveillant signé légitimement.

**Recommandations :**

*   **Pour les utilisateurs :**
    *   Restez sur des versions antérieures connues pour être sûres (la version 30.19 semble ne pas être détectée comme dangereuse par Play Protect).
    *   Désactivez les mises à jour automatiques de l'application.
    *   Évitez de vous connecter avec des comptes premium ou d'enregistrer des informations sensibles.
    *   Réinitialisez les mots de passe de votre compte Google.
    *   Vérifiez votre console de compte pour toute activité suspecte et supprimez les services inconnus.
    *   Attendez la publication transparente et détaillée du développeur sur l'incident avant de revenir à des versions récentes.
*   **Pour le développeur (implicite) :**
    *   Mettre en place des mesures de sécurité robustes pour la protection des clés de signature.
    *   Effectuer des audits de sécurité réguliers.
    *   Fournir une communication transparente et détaillée suite à un incident de sécurité.
    *   Publier les versions sécurisées sur les dépôts officiels.

---
[Source](https://www.bleepingcomputer.com/news/security/smarttube-youtube-app-for-android-tv-breached-to-push-malicious-update/){:target="_blank"}
