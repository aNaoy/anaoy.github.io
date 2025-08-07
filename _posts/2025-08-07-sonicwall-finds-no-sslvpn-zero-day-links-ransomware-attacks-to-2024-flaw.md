---
title: 'SonicWall finds no SSLVPN zero-day, links ransomware attacks to 2024 flaw'
date: 2025-08-07
permalink: /posts/2025/08/07/sonicwall-finds-no-sslvpn-zero-day-links-ransomware-attacks-to-2024-flaw/
tags:
- veille-cyber
- bleepingcomp
---
**Attaques de Ransomware : La Vulnérabilité CVE-2024-40766 Exploite les Pare-feux SonicWall**

Les récentes attaques de ransomware, attribuées au groupe Akira, ne seraient pas le fait d'une faille inconnue (zero-day) mais plutôt de l'exploitation d'une vulnérabilité précédemment corrigée. SonicWall a identifié la faille CVE-2024-40766 comme étant la cause des intrusions, permettant un accès non autorisé aux systèmes utilisant SSLVPN sur les pare-feux Gen 7.

**Points Clés :**

*   Les attaques exploitent la faille CVE-2024-40766, une faille de contrôle d'accès SSLVPN dans SonicOS.
*   Cette vulnérabilité permet le détournement de sessions ou l'obtention d'un accès VPN non autorisé.
*   La faille avait été divulguée il y a environ un an et était exploitée par des groupes comme Akira et Fog.
*   SonicWall a d'abord laissé entendre qu'il pourrait s'agir d'une zero-day, mais après investigation, il attribue les attaques à une exploitation de la faille connue.
*   Les compromissions seraient liées à des migrations de pare-feux Gen 6 vers Gen 7 où les mots de passe utilisateur locaux n'ont pas été réinitialisés, une étape pourtant recommandée dans l'avis initial.
*   Certains clients rapportent des incidents même sur des comptes inexistants avant la migration, soulevant des doutes sur l'exhaustivité des explications de SonicWall.

**Vulnérabilités :**

*   **CVE-2024-40766** : Faute critique de contrôle d'accès SSLVPN dans SonicOS permettant un accès non autorisé.

**Recommandations :**

*   Mettre à jour le firmware vers la version 7.3.0 ou ultérieure pour bénéficier de protections renforcées contre les attaques par force brute et l'authentification multifacteur (MFA).
*   Réinitialiser tous les mots de passe des utilisateurs locaux, en particulier ceux utilisés pour SSLVPN.
*   Désactiver les services SSLVPN et limiter la connectivité aux adresses IP de confiance jusqu'à la résolution complète du problème.

---
[Source](https://www.bleepingcomputer.com/news/security/sonicwall-finds-no-sslvpn-zero-day-links-ransomware-attacks-to-2024-flaw/){:target="_blank"}
