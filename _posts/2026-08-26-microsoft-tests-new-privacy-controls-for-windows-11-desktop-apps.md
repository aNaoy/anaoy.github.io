---
title: 'Microsoft tests new privacy controls for Windows 11 desktop apps'
date: 2026-08-26
permalink: /posts/2026/08/26/microsoft-tests-new-privacy-controls-for-windows-11-desktop-apps/
tags:
- veille-cyber
- bleepingcomp
---
### Renforcement du contrôle de la confidentialité sur Windows 11

Microsoft teste actuellement, dans la version *Insider Preview Build 26340.9233*, une mise à jour permettant une gestion granulaire des autorisations pour les applications de bureau. Contrairement au modèle précédent qui appliquait des paramètres à l'échelle du système, cette évolution autorise les utilisateurs à contrôler individuellement l'accès à la caméra, au microphone et à la géolocalisation pour chaque logiciel.

**Points clés :**
* **Gestion par application :** Introduction d'un contrôle spécifique permettant d'accorder ou de révoquer les accès sensibles application par application.
* **Transparence accrue :** Cette mesure s'inscrit dans les initiatives « Windows Baseline Security Mode » visant à offrir une expérience similaire aux permissions mobiles (demandes de consentement explicite).
* **Motivations :** Lutter contre les applications malveillantes qui modifient les paramètres système ou accèdent à des données privées sans autorisation préalable.

**Vulnérabilités :**
* Aucune CVE n'est associée à cette annonce, car il s'agit d'une évolution de fonctionnalité et non de la correction d'une faille spécifique.
* Risque résiduel : Microsoft souligne que certaines applications utilisant des composants partagés ou des technologies de navigation pourraient apparaître sous des noms génériques ou comme « non signées », compliquant l'identification de l'éditeur par l'utilisateur.

**Recommandations :**
* **Vigilance utilisateur :** N'accorder l'accès aux ressources sensibles (caméra, micro, localisation) qu'aux applications de confiance et dont l'éditeur est clairement identifié.
* **Audit des permissions :** Utiliser les nouveaux menus dans *Paramètres > Confidentialité et sécurité* pour passer en revue et restreindre les accès aux applications jugées non essentielles.
* **Surveillance des applications non signées :** Faire preuve d'une prudence accrue face aux processus dont l'origine n'est pas vérifiable par Windows.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-tests-new-privacy-controls-for-windows-11-desktop-apps/){:target="_blank"}
