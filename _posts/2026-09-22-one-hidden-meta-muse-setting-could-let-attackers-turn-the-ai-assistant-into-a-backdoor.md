---
title: 'One Hidden Meta Muse Setting Could Let Attackers Turn the AI Assistant Into a Backdoor'
date: 2026-09-22
permalink: /posts/2026/09/22/one-hidden-meta-muse-setting-could-let-attackers-turn-the-ai-assistant-into-a-backdoor/
tags:
- veille-cyber
- hackernews
---
### Risque de détournement de l'assistant IA Meta Muse sur macOS

Le chercheur en sécurité Patrick Wardle a mis en évidence une vulnérabilité critique dans l'application Mac de l'assistant IA « Muse » de Meta. En exploitant un réglage caché, un logiciel malveillant déjà présent sur la machine peut intercepter les commandes vocales de l'utilisateur et détourner les privilèges étendus de l'assistant.

**Points clés :**
* **Détournement de flux :** Une préférence non documentée, `endo_voyager_dictation_endpoint`, permet de rediriger les données de dictée vers un serveur contrôlé par un attaquant au lieu des serveurs de Meta.
* **Escalade de privilèges :** L'attaquant peut subtiliser le jeton d'authentification (token) de l'utilisateur. Ce jeton permet ensuite de contrôler l'assistant sur tous les appareils synchronisés, incluant l'accès à l'historique des discussions, la géolocalisation ou les commandes domotiques.
* **Discrétion :** Comme les commandes malveillantes proviennent d'une application signée (Muse), les solutions de sécurité traditionnelles peuvent ne pas détecter l'activité suspecte.
* **Vecteur d'attaque :** Bien que l'attaquant doive déjà disposer d'un accès initial (via un malware ou une technique de type « ClickFix »), il n'a besoin d'aucune autorisation supplémentaire pour modifier le réglage de Muse.

**Vulnérabilités :**
* Il n'existe pas de CVE officielle attribuée à cette date. La vulnérabilité réside dans la conception de l'application Muse sur macOS, qui privilégie un système de dictée propriétaire au détriment de l'implémentation sécurisée d'Apple.

**Recommandations :**
* **Désinstallation ou suspension :** Fermer ou supprimer l'application Muse jusqu'à confirmation d'une correction robuste par Meta.
* **Gestion des permissions :** Réduire au strict minimum les accès accordés à l'application si celle-ci est maintenue.
* **Précautions d'usage :** Éviter d'utiliser la fonction de dictée vocale de Muse pour fermer le vecteur d'attaque.
* **Hygiène informatique :** Ne jamais exécuter de commandes dans le Terminal suggérées par des sources non fiables (prévention contre les attaques de type « ClickFix »).
* **Réinitialisation :** En cas de doute sur la compromission du système, révoquer les accès et modifier les mots de passe des comptes liés à Muse.

---
[Source](https://thehackernews.com/2026/09/one-hidden-meta-muse-setting-could-let.html){:target="_blank"}
