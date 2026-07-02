---
title: 'FortiBleed Credential Theft Linked to INC and Lynx Ransomware Operations'
date: 2026-07-02
permalink: /posts/2026/07/02/fortibleed-credential-theft-linked-to-inc-and-lynx-ransomware-operations/
tags:
- veille-cyber
- hackernews
---
### Campagne FortiBleed : Espionnage et Ransomwares à grande échelle

La campagne **FortiBleed** est une opération de cybercriminalité organisée visant les équipements FortiGate, impliquant le vol massif d'identifiants pour faciliter des déploiements de ransomwares (notamment INC et Lynx). L'infrastructure des attaquants, découverte suite à une erreur de sécurité opérationnelle, révèle une organisation structurée composée d'environ 20 personnes ciblant principalement les secteurs de l'industrie, de la technologie et de la logistique.

**Points clés :**
*   **Vol massif :** Environ 430 000 pare-feu FortiGate visés et plus de 110 millions d'identifiants compromis.
*   **Mode opératoire :** Balayage Internet pour identifier des cibles, accès administratif via des combinaisons d'identifiants connues, et déploiement de sniffeurs de paquets personnalisés en Golang pour intercepter le trafic réseau.
*   **Réseau criminel :** L'infrastructure sert d'intermédiaire d'accès initial (IAB) pour des groupes de ransomware. Des preuves indiquent une extension prochaine des activités vers les environnements Citrix.
*   **Zero-day :** Les attaquants disposeraient d'une vulnérabilité « zero-day » non divulguée affectant Nextcloud.

**Vulnérabilités mentionnées :**
*   **CVE-2026-35616 :** Faille critique (score CVSS 9.1) dans Fortinet FortiClient EMS, exploitée par le logiciel malveillant « EKZ Stealer » pour dérober des identifiants de navigateurs.

**Recommandations :**
*   **Renforcement de l'authentification :** Imposer l'authentification multifacteur (MFA) sur tous les accès distants et équipements exposés.
*   **Gestion des accès :** Procéder à une rotation systématique des identifiants et mots de passe pour les comptes ayant potentiellement été exposés.
*   **Surveillance proactive :** Analyser les logs d'authentification à la recherche d'activités anormales, particulièrement sur les infrastructures Fortinet et Citrix.
*   **Veille de sécurité :** Appliquer les correctifs de sécurité dès leur publication, notamment concernant la faille CVE-2026-35616 pour les utilisateurs de FortiClient EMS.

---
[Source](https://thehackernews.com/2026/07/fortibleed-credential-theft-linked-to.html){:target="_blank"}
