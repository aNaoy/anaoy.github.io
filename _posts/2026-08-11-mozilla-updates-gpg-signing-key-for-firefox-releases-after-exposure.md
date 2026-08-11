---
title: 'Mozilla updates GPG signing key for Firefox releases after exposure'
date: 2026-08-11
permalink: /posts/2026/08/11/mozilla-updates-gpg-signing-key-for-firefox-releases-after-exposure/
tags:
- veille-cyber
- bleepingcomp
---
### Remplacement de la clé GPG de Mozilla suite à une exposition accidentelle

Mozilla a procédé au remplacement de sa clé de signature GPG utilisée pour les versions Linux (tarballs, paquets RPM) de Firefox et Thunderbird, après la découverte d'une copie non chiffrée de cette clé dans un dépôt GitHub privé. Bien qu'aucune preuve d'exploitation malveillante n'ait été détectée, cette mesure de précaution vise à sécuriser la chaîne d'approvisionnement logicielle.

**Points clés :**
*   **Incident :** Exposition accidentelle d'une sous-clé de signature GPG sur GitHub.
*   **Impact limité :** L'accès au dépôt était restreint à un groupe restreint de collaborateurs autorisés, et aucun accès non autorisé n'a été identifié via les logs d'audit.
*   **Action corrective :** Révocation de l'ancienne clé et déploiement d'une nouvelle sous-clé (valide jusqu'en août 2028).

**Vulnérabilités :**
*   Aucune CVE n'est associée à cet incident, car il s'agit d'une erreur de gestion de configuration (fuite de secret dans un dépôt de code) plutôt qu'une faille logicielle.

**Recommandations :**
*   **Utilisateurs effectuant des vérifications manuelles :** Importer la nouvelle clé publique et la révocation de l'ancienne via les serveurs de clés (keys.openpgp.org).
*   **Utilisateurs Linux (paquets RPM) :** Suivre les instructions spécifiques fournies par Mozilla pour Fedora, RHEL/Rocky/AlmaLinux ou openSUSE afin de maintenir la validité des signatures et la réception des mises à jour.

---
[Source](https://www.bleepingcomputer.com/news/security/mozilla-updates-gpg-key-for-signing-firefox-thunderbird-releases-after-exposure/){:target="_blank"}
