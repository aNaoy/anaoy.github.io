---
title: 'VMware fixes three critical flaws allowing auth bypass, VM escapes'
date: 2026-07-30
permalink: /posts/2026/07/30/vmware-fixes-three-critical-flaws-allowing-auth-bypass-vm-escapes/
tags:
- veille-cyber
- bleepingcomp
---
### Alerte de sécurité : Correctifs critiques pour les infrastructures VMware

Broadcom a publié des mises à jour de sécurité pour corriger cinq vulnérabilités affectant VMware vCenter, ESX, Workstation et Fusion. Trois de ces failles sont classées comme critiques et permettent le contournement de l'authentification, l'exécution de code à distance ou l'évasion de machine virtuelle (VM escape).

**Vulnérabilités identifiées :**

*   **CVE-2026-59309 (CVSS 9.8) :** Contournement de l'authentification dans *VMware Directory Service* permettant à un attaquant non authentifié d'accéder au système via le réseau.
*   **CVE-2026-59310 (CVSS 9.8) :** Traversée de répertoire dans le serveur Syslog de vCenter permettant l'exécution de code arbitraire.
*   **CVE-2026-47876 (CVSS 9.3) :** Écriture hors limites dans l'adaptateur réseau virtuel VMXNET3, permettant à un administrateur local d'une VM de s'échapper vers l'hôte ESX.
*   **CVE-2026-41703 (CVSS 7.6) :** Lecture hors limites pouvant mener à une divulgation d'informations ou un déni de service.
*   **CVE-2026-41709 (CVSS 2.7) :** Défaut de journalisation permettant à un administrateur malveillant d'effectuer des opérations non tracées.

**Points clés :**
*   Aucun contournement (workaround) n'est disponible ; le passage à un autre type d'adaptateur réseau que VMXNET3 est déconseillé.
*   Bien qu'aucune exploitation active ne soit signalée, les serveurs VMware sont des cibles privilégiées pour les ransomwares et les cyberattaques persistantes.
*   Le déploiement est considéré comme un changement d'urgence selon la méthodologie ITIL.

**Recommandations :**
*   **Application immédiate :** Mettre à jour les systèmes vers les versions corrigées (vCenter/ESXi 9.1.0.0300, 9.0.2.0100 ou 8.0 Update 3k, et Workstation/Fusion 26H1).
*   **Gestion des interruptions :** La mise à jour de vCenter interrompt temporairement l'accès aux interfaces de gestion. Pour ESXi, prévoyez un redémarrage des hôtes ; utilisez *vMotion* pour déplacer les machines virtuelles en amont ou, à défaut, éteignez-les.
*   **Compatibilité :** Soyez vigilant lors de l'utilisation de *VMware Cloud Foundation*, car ces correctifs peuvent entraîner des erreurs de compatibilité ("back in time") avec certaines mises à niveau prévues.

---
[Source](https://www.bleepingcomputer.com/news/security/vmware-fixes-three-critical-flaws-allowing-auth-bypass-vm-escapes/){:target="_blank"}
