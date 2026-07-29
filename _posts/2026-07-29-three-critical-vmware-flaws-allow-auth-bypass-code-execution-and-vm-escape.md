---
title: 'Three Critical VMware Flaws Allow Auth Bypass, Code Execution, and VM Escape'
date: 2026-07-29
permalink: /posts/2026/07/29/three-critical-vmware-flaws-allow-auth-bypass-code-execution-and-vm-escape/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques et correctifs de sécurité chez VMware

Broadcom a publié des correctifs de sécurité pour ses solutions VMware (ESXi, vCenter, Workstation et Fusion) afin de corriger six vulnérabilités, dont trois sont classées comme critiques. À ce jour, aucune preuve d'exploitation active n'a été signalée.

**Points clés :**
*   **Risques majeurs :** Les failles les plus graves permettent le contournement de l'authentification, l'exécution de code arbitraire et l'évasion de machine virtuelle (VM escape).
*   **Vecteurs d'attaque :** Les vulnérabilités concernent principalement des accès réseau vers vCenter ou des privilèges administrateur locaux au sein d'une machine virtuelle.

**Vulnérabilités identifiées :**

| CVE | Sévérité (CVSS) | Description |
| :--- | :--- | :--- |
| **CVE-2026-59309** | 9.8 (Critique) | Contournement de l'authentification dans VMware vCenter. |
| **CVE-2026-59310** | 9.8 (Critique) | Traversée de répertoire dans vCenter permettant l'exécution de code. |
| **CVE-2026-47876** | 9.3 (Critique) | Écriture hors limites dans VMXNET3 permettant une évasion de VM. |
| **CVE-2026-41703** | 7.6 | Lecture hors limites dans ESX (divulgation d'infos ou DoS). |
| **CVE-2026-41709** | 2.7 | Journalisation insuffisante dans ESX. |

**Recommandations :**
Il est impératif de mettre à jour les environnements VMware vers les versions corrigées dès que possible :
*   **VMware vCenter / VCF :** Appliquer les correctifs vers les versions 8.0 U3k, 9.0.2.0100 ou 9.1.0.0300 selon votre infrastructure.
*   **VMware ESXi :** Appliquer les correctifs spécifiques (ex: ESXi80U3k, ou les versions 9.x mentionnées).
*   **Workstation et Fusion :** Mettre à jour vers la version 26H1.

---
[Source](https://thehackernews.com/2026/07/three-critical-vmware-flaws-allow-auth.html){:target="_blank"}
