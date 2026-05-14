---
title: 'Windows Zero-Days Expose BitLocker Bypasses And CTFMON Privilege Escalation'
date: 2026-05-14
permalink: /posts/2026/05/14/windows-zero-days-expose-bitlocker-bypasses-and-ctfmon-privilege-escalation/
tags:
- veille-cyber
- hackernews
---
### Nouvelles vulnérabilités Zero-Day sous Windows : BitLocker et élévation de privilèges

Deux nouvelles vulnérabilités zero-day, baptisées **YellowKey** et **GreenPlasma**, ont été révélées par le chercheur en sécurité « Chaotic Eclipse », ciblant Windows 11 et Windows Server 2022/2025.

#### Points clés
*   **YellowKey (Contournement BitLocker) :** Exploite une faille dans l'environnement de récupération Windows (WinRE). En manipulant des fichiers « FsTx » sur un support externe, un attaquant peut forcer le système à déverrouiller le volume BitLocker et obtenir un accès en ligne de commande (cmd.exe) via le mode dépannage, même avec une protection TPM+PIN.
*   **GreenPlasma (Élévation de privilèges) :** Concerne le framework *CTFMON*. Cette faille permet à un utilisateur non privilégié de créer des objets en mémoire (sections arbitraires) dans des répertoires normalement réservés au système, ouvrant la voie à une potentielle élévation de privilèges vers SYSTEM.
*   **Contexte BitLocker :** Parallèlement, des attaques de type « downgrade » (rétrogradation) exploitant des certificats obsolètes (PCA 2011) continuent de menacer BitLocker malgré les patchs précédents (notamment **CVE-2025-48804**).

#### Vulnérabilités identifiées
*   **YellowKey :** Faille de contournement BitLocker via WinRE (non encore patché).
*   **GreenPlasma :** Élévation de privilèges via *CTFMON* (non encore patché).
*   **CVE-2025-48804 :** Vulnerabilité de type *downgrade attack* du boot manager, utilisée pour contourner les protections par chiffrement.

#### Recommandations
*   **Authentification pré-démarrage :** Activer systématiquement un code **PIN BitLocker** au démarrage pour renforcer la protection contre l'accès physique.
*   **Gestion des certificats :** Migrer vers le certificat d'autorité **CA 2023** et révoquer les anciens certificats **PCA 2011** utilisés par le gestionnaire de démarrage (boot manager) pour prévenir les attaques par rétrogradation.
*   **Veille :** Surveiller les bulletins de sécurité de Microsoft en prévision du prochain « Patch Tuesday », le chercheur ayant annoncé de nouvelles divulgations.

---
[Source](https://thehackernews.com/2026/05/windows-zero-days-expose-bitlocker.html){:target="_blank"}
