---
title: 'Mozilla Revokes Firefox and Thunderbird Linux Signing Key After Key Lands in Private Repo'
date: 2026-08-11
permalink: /posts/2026/08/11/mozilla-revokes-firefox-and-thunderbird-linux-signing-key-after-key-lands-in-private-repo/
tags:
- veille-cyber
- hackernews
---
### Révocation de la clé de signature Linux de Mozilla suite à une exposition accidentelle

Mozilla a révoqué la sous-clé de signature GPG utilisée pour valider les téléchargements de Firefox et Thunderbird sur Linux. Cette décision fait suite à l'insertion accidentelle d'une copie non chiffrée de la clé dans l'un des dépôts de code privé de l'entreprise. Bien qu'aucune preuve d'accès non autorisé n'ait été détectée, Mozilla a classé cette révocation sous le code « clé compromise » par mesure de précaution.

**Points clés :**
* **Nature de l'incident :** Exposition involontaire de matériel cryptographique (sous-clé) dans un dépôt privé.
* **Impact :** La révocation invalide les signatures des téléchargements passés et actuels, rendant nécessaire une mise à jour manuelle pour les utilisateurs vérifiant les signatures ou utilisant les paquets RPM.
* **Statu quo :** La clé primaire reste valide, seule la sous-clé de signature est remplacée.
* **Note :** Les utilisateurs de paquets `.deb` (Debian/Ubuntu) ne sont pas concernés par cette modification.

**Vulnérabilités :**
* Pas de CVE associée. Le problème relève d'une erreur de gestion de secrets (exposition de clé privée) au sein du cycle de développement.

**Recommandations :**
* **Pour les utilisateurs vérifiant les signatures manuellement :** Importer la nouvelle sous-clé (empreinte : `827E 6586 0867 9618 CD34 9F93 678E 455D 7676 7AA3`) et le certificat de révocation de l'ancienne clé.
* **Pour les utilisateurs de paquets RPM (Fedora, openSUSE, etc.) :** Si une erreur de mise à jour survient, il est nécessaire de supprimer l'ancienne clé et d'importer la nouvelle via les commandes suivantes :
    1. `sudo rpm -e --allmatches gpg-pubkey-14f26682d0916cdd81e37b6d61b7b526d98f0353`
    2. `sudo rpm --import https://packages.mozilla.org/rpm/firefox/signing-key.gpg`
    3. `sudo dnf clean all` (ou `zypper refresh` pour openSUSE).

---
[Source](https://thehackernews.com/2026/08/mozilla-revokes-firefox-and-thunderbird.html){:target="_blank"}
