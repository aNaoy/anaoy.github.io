---
title: '101 Malicious npm Packages Add Developers WhatsApp Accounts to Groups Without Consent'
date: 2026-09-29
permalink: /posts/2026/09/29/101-malicious-npm-packages-add-developers-whatsapp-accounts-to-groups-without-consent/
tags:
- veille-cyber
- hackernews
---
### Campagne PhantomSub : 101 paquets npm malveillants détournent WhatsApp

Une campagne baptisée « PhantomSub » a été identifiée, impliquant 101 paquets npm malveillants téléchargés près de 490 000 fois. Ces paquets détournent le projet open source « Baileys » pour inscrire automatiquement les comptes WhatsApp des développeurs à des groupes et chaînes de spam, sans leur consentement.

**Points clés :**
* **Objectif :** Utiliser les comptes des développeurs comme « preuve sociale » pour gonfler artificiellement le nombre d'abonnés de chaînes vendant des scripts, des applications piratées et des services de boost pour réseaux sociaux.
* **Origine :** Une grande partie des canaux identifiés est basée en Indonésie.
* **Méthodologies :** Les chercheurs ont identifié trois variantes de fonctionnement :
    * Récupération dynamique des identifiants de canaux via GitHub.
    * Intégration des identifiants en clair dans le code source.
    * Utilisation d'identifiants obfusqués et encodés dans le code.

**Vulnérabilités :**
* Il n'existe pas de CVE spécifique pour cette campagne, car il s'agit d'un abus de fonctionnalités légitimes (utilisation malveillante de bibliothèques tierces). La faille réside dans l'utilisation de paquets npm non vérifiés qui exploitent les sessions WhatsApp authentifiées pour exécuter des actions non autorisées.

**Recommandations :**
* **Audit :** Vérifiez si vos comptes WhatsApp ont été ajoutés à des groupes suspects et quittez-les immédiatement.
* **Vigilance logicielle :** Évitez d'installer des paquets npm douteux ou des forks non officiels du projet Baileys.
* **Sécurité :** Ne connectez pas de compte WhatsApp personnel ou sensible à des scripts ou des outils de développement tiers dont la source n'est pas fiable.
* **Détection :** Mettez en place des règles de blocage pour les paquets identifiés dans votre environnement de développement.

---
[Source](https://thehackernews.com/2026/09/101-malicious-npm-packages-add.html){:target="_blank"}
