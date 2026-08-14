---
title: 'Akira hackers disable EDR with Safe Mode, steal data but fail to encrypt'
date: 2026-08-14
permalink: /posts/2026/08/14/akira-hackers-disable-edr-with-safe-mode-steal-data-but-fail-to-encrypt/
tags:
- veille-cyber
- bleepingcomp
---
### Contournement de l'EDR via le mode sans échec : le cas Akira

Des attaquants utilisant le ransomware Akira ont compromis un réseau en exploitant un VPN SonicWall dépourvu d'authentification multifacteur (MFA). Bien que l'opération de chiffrement ait échoué, les assaillants ont réussi à exfiltrer des données sensibles en moins de cinq heures.

**Points clés de l'attaque :**
*   **Accès initial :** Utilisation d'un VPN non sécurisé par MFA.
*   **Mouvement latéral :** Accès au contrôleur de domaine via RDP, énumération de l'Active Directory, puis déploiement d'AnyDesk.
*   **Technique d'évasion :** Forçage du redémarrage du système en « Mode sans échec avec prise en charge réseau ». Cela a permis de désactiver les agents EDR (Huntress) et Microsoft Defender, rendant le système vulnérable pendant 10 minutes.
*   **Persistance :** Ajout d'AnyDesk au registre du mode sans échec pour garantir un accès persistant.
*   **Échec du chiffrement :** La charge utile du ransomware a échoué en raison d'erreurs de mémoire virtuelle et de PowerShell, bien que le vol de données ait été accompli.

**Vulnérabilités exploitées :**
*   **Absence de MFA :** Accès VPN vulnérable aux attaques par force brute ou aux identifiants compromis.
*   **Mode sans échec Windows :** Conception permettant de suspendre les services de sécurité tiers. Aucune CVE spécifique n'est associée, car il s'agit d'un détournement de fonctionnalité système native.

**Recommandations :**
*   **Renforcement des accès :** Imposer l'authentification multifacteur (MFA) sur tous les accès distants (VPN).
*   **Détection proactive :** Surveiller étroitement les modifications des configurations de démarrage (boot) et les ajouts d'outils de prise en main à distance dans les clés de registre liées au mode sans échec.
*   **Limitation des privilèges :** Restreindre l'accès RDP et surveiller les comportements anormaux au sein de l'Active Directory.
*   **Analyse comportementale :** Mettre en place des alertes sur l'utilisation inhabituelle de commandes système liées au redémarrage en mode de diagnostic.

---
[Source](https://www.bleepingcomputer.com/news/security/akira-hackers-disable-edr-with-safe-mode-steal-data-but-fail-to-encrypt/){:target="_blank"}
