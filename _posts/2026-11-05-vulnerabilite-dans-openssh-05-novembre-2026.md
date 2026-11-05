---
title: 'Vulnérabilité dans OpenSSH (05 novembre 2026)'
date: 2026-11-05
permalink: /posts/2026/11/05/vulnerabilite-dans-openssh-05-novembre-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilité critique de contournement d'authentification dans OpenSSH

**Points clés**
*   **Risque :** Contournement de la politique de sécurité permettant une authentification non autorisée sur le service SSH.
*   **Conditions d'exploitation :** La vulnérabilité concerne exclusivement les systèmes Linux utilisant la bibliothèque standard `musl` et configurés sans support PAM (ou avec PAM désactivé). L'attaque est triviale à réaliser en utilisant deux mots de passe, le second devant mesurer entre 257 et 1024 caractères.
*   **Systèmes affectés :** Toutes les versions d'OpenSSH antérieures à la version 10.6p2.

**Vulnérabilités**
*   Le bulletin ne mentionne pas de CVE spécifique, mais identifie un défaut critique dans la gestion de l'authentification sous `musl` (voir bulletin OpenSSH release-10.6p2).

**Recommandations**
*   **Mise à jour :** Installer immédiatement la version 10.6p2 ou supérieure d'OpenSSH.
*   **Mesures palliatives :** En cas d'impossibilité de mise à jour, désactiver l'authentification par mot de passe ou suspendre le service SSH.
*   **Audit de sécurité :** Vérifier les journaux système (`/var/log/messages`) pour détecter toute tentative de connexion suspecte sur les comptes système dont le mot de passe est désactivé (indiqués par une étoile dans `/etc/shadow`).

---
[Source](https://www.cert.cyber.gouv.fr/alerte/CERTFR-2026-ALE-015/){:target="_blank"}
