---
title: 'JanelaRAT: a financial threat targeting users in Latin America'
date: 2026-04-13
permalink: /posts/2026/04/13/janelarat-a-financial-threat-targeting-users-in-latin-america/
tags:
- veille-cyber
- securelist
---
### JanelaRAT : Une menace financière persistante en Amérique latine

JanelaRAT est un cheval de Troie bancaire évolutif ciblant principalement les utilisateurs au Brésil et au Mexique. Ce malware, dérivé de BX RAT, se spécialise dans le vol d'identifiants financiers et le détournement de sessions bancaires en temps réel.

**Points clés :**
*   **Vecteur d'attaque :** Campagnes d'e-mails de phishing imitant des factures impayées redirigeant vers des archives malveillantes.
*   **Mécanisme d'infection :** Utilisation de fichiers MSI comme droppers pour installer des composants, suivis d'une technique de *DLL sideloading* (chargement de bibliothèque illégitime par un exécutable sain) pour exécuter la charge utile finale.
*   **Persistance :** Installation de raccourcis dans le dossier de démarrage de Windows ou via des scripts de commande.
*   **Fonctionnalités malveillantes :** Surveillance active des fenêtres du navigateur, capture d'écran, enregistrement des frappes clavier (*keylogging*), injection de saisie et affichage d'overlays (fenêtres superposées) trompeurs imitant des mises à jour Windows ou des interfaces bancaires pour capturer des codes MFA ou des identifiants.
*   **Évasion :** Utilisation d'obfuscateurs (.NET/Eazfuscator), rotation quotidienne des serveurs C2 et détection de logiciels de sécurité bancaire pour adapter son comportement.

**Vulnérabilités exploitées :**
L'article ne mentionne pas de CVE spécifique, car le malware repose sur l'ingénierie sociale, le *DLL sideloading* et des techniques d'obfuscation logicielle plutôt que sur l'exploitation directe de failles logicielles documentées.

**Recommandations :**
*   **Filtrage DNS :** Bloquer les services de DNS dynamiques (DDNS) au niveau du périmètre réseau ou des résolveurs internes pour perturber la communication avec les serveurs C2.
*   **Sensibilisation :** Former les utilisateurs à la méfiance envers les e-mails non sollicités contenant des liens ou des pièces jointes, même lorsqu'ils semblent provenir d'institutions familières.
*   **Surveillance système :** Détecter la présence de fichiers exécutables suspects dans les dossiers de démarrage ou des comportements anormaux liés au *DLL sideloading*.
*   **Protection des points de terminaison :** Maintenir des solutions EDR/antivirus capables d'identifier les comportements suspects (ex: accès répétitif aux processus bancaires, overlays plein écran suspects).

---
[Source](https://securelist.com/janelarat-financial-threat-in-latin-america/119332/){:target="_blank"}
