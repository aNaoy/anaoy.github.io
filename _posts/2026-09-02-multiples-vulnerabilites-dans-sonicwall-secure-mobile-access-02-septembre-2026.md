---
title: 'Multiples vulnérabilités dans SonicWall Secure Mobile Access (02 septembre 2026)'
date: 2026-09-02
permalink: /posts/2026/09/02/multiples-vulnerabilites-dans-sonicwall-secure-mobile-access-02-septembre-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilités critiques sur les équipements SonicWall SMA 1000

SonicWall a alerté sur deux vulnérabilités critiques affectant les appliances Secure Mobile Access (SMA) 1000, actuellement exploitées par des attaquants.

**Vulnérabilités identifiées :**
*   **CVE-2026-83548 :** Falsification de requêtes côté serveur (SSRF) exploitable par un attaquant non authentifié.
*   **CVE-2026-83549 :** Exécution de code arbitraire à distance (RCE) accessible à un attaquant disposant de privilèges administrateur.

**Systèmes affectés :**
*   Modèles SMA 6210, 7210 et 8200v (versions 12.5.x antérieures à 12.5.0-02952).
*   Modèles SMA 6210, 7210 et 8200v (versions antérieures à 12.4.3-03526).

**Recommandations :**
L'application des correctifs logiciels fournis par SonicWall est indispensable mais insuffisante compte tenu de l'exploitation active. Il est impératif de réaliser les opérations suivantes pour sécuriser les équipements :
*   Réinstaller le système.
*   Renouveler l'intégralité des mots de passe (utilisateurs et administrateurs).
*   Réinitialiser les jetons TOTP (Time-based One Time Password).
*   Contacter le support technique de SonicWall pour obtenir les indicateurs de compromission (IoC).

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2026-ALE-009/){:target="_blank"}
