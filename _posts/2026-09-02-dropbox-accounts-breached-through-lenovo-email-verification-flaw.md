---
title: 'Dropbox accounts breached through Lenovo email verification flaw'
date: 2026-09-02
permalink: /posts/2026/09/02/dropbox-accounts-breached-through-lenovo-email-verification-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de comptes Dropbox via une faille d'authentification Lenovo

Une faille dans le processus de vérification d'e-mail de Lenovo a permis à des attaquants de compromettre environ 5 000 comptes Dropbox. Bien que les victimes n'aient pas toujours possédé de compte Lenovo, l'intégration entre les deux services (SSO) a été exploitée pour contourner les protections d'accès classiques.

**Points clés :**
*   **Mécanisme d'attaque :** Les attaquants ont créé des identifiants Lenovo frauduleux en utilisant les adresses e-mail de leurs victimes.
*   **Faille logique :** Le système d'authentification unique (SSO) de Dropbox faisait confiance à la validation de Lenovo sans exiger de confirmation supplémentaire de l'utilisateur, permettant un accès direct sans mot de passe Dropbox.
*   **Période d'impact :** Les accès non autorisés ont eu lieu entre le 4 et le 21 août.
*   **Conséquences :** Environ 5 000 comptes ont été consultés, avec des cas avérés de téléchargement de données.

**Vulnérabilités :**
*   Aucune CVE n'a été attribuée à ce jour, la faille reposant sur une erreur de conception dans l'intégration legacy entre les services d'identité de Lenovo et l'infrastructure d'authentification de Dropbox.

**Recommandations :**
*   **Actions entreprises :** Dropbox a invalidé toutes les sessions authentifiées via Lenovo ID et impose désormais la saisie du mot de passe Dropbox même lors de l'utilisation du SSO Lenovo.
*   **Conseils aux utilisateurs :** Il est fortement recommandé d'activer l'authentification à deux facteurs (2FA) sur tous les comptes sensibles et de surveiller l'historique des connexions. En cas de doute, la réinitialisation du mot de passe reste la procédure de sécurité standard la plus efficace.

---
[Source](https://www.bleepingcomputer.com/news/security/dropbox-accounts-breached-through-lenovo-email-verification-flaw/){:target="_blank"}
