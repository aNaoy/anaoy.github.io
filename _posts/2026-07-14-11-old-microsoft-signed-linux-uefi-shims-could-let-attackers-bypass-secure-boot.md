---
title: '11 Old Microsoft-Signed Linux UEFI Shims Could Let Attackers Bypass Secure Boot'
date: 2026-07-14
permalink: /posts/2026/07/14/11-old-microsoft-signed-linux-uefi-shims-could-let-attackers-bypass-secure-boot/
tags:
- veille-cyber
- hackernews
---
### Contournement du Secure Boot via des « Shim » UEFI obsolètes signés par Microsoft

Des chercheurs ont identifié 11 applications UEFI (bootloaders « shim ») obsolètes, toujours signées par Microsoft, permettant de contourner la sécurité **Secure Boot**. Ces outils permettent à un attaquant d'exécuter du code malveillant avant même le chargement du système d'exploitation, facilitant l'installation de rootkits persistants (ex: BlackLotus) indétectables par les solutions EDR classiques.

**Points clés :**
* **Mécanisme d'attaque :** Les attaquants remplacent un shim légitime par une version vulnérable (mais toujours valide selon le firmware) pour exécuter du code arbitraire lors du démarrage.
* **Persistance :** L'attaque survit au redémarrage et parfois à la réinstallation du système d'exploitation.
* **Échec des protections :** Le contournement neutralise les mécanismes de défense comme la liste de révocation MOK (Machine Owner Key) et le système SBAT (Secure Boot Advanced Targeting).
* **Responsabilité :** Le problème provient de l'absence de révocation via la liste `DBX` (base de données des signatures révoquées) pour ces binaires spécifiques, bien que les vulnérabilités soient connues.

**Vulnérabilités :**
* **CVE-2026-8863**
* **CVE-2026-10797** (permettant le contournement du mécanisme de révocation basé sur les certificats).

**Systèmes impactés (liste non exhaustive) :**
Divers chargeurs de démarrage pour RedHat Enterprise Linux, CentOS, openSUSE, ROSA Linux, ainsi que des outils de gestion et de diagnostic (PC-Doctor, Baramundi, WipeDrive, Spyrus, Abitti).

**Recommandations :**
* **Mise à jour :** Appliquer les correctifs du « Patch Tuesday » de juin 2026 diffusés par Microsoft pour mettre à jour les listes de révocation `DBX`.
* **Surveillance :** S'assurer que les systèmes utilisent les versions les plus récentes du shim et que les mécanismes de sécurité UEFI sont correctement configurés.
* **Audit :** Identifier et supprimer toute présence d'anciens chargeurs de démarrage sur les machines, car leur simple présence sur le disque (même non actifs) peut être exploitée si un attaquant possède des privilèges d'administration.

---
[Source](https://thehackernews.com/2026/07/11-old-microsoft-signed-linux-uefi.html){:target="_blank"}
