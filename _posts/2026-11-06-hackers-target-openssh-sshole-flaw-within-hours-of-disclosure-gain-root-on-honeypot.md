---
title: 'Hackers Target OpenSSH SSHole Flaw Within Hours of Disclosure, Gain Root on Honeypot'
date: 2026-11-06
permalink: /posts/2026/11/06/hackers-target-openssh-sshole-flaw-within-hours-of-disclosure-gain-root-on-honeypot/
tags:
- veille-cyber
- hackernews
---
### Exploitation active de la faille "SSHole" dans OpenSSH

Des attaquants exploitent activement une vulnérabilité critique dans OpenSSH, baptisée **SSHole**, permettant un contournement de l'authentification sur des systèmes spécifiques.

**Points clés :**
*   La vulnérabilité permet à un attaquant non authentifié d'accéder à des comptes dépourvus de mot de passe (marqués par un astérisque dans le fichier système) en envoyant un mot de passe de taille excessive (entre 257 et 1 024 octets).
*   L'erreur provient d'une mauvaise gestion de l'échec de hachage, interprété par erreur comme une authentification réussie.
*   Les attaques ont été observées moins de neuf heures après la divulgation publique, incluant des accès root sur des serveurs honeypot.
*   La faille concerne principalement les systèmes utilisant **musl C** avec **PAM désactivé** (notamment Alpine Linux). Les systèmes utilisant `glibc` ou PAM ne sont pas affectés.

**Vulnérabilité :**
*   **CVE-2026-123158** (Score CVSS : 8.1)

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer la version **OpenSSH 10.6p2** ou la mise à jour fournie par votre distribution Linux.
*   **Redémarrage :** Redémarrer le service `sshd` après installation du correctif.
*   **Audit de sécurité :** Inspecter les journaux système (`/var/log/messages`) à la recherche de lignes indiquant "Accepted password for" concernant des comptes qui ne devraient pas autoriser l'authentification par mot de passe.
*   **Investigation post-compromission :** Vérifier l'utilisation de `doas`, les nouveaux utilisateurs créés, les fichiers suspects et les clés SSH autorisées sur les machines potentiellement exposées.

---
[Source](https://thehackernews.com/2026/11/hackers-exploited-openssh-sshole-flaw.html){:target="_blank"}
