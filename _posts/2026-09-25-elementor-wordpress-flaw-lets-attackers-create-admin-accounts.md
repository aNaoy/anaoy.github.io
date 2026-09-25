---
title: 'Elementor WordPress flaw lets attackers create admin accounts'
date: 2026-09-25
permalink: /posts/2026/09/25/elementor-wordpress-flaw-lets-attackers-create-admin-accounts/
tags:
- veille-cyber
- bleepingcomp
---
# Faille critique dans le plugin Elementor : création non autorisée de comptes administrateur

Une vulnérabilité de type Cross-Site Request Forgery (CSRF) a été identifiée dans le plugin Elementor pour WordPress (versions 4.3.0 et 4.3.1), exposant potentiellement jusqu'à 2 millions de sites web.

### Points clés
* **Mécanisme d'attaque :** Un attaquant peut tromper un administrateur connecté en l'incitant à cliquer sur un lien piégé. Cela déclenche une requête API REST malveillante exécutée avec les privilèges de l'administrateur.
* **Conséquences :** L'attaque permet la création automatique d'un compte administrateur sous le contrôle de l'attaquant.
* **Origine technique :** Une mauvaise validation du chemin URI dans le module "Editor Events" contourne le contrôle de sécurité standard (nonce) de l'API REST de WordPress.
* **Simplicité :** L'attaque ne nécessite aucun script complexe ni page web dédiée ; un simple lien envoyé par e-mail ou messagerie suffit.

### Vulnérabilités
* **Type :** CSRF (Cross-Site Request Forgery).
* **Identifiant CVE :** Non attribué (le correctif a été publié rapidement suite à un signalement).
* **Versions impactées :** 4.3.0 et 4.3.1.

### Recommandations
* **Mise à jour immédiate :** Tous les utilisateurs doivent mettre à jour le plugin Elementor vers la version **4.3.2 ou supérieure**, qui corrige la faille en bloquant le contournement via les chaînes de requête (query string).
* **Vigilance :** Bien que ce correctif règle ce problème précis, il est conseillé de maintenir l'ensemble des extensions WordPress à jour pour se prémunir d'autres vulnérabilités connues.

---
[Source](https://www.bleepingcomputer.com/news/security/elementor-wordpress-flaw-lets-attackers-create-admin-accounts/){:target="_blank"}
