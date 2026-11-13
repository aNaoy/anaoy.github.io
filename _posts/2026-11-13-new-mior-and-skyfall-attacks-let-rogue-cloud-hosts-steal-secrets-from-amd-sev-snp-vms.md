---
title: 'New Mior and Skyfall Attacks Let Rogue Cloud Hosts Steal Secrets From AMD SEV-SNP VMs'
date: 2026-11-13
permalink: /posts/2026/11/13/new-mior-and-skyfall-attacks-let-rogue-cloud-hosts-steal-secrets-from-amd-sev-snp-vms/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques affectant AMD SEV-SNP

Deux nouvelles attaques, **Mior** et **Skyfall**, permettent à un hôte malveillant (hyperviseur) de compromettre la confidentialité des machines virtuelles (VM) protégées par la technologie AMD SEV-SNP, conçue pourtant pour empêcher l'accès aux données par l'opérateur du serveur.

**Points clés :**
*   **Mior :** Exploite une faille lors du démarrage de la VM en manipulant la table de gestion mémoire (RMP). Cela permet à un attaquant de modifier la mémoire de la VM, d'accéder aux commandes de débogage et de falsifier les rapports d'attestation de sécurité.
*   **Skyfall :** Tire parti de failles de synchronisation (Transient Scheduler Attacks) pour récupérer des données sensibles, comme des clés de chiffrement, après une interruption forcée du démarrage d'une VM. Elle peut également exfiltrer des données du mode de gestion système (SMM).
*   **Conditions :** Ces attaques nécessitent un contrôle de l'hyperviseur. Mior requiert en plus un accès au BIOS/UEFI.

**Vulnérabilités identifiées :**
*   **CVE-2026-0462 (Mior) :** Score CVSS 5.9. Affecte le firmware SEV-SNP.
*   **CVE-2026-40671 (Skyfall - fuite de registres VM) :** Score CVSS 4.9.
*   **CVE-2026-18448 (Skyfall - fuite SMM) :** Score CVSS 5.6. Affecte le code firmware EDK II.

**Recommandations :**
*   **Mise à jour du firmware :** Appliquer les correctifs fournis par les constructeurs de serveurs (BIOS/UEFI et micrologiciels SEV). Le calendrier de déploiement des correctifs plate-forme s'échelonne entre novembre et décembre 2024, voire au-delà pour certains modèles embarqués.
*   **Gestion des fournisseurs cloud :** Les utilisateurs de machines virtuelles confidentielles dépendent entièrement de leurs fournisseurs cloud pour l'application de ces correctifs critiques au niveau du matériel hôte.
*   **Vérification :** Surveiller les bulletins de sécurité AMD (notamment AMD-SB-3059, AMD-SB-3061 et AMD-SB-7072) pour suivre les mises à jour spécifiques aux séries de processeurs EPYC utilisées.

---
[Source](https://thehackernews.com/2026/11/new-mior-and-skyfall-attacks-let-rogue.html){:target="_blank"}
