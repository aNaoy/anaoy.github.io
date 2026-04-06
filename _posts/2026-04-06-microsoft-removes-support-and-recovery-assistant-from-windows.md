---
title: 'Microsoft removes Support and Recovery Assistant from Windows'
date: 2026-04-06
permalink: /posts/2026/04/06/microsoft-removes-support-and-recovery-assistant-from-windows/
tags:
- veille-cyber
- bleepingcomp
---
### Fin du support de l'outil de diagnostic SaRA par Microsoft

Microsoft a officiellement abandonné et retiré l'utilitaire en ligne de commande « Support and Recovery Assistant » (SaRA) depuis le 10 mars. Cet outil, utilisé pour diagnostiquer et résoudre les problèmes liés à Office, Microsoft 365, Outlook et Windows, est supprimé dans le but de renforcer la sécurité des environnements informatiques.

**Points clés :**
*   **Obsolescence :** SaRA n'est plus pris en charge sur aucune version de Windows.
*   **Motivation :** La transition vers un nouvel outil vise à améliorer la sécurité globale et le durcissement des systèmes (hardening).
*   **Continuité :** Les fonctionnalités de diagnostic restent disponibles via un outil de remplacement.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée à cette décision ; il s'agit d'une mesure proactive de réduction de la surface d'attaque et d'amélioration de l'infrastructure de sécurité.

**Recommandations :**
*   **Migration immédiate :** Les administrateurs informatiques doivent cesser l'utilisation de SaRA et migrer vers l'outil **« Get Help »**.
*   **Utilisation de GetHelpCmd.exe :** Ce nouvel utilitaire offre des capacités similaires à SaRA, est prêt pour le déploiement en entreprise et peut être exécuté via des scripts (PowerShell) ou en ligne de commande pour une gestion distante des postes clients.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-removes-support-and-recovery-assistant-from-windows/){:target="_blank"}
