---
title: 'Accenture confirms breach after hacker offers stolen data for sale'
date: 2026-07-08
permalink: /posts/2026/07/08/accenture-confirms-breach-after-hacker-offers-stolen-data-for-sale/
tags:
- veille-cyber
- bleepingcomp
---
### Incident de sécurité chez Accenture : fuite de données confidentielles

Le géant des services informatiques Accenture a confirmé avoir subi une intrusion après qu'un acteur malveillant a mis en vente 35 Go de données internes sur un forum de cybercriminalité. Bien que l'entreprise assure avoir neutralisé la source de l'incident et affirme qu'aucune opération n'est impactée, elle n'a pas précisé la nature exacte des données exfiltrées ni la méthode d'intrusion utilisée.

**Points clés :**
*   **Volume de données :** Environ 35 Go de fichiers dérobés.
*   **Nature des données compromises :** Selon le pirate (alias « 888 »), le vol inclurait du code source, des clés RSA et SSH, des jetons d'accès personnels (PAT) Azure, des clés de stockage Azure et des fichiers de configuration.
*   **Vérification :** Une capture d'écran suggérant le clonage d'un dépôt Azure DevOps a été partagée par l'attaquant, mais l'ampleur réelle de la fuite n'a pas été confirmée par Accenture.
*   **Antécédents :** Il s'agit du troisième incident notable pour Accenture, après une attaque par ransomware LockBit en 2021 et une fuite de données via un tiers en 2024.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, l'incident étant lié à une exposition potentielle de secrets techniques (clés d'accès et jetons) permettant un accès non autorisé aux systèmes Azure DevOps.

**Recommandations :**
*   **Rotation des secrets :** En cas d'exposition de clés SSH, RSA et de jetons d'accès (Azure PAT), une révocation immédiate et une régénération de l'ensemble de ces identifiants sont indispensables.
*   **Audit d'accès :** Renforcer la surveillance des journaux d'accès sur les environnements cloud (Azure DevOps) pour identifier des activités suspectes ou des accès non autorisés.
*   **Gestion des privilèges :** Appliquer le principe du moindre privilège pour limiter les droits associés aux jetons d'accès et aux clés de configuration, afin de restreindre l'impact en cas de compromission future.

---
[Source](https://www.bleepingcomputer.com/news/security/accenture-confirms-breach-after-hacker-offers-stolen-data-for-sale/){:target="_blank"}
