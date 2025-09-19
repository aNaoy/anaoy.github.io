---
title: 'Fortra warns of max severity flaw in GoAnywhere MFT’s License Servlet'
date: 2025-09-19
permalink: /posts/2025/09/19/fortra-warns-of-max-severity-flaw-in-goanywhere-mfts-license-servlet/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilité critique dans GoAnywhere MFT : Injection de commandes**

Une faille de sécurité d'une gravité maximale a été identifiée dans le composant License Servlet du logiciel GoAnywhere MFT de Fortra. Cette vulnérabilité, référencée CVE-2025-10035, permet des attaques par injection de commandes à distance.

**Points clés :**

*   **Nature de la faille :** Désérialisation de données non fiables.
*   **Méthode d'exploitation :** Attaques à faible complexité, ne nécessitant pas d'interaction utilisateur, par le biais d'une réponse de licence falsifiée.
*   **Conséquences potentielles :** Injection de commandes arbitraires sur le système affecté.
*   **Condition d'exploitabilité :** Les systèmes doivent être accessibles depuis Internet.

**Vulnérabilités :**

*   **CVE-2025-10035** : Permet l'injection de commandes via le License Servlet.

**Recommandations :**

*   **Mise à jour immédiate :** Appliquer les correctifs disponibles dans les versions GoAnywhere MFT 7.8.4 et Sustain Release 7.6.3.
*   **Restriction d'accès :** Pour les utilisateurs ne pouvant pas mettre à jour immédiatement, il est impératif de sécuriser les systèmes en s'assurant que la console d'administration (Admin Console) de GoAnywhere n'est pas accessible publiquement depuis Internet.
*   **Surveillance :** Les organisations utilisant GoAnywhere MFT devraient surveiller attentivement leurs instances, étant donné que ce type de logiciel est une cible privilégiée pour les acteurs malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/fortra-warns-of-max-severity-flaw-in-goanywhere-mfts-license-servlet/){:target="_blank"}
