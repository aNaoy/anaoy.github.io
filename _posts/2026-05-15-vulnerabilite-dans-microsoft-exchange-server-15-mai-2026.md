---
title: 'Vulnérabilité dans Microsoft Exchange Server (15 mai 2026)'
date: 2026-05-15
permalink: /posts/2026/05/15/vulnerabilite-dans-microsoft-exchange-server-15-mai-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilité critique active sur Microsoft Exchange Server

Une faille de sécurité critique, identifiée sous la référence **CVE-2026-42897**, affecte actuellement Microsoft Exchange Server et fait l'objet d'une exploitation active.

**Points clés :**
*   La vulnérabilité permet à un attaquant non authentifié d'exécuter une injection de code indirecte (XSS) et de contourner les politiques de sécurité.
*   L'attaque se déclenche lorsqu'un utilisateur ouvre un courriel malveillant via Outlook Web Access (OWA).

**Vulnérabilité :**
*   **CVE-2026-42897** : Risque d'exécution de code à distance et contournement de sécurité.

**Recommandations :**
*   **Environnements connectés :** S'assurer que le service *Exchange Emergency Mitigation Service* est bien activé (fonctionnement par défaut).
*   **Environnements déconnectés :** Appliquer manuellement la procédure de contournement fournie par Microsoft via leur documentation officielle.
*   **Veille :** Surveiller étroitement les publications de Microsoft pour déployer le correctif officiel dès sa mise à disposition.

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2026-ALE-005/){:target="_blank"}
