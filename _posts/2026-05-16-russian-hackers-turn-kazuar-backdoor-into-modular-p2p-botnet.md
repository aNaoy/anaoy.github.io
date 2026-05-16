---
title: 'Russian hackers turn Kazuar backdoor into modular P2P botnet'
date: 2026-05-16
permalink: /posts/2026/05/16/russian-hackers-turn-kazuar-backdoor-into-modular-p2p-botnet/
tags:
- veille-cyber
- bleepingcomp
---
### Évolution de Kazuar : Le botnet modulaire du groupe Secret Blizzard

Le groupe de cyberespionnage russe Secret Blizzard (lié au FSB) a transformé sa porte dérobée Kazuar en un botnet P2P modulaire sophistiqué, conçu pour l'espionnage à long terme contre des cibles gouvernementales, diplomatiques et militaires.

**Points clés :**
*   **Architecture modulaire :** Le malware repose sur trois modules :
    *   **Kernel :** Coordonne les tâches et élit un « leader » parmi les machines infectées pour centraliser les communications, minimisant ainsi le trafic réseau suspect.
    *   **Bridge :** Agit comme un proxy de communication entre le réseau interne et le serveur de commande (C2) via HTTP, WebSockets ou EWS.
    *   **Worker :** Exécute les actions malveillantes (keylogging, capture d'écran, vol de données, exfiltration).
*   **Furtivité :** Les communications internes utilisent des canaux légitimes (IPC, Windows Messaging, Named Pipes) chiffrés en AES.
*   **Polyvalence :** Le logiciel propose plus de 150 options de configuration, incluant des mécanismes de contournement de sécurité avancés.

**Vulnérabilités exploitées :**
*   Le malware intègre des techniques de contournement spécifiques aux mécanismes de sécurité natifs de Windows, notamment :
    *   **AMSI** (Antimalware Scan Interface)
    *   **ETW** (Event Tracing for Windows)
    *   **WLDP** (Windows Lockdown Policy)
*   *Note : Aucune CVE spécifique n'est mentionnée dans l'article, le malware exploitant les fonctionnalités du système plutôt qu'une faille logicielle précise.*

**Recommandations :**
*   **Détection comportementale :** Privilégier une approche de détection basée sur les comportements suspects plutôt que sur des signatures statiques, Kazuar étant trop configurable pour être détecté par des outils traditionnels.
*   **Surveillance IPC :** Porter une attention particulière aux communications inter-processus anormales (Named Pipes, Mailslots) au sein du réseau.
*   **Validation des contrôles :** Tester régulièrement l'efficacité des règles de détection et des configurations de sécurité contre les tactiques d'évasion (AMSI/ETW bypass).

---
[Source](https://www.bleepingcomputer.com/news/security/russian-hackers-turn-kazuar-backdoor-into-modular-p2p-botnet/){:target="_blank"}
