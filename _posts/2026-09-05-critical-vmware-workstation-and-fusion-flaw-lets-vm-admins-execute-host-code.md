---
title: 'Critical VMware Workstation and Fusion Flaw Lets VM Admins Execute Host Code'
date: 2026-09-05
permalink: /posts/2026/09/05/critical-vmware-workstation-and-fusion-flaw-lets-vm-admins-execute-host-code/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans VMware Workstation et Fusion

Broadcom a publié des correctifs pour deux vulnérabilités majeures touchant VMware Workstation et Fusion (versions 25H2 et 26H1). Bien que leur exploitation nécessite des privilèges administratifs locaux sur une machine virtuelle, elles permettent de compromettre l'hôte sous-jacent.

**Points clés :**
*   Les vulnérabilités permettent une exécution de code arbitraire sur l'hôte à partir d'une machine virtuelle.
*   L'exploitation repose sur l'obtention préalable de droits d'administrateur local sur la VM, pouvant être acquis via d'autres vecteurs (phishing, mauvaises configurations).
*   Aucune preuve d'exploitation active n'a été constatée à ce jour, mais les produits VMware sont des cibles privilégiées par les acteurs malveillants.

**Vulnérabilités :**
*   **CVE-2026-59346 (Score CVSS : 9.3) :** Une faille de dépassement d'entier (integer overflow) située dans l'adaptateur réseau virtuel VMXNET3, permettant une exécution de code sur l'hôte.
*   **CVE-2026-59347 (Score CVSS : 8.1) :** Une faille de dépassement de tampon (buffer overflow) basée sur la pile dans HGFS (Host Guest File System), permettant d'exécuter du code via le processus VMX de l'hôte.

**Recommandations :**
*   Il n'existe aucune solution de contournement (workaround) pour ces failles.
*   La seule protection efficace est la mise à jour immédiate vers les versions corrigées : **VMware Workstation 26H1u1** ou **VMware Fusion 26H1u1**.

---
[Source](https://thehackernews.com/2026/09/critical-vmware-workstation-and-fusion.html){:target="_blank"}
