---
title: 'BlackX UEFI Bootkit Bypasses Secure Boot on Patched Windows Systems Missing Revocations'
date: 2026-10-23
permalink: /posts/2026/10/23/blackx-uefi-bootkit-bypasses-secure-boot-on-patched-windows-systems-missing-revocations/
tags:
- veille-cyber
- hackernews
---
### Menace persistante : Le bootkit UEFI BlackX cible les institutions diplomatiques

Le groupe APT41, lié à la Chine, déploie le bootkit UEFI **BlackX** pour cibler des entités diplomatiques en Asie centrale. Ce malware est une évolution sophistiquée de *BlackLotus*, utilisée pour contourner les défenses de démarrage de Windows et neutraliser les logiciels de sécurité, assurant ainsi une persistance à long terme sur les systèmes compromis.

**Points clés :**
*   **Objectif :** Espionnage cybernétique via des chevaux de Troie d'accès à distance (RAT) utilisant des services cloud légitimes (Google Drive, OneDrive) pour le contrôle et la commande (C2).
*   **Propagation :** Le bootkit n'est pas un vecteur d'accès initial. Il est installé après une compromission réussie, nécessitant des privilèges administrateur ou un accès physique.
*   **Technique :** Utilisation de la technique "BYOVD" (Bring Your Own Vulnerable Driver) avec des pilotes signés pour corrompre le noyau Windows et désactiver les solutions EDR/antivirus.
*   **Origine :** Le code semble être une réingénierie du bootkit *BlackLotus*, illustrant une collaboration ou un partage de ressources inhabituel entre acteurs étatiques et cybercriminels.

**Vulnérabilités exploitées :**
*   **CVE-2022-21894 (Baton Drop) :** Vulnérabilité de contournement du *Secure Boot* permettant de charger du code malveillant avant le démarrage du système d'exploitation.
*   **CVE-2023-24932 :** Vulnérabilité connexe de contournement du *Secure Boot* potentiellement utilisée par certaines variantes.

**Recommandations :**
*   **Appliquer les révocations manuelles :** L'installation des correctifs Windows ne suffit pas. Il est impératif d'ajouter manuellement le certificat « Windows Production PCA 2011 » à la liste noire (DBX) du *Secure Boot* dans l'UEFI pour bloquer les binaires vulnérables.
*   **Sécurisation des accès :** Restreindre strictement les privilèges administrateur et surveiller les comportements suspects liés au chargement de pilotes non signés ou au *DLL sideloading* (notamment via `googleupdate.exe`).
*   **Surveillance réseau :** Détecter les communications sortantes vers des services de stockage cloud non autorisés et surveiller les journaux d'exécution pour des commandes de type `inst.exe`.

---
[Source](https://thehackernews.com/2026/10/blackx-uefi-bootkit-bypasses-secure.html){:target="_blank"}
