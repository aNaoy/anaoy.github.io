---
title: 'Microsoft Patch Tuesday April 2026., (Tue, Apr 14th)'
date: 2026-04-14
permalink: /posts/2026/04/14/microsoft-patch-tuesday-april-2026-tue-apr-14th/
tags:
- veille-cyber
- sans-isc
---
### Analyse du Patch Tuesday Microsoft d'avril 2026

La mise à jour de ce mois-ci corrige un total de 243 vulnérabilités. En excluant les 78 correctifs spécifiques à Chromium (déjà déployés pour Edge), il reste 165 vulnérabilités affectant l'écosystème Microsoft, dont 8 critiques et 154 importantes. Une vulnérabilité est actuellement exploitée activement.

**Points clés :**
*   **Volumétrie :** 243 CVE au total.
*   **Vecteurs d'attaque :** De nombreuses failles concernent l'exécution de code à distance (RCE), l'élévation de privilèges (EoP) et le contournement de fonctionnalités de sécurité.
*   **Menace active :** `CVE-2026-32201` (SharePoint) est confirmée comme étant activement exploitée.

**Vulnérabilités notables :**

| CVE | Type | Gravité | Note |
| :--- | :--- | :--- | :--- |
| **CVE-2026-33827** | RCE (TCP/IP) | Critique | Race condition permettant l'exécution de code arbitraire via le réseau. |
| **CVE-2026-33826** | RCE (Active Directory) | Critique | Score CVSS 8.0, risque élevé pour les infrastructures. |
| **CVE-2026-33114/5** | RCE (Word) | Critique | Risques d'exécution de code via des fichiers Word compromis. |
| **CVE-2026-32157** | RCE (RDP) | Critique | Risque lors de la connexion à un serveur RDP malveillant. |
| **CVE-2026-33824** | RCE (IKE/IPSEC) | Critique | Service souvent non activé par défaut, impact à surveiller. |
| **CVE-2026-32201** | Spoofing (SharePoint) | Important | **Exploitée activement.** |
| **CVE-2026-33825** | EoP (Defender) | Important | Déjà divulguée publiquement. |

**Recommandations :**
*   **Priorisation :** Appliquer en priorité les correctifs pour les vulnérabilités RCE et celle déjà exploitée (`CVE-2026-32201`).
*   **Surveillance :** Surveiller les services non essentiels (comme IKE/IPSEC) et restreindre les accès aux serveurs SharePoint et RDP.
*   **Hygiène logicielle :** Bien que les correctifs Edge aient été anticipés, s'assurer que l'ensemble du parc est à jour pour mitiger les failles persistantes liées au noyau (Kernel), au spooler d'impression et aux composants Office.

---
[Source](https://isc.sans.edu/diary/rss/32898){:target="_blank"}
