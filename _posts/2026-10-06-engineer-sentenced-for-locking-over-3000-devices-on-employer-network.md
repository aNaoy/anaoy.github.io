---
title: 'Engineer sentenced for locking over 3,000 devices on employer network'
date: 2026-10-06
permalink: /posts/2026/10/06/engineer-sentenced-for-locking-over-3000-devices-on-employer-network/
tags:
- veille-cyber
- bleepingcomp
---
### Sabotage interne : Un ingénieur condamné pour extorsion

Un ingénieur en infrastructures a été condamné à 32 mois de prison pour avoir orchestré une attaque par rançongiciel contre son propre employeur. Utilisant ses accès administrateur, il a compromis plus de 3 000 appareils en modifiant les mots de passe de comptes critiques, en supprimant des comptes d'administration de domaine et en planifiant des arrêts système distants, avant de réclamer une rançon de 20 bitcoins.

**Points clés :**
*   **Méthodologie :** L'attaquant a exploité des comptes administrateur légitimes pour automatiser des tâches de blocage (via le planificateur de tâches Windows).
*   **Impact :** Verrouillage de 3 284 postes de travail et 254 serveurs, suppression de comptes administratifs et tentative de destruction des sauvegardes.
*   **Motivation :** Extorsion financière par le biais d'un rançongiciel menaçant d'intensifier le sabotage du réseau.

**Vulnérabilités exploitées :**
*   **Abus de privilèges (Insider Threat) :** Utilisation légitime de comptes à hauts privilèges pour des actions malveillantes.
*   **Absence de cloisonnement :** Une confiance excessive accordée à un compte administrateur unique a permis une paralysie généralisée du domaine.
*   **Absence de détection immédiate :** L'attaquant a pu manipuler les journaux système (*Windows logs*) pour dissimuler ses recherches et ses actions préalables.
*   *Note : Aucune CVE spécifique n'est associée, car il s'agit d'un détournement de fonctionnalités natives (Living off the Land).*

**Recommandations :**
*   **Principe du moindre privilège :** Restreindre strictement les accès d'administration et éviter que les comptes d'ingénieurs ne disposent de droits globaux non supervisés.
*   **Authentification et supervision :** Implémenter une authentification multi-facteurs (MFA) pour toute modification critique sur le domaine et instaurer une validation à deux personnes (*Dual Control*) pour les opérations sensibles.
*   **Gestion des logs :** Centraliser les journaux d'événements vers un serveur SIEM externe, inviolable par les administrateurs locaux, pour garantir la traçabilité.
*   **Stratégie de sauvegarde :** Maintenir des sauvegardes immuables et isolées du réseau (hors ligne ou via des solutions WORM) pour prévenir toute suppression malveillante par un administrateur compromis.

---
[Source](https://www.bleepingcomputer.com/news/security/engineer-sentenced-for-locking-thousands-of-devices-on-employer-network/){:target="_blank"}
