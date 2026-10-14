---
title: 'Vulnérabilité dans Ivanti Connect Secure (ICS) (14 octobre 2026)'
date: 2026-10-14
permalink: /posts/2026/10/14/vulnerabilite-dans-ivanti-connect-secure-ics-14-octobre-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilité critique activement exploitée dans Ivanti Connect Secure

Une vulnérabilité critique affectant Ivanti Connect Secure (ICS) permet à un attaquant distant d'exécuter du code arbitraire, d'élever ses privilèges et de contourner les politiques de sécurité. Cette faille fait actuellement l'objet d'une exploitation active.

**Vulnérabilité identifiée :**
*   **CVE-2026-104935**

**Systèmes affectés :**
*   Version 22.8Rx antérieures à la 22.8R2.5
*   Version 25.1.1.x antérieures à la 25.1.1.2
*   Version 25.1.3.x antérieures à la 25.1.3.1

**Points clés :**
*   La vulnérabilité permet une prise de contrôle totale de l'équipement par un attaquant.
*   Des preuves d'exploitation active sont confirmées.
*   Un risque de latéralisation au sein du réseau est avéré, notamment via l'utilisation détournée de secrets (LDAP, AD) stockés sur l'équipement.

**Recommandations immédiates :**
*   **Isolation :** Déconnecter immédiatement l'équipement concerné des réseaux internes et d'Internet.
*   **Investigations :** Réaliser des instantanés (mémoire et système) avant toute extinction pour préserver les traces, puis utiliser l'outil *Integrity Check Tool* (ICT) fourni par Ivanti pour détecter une compromission.
*   **Gestion post-compromission :** En cas de preuve d'intrusion, procéder à un retour aux réglages d'usine (*Factory Reset*), mettre à jour le micrologiciel, et révoquer l'ensemble des secrets (mots de passe, clés API, certificats TLS/authentification) ayant transité par la passerelle.
*   **Prévention :** Si aucune compromission n'est détectée, installer les correctifs de mise à jour dès que possible et surveiller étroitement les comptes de service associés (LDAP/AD).

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2026-ALE-013/){:target="_blank"}
