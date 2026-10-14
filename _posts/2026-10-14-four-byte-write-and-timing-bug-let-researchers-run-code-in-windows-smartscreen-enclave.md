---
title: 'Four-Byte Write and Timing Bug Let Researchers Run Code in Windows SmartScreen Enclave'
date: 2026-10-14
permalink: /posts/2026/10/14/four-byte-write-and-timing-bug-let-researchers-run-code-in-windows-smartscreen-enclave/
tags:
- veille-cyber
- hackernews
---
### Compromission de l'enclave de sécurité Windows SmartScreen

Des chercheurs en sécurité de Doyensec ont réussi à exécuter du code arbitraire au sein d'une enclave VBS (*Virtualization-Based Security*) de Windows, une zone mémoire isolée conçue pour protéger les données sensibles contre les accès non autorisés, même au niveau noyau.

**Points clés :**
*   **Cible :** L'enclave `SFAPE.dll`, utilisée par la fonctionnalité « Protection avancée contre le phishing » de Microsoft Defender SmartScreen pour protéger les mots de passe.
*   **Mécanisme d'attaque :** L'exploitation repose sur une écriture mémoire de quatre octets (provoquée par une double initialisation de l'enclave) combinée à une faille temporelle. Ces erreurs permettent de contourner les contrôles de sécurité et de détourner le fonctionnement interne de l'enclave.
*   **Contexte :** L'attaque nécessite un accès local préalable sur la machine. Elle démontre une rupture de l'isolation de l'enclave, bien qu'aucune preuve de vol de mot de passe n'ait été constatée.

**Vulnérabilité :**
*   **CVE-2026-83498 :** Élévation de privilèges (Score CVSS : 7.8, classée Critique).

**Recommandations :**
*   **Mise à jour système :** Appliquer la mise à jour cumulative de septembre 2026 (KB5124008) pour Windows 11 (versions 24H2 et 25H2), qui corrige la vulnérabilité et interdit le chargement de l'ancienne version de l'enclave.
*   **Vigilance sur le « BYOVD » :** Les chercheurs soulignent l'absence d'une liste de blocage généralisée pour les enclaves vulnérables. Il est recommandé de surveiller le chargement de bibliothèques signées mais obsolètes, une technique connue sous le nom de « *bring your own vulnerable enclave* » (BYOVE).

---
[Source](https://thehackernews.com/2026/10/four-byte-write-and-timing-bug-let.html){:target="_blank"}
