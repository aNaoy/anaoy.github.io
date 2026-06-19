---
title: 'CISA warns Fortinet users to secure devices after FortiBleed leak'
date: 2026-06-19
permalink: /posts/2026/06/19/cisa-warns-fortinet-users-to-secure-devices-after-fortibleed-leak/
tags:
- veille-cyber
- bleepingcomp
---
### FortiBleed : Fuite massive d'identifiants Fortinet

La CISA a émis une alerte urgente suite à la découverte de « FortiBleed », une fuite de données exposant les identifiants (noms d'utilisateurs, adresses e-mail et mots de passe en clair) de près de 74 000 équipements Fortinet (pare-feux et passerelles VPN) à travers le monde. Cette base de données, attribuée à un groupe russophone, cible des organisations privées, gouvernementales et des infrastructures critiques.

**Points clés :**
*   **Ampleur :** 73 932 appareils touchés dans 194 pays, incluant des entreprises majeures (Samsung, Toyota, etc.).
*   **Origine :** Les données proviendraient de fichiers de configuration Fortinet, potentiellement collectés via plus d'un milliard de tentatives d'authentification.
*   **Risque :** Les attaquants exploitent ces accès pour s'introduire dans les réseaux, compromettre des sessions VPN et effectuer des mouvements latéraux.
*   **Contexte vulnérabilités :** La CISA répertorie actuellement 26 vulnérabilités Fortinet exploitées « dans la nature » (Known Exploited Vulnerabilities), dont plusieurs liées à FortiSandbox.

**Vulnérabilités :**
Bien que la fuite soit liée à des identifiants compromis, l'article souligne une exploitation active de failles critiques dans **FortiSandbox**. Il est conseillé de consulter régulièrement le catalogue [CISA KEV](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) pour suivre les 26 vulnérabilités Fortinet connues et activement exploitées.

**Recommandations de sécurité :**
*   **Réinitialisation immédiate :** Changer tous les mots de passe des sessions VPN et des comptes administratifs.
*   **Gestion des sessions :** Terminer toutes les sessions SSL VPN et administratives actives.
*   **Authentification :** Activer une authentification multifacteur (MFA) résistante au phishing.
*   **Durcissement :** Restreindre l'accès aux interfaces de gestion via le réseau public et supprimer les comptes non autorisés.
*   **Algorithmes :** Stocker les identifiants d'administration en utilisant le standard PBKDF2.
*   **Audit :** Examiner les logs pour détecter toute activité suspecte ou mouvement latéral.
*   **Vérification :** Utiliser des outils de recherche dédiés (comme celui fourni par *Hudson Rock*) pour vérifier si une organisation est présente dans le dataset compromis.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-warns-fortinet-users-to-secure-devices-after-fortibleed-leak/){:target="_blank"}
