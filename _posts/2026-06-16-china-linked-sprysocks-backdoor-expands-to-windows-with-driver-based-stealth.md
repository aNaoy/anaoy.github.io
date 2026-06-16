---
title: 'China-Linked SprySOCKS Backdoor Expands to Windows with Driver-Based Stealth'
date: 2026-06-16
permalink: /posts/2026/06/16/china-linked-sprysocks-backdoor-expands-to-windows-with-driver-based-stealth/
tags:
- veille-cyber
- hackernews
---
### Expansion du backdoor SprySOCKS : Menaces sur Windows et furtivité accrue

Le groupe de cyberespionnage "FishMonger" (lié à l'acteur étatique chinois Earth Lusca) a adapté son backdoor Linux, **SprySOCKS**, pour cibler les environnements Windows. Ce déploiement marque une montée en puissance de leurs capacités cross-plateforme et de leur furtivité.

**Points clés :**
*   **Variantes Windows :** Deux versions, `WIN_DRV` et `WIN_PLUS`, ont été identifiées.
*   **Techniques de dissimulation :** Utilisation de pilotes noyau (RawWNPF) pour masquer les processus, connexions réseau, fichiers et clés de registre.
*   **Persistance et exécution :** Utilisation de techniques de chargement avancées, notamment le *DLL side-loading* et l'injection via le service d'impression Windows (*Print Spooler*).
*   **Ciblage :** Des attaques observées entre 2023 et 2024 visant des organisations gouvernementales à travers le monde (Honduras, Taïwan, Thaïlande, Pakistan).
*   **Infrastructure :** Le malware utilise une communication C2 flexible via TCP, UDP et WebSocket.

**Vulnérabilités exploitées :**
*   **CVE-2023-24932 :** Faille de contournement du gestionnaire de démarrage Windows (associée au bootkit BlackLotus). L'exploitation permet une persistance profonde au niveau UEFI.
*   *Note :* Le groupe privilégie également l'exploitation de vulnérabilités "N-day" sur des solutions exposées (Fortinet, GitLab, Microsoft Exchange, Zimbra, etc.) pour l'accès initial.

**Recommandations :**
*   **Gestion des correctifs (Patch Management) :** Appliquer prioritairement les mises à jour pour les vulnérabilités N-day connues touchant les applications exposées sur Internet.
*   **Mise à jour du firmware/Boot :** S'assurer que le correctif pour la CVE-2023-24932 est appliqué et que le *Secure Boot* est correctement configuré.
*   **Surveillance du service d'impression :** Restreindre les privilèges du service `spoolsv.exe` et surveiller les comportements inhabituels des processus enfants lancés par ce service.
*   **Analyse comportementale :** Détecter l'exécution de pilotes non signés ou suspects (comme `RawWNPF`) et monitorer les communications réseau non standards vers des ports aléatoires (détournement de trafic TCP).

---
[Source](https://thehackernews.com/2026/06/china-linked-sprysocks-backdoor-expands.html){:target="_blank"}
