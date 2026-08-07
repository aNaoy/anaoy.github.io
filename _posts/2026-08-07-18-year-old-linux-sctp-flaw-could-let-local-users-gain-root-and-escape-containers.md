---
title: '18-Year-Old Linux SCTP Flaw Could Let Local Users Gain Root and Escape Containers'
date: 2026-08-07
permalink: /posts/2026/08/07/18-year-old-linux-sctp-flaw-could-let-local-users-gain-root-and-escape-containers/
tags:
- veille-cyber
- hackernews
---
### SCTPhantom : Une faille critique vieille de 18 ans dans le protocole SCTP de Linux

Une vulnérabilité de type « use-after-free » présente dans le code réseau SCTP du noyau Linux depuis 2008 permet à un utilisateur local d'obtenir des privilèges root ou de s'échapper d'un conteneur vers la machine hôte. Identifiée sous le nom **SCTPhantom**, cette faille affecte une large gamme de distributions Linux.

**Points clés :**
* **Origine :** La faille existe depuis le noyau Linux 2.6.25 (2008).
* **Mécanisme :** Une erreur de gestion lors de la reconfiguration dynamique des adresses IP dans le protocole SCTP entraîne l'utilisation d'un pointeur mémoire déjà libéré.
* **Impact :** Bien qu'il s'agisse d'une attaque locale, elle peut permettre une escalade de privilèges (root) et une évasion de conteneur, même sans privilèges administratifs particuliers (`CAP_NET_ADMIN` ou `CAP_SYS_ADMIN`), selon les tests de Tencent.
* **Complexité :** L'exploitation nécessite que le protocole SCTP soit accessible sur la cible.

**Vulnérabilité :**
* **CVE-2026-64564** : Faille de corruption mémoire (use-after-free) dans l'implémentation SCTP du noyau Linux.

**Recommandations :**
* **Mise à jour immédiate :** Appliquer les correctifs du noyau fournis par les distributions. Les versions stables intégrant le correctif incluent 7.1.6, 6.18.42, 6.12.101 et 6.6.148.
* **Vérification :** Ne pas se fier uniquement au numéro de version du noyau, car les éditeurs effectuent souvent des rétroportages (backports). Consulter le gestionnaire de mises à jour de sa distribution spécifique.
* **Réduction de la surface d'attaque :** Si le protocole SCTP n'est pas nécessaire, désactiver le module noyau correspondant pour éliminer tout risque lié à cette faille.

---
[Source](https://thehackernews.com/2026/08/18-year-old-linux-sctp-flaw-could-let.html){:target="_blank"}
