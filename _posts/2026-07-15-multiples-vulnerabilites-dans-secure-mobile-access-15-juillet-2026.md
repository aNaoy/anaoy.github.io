---
title: 'Multiples vulnérabilités dans Secure Mobile Access (15 juillet 2026)'
date: 2026-07-15
permalink: /posts/2026/07/15/multiples-vulnerabilites-dans-secure-mobile-access-15-juillet-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilités critiques dans les équipements SonicWall SMA 1000

SonicWall a alerté sur l'exploitation active de deux vulnérabilités majeures touchant les passerelles Secure Mobile Access (SMA) 1000. Ces failles exposent les systèmes à des risques d'exécution de code et de falsification de requêtes.

**Systèmes affectés :**
*   Modèles 6210, 7210 et 8200v : versions 12.5.x antérieures à 12.5.0-02835.
*   Modèles 6210, 7210 et 8200v : versions antérieures à 12.4.3-03453.

**Vulnérabilités :**
*   **CVE-2026-15409 (SSRF) :** Permet une falsification de requêtes côté serveur par un attaquant non authentifié.
*   **CVE-2026-15410 (RCE) :** Permet à un administrateur authentifié d'exécuter du code arbitraire à distance.

**Recommandations :**
1.  **Mise à jour :** Appliquer les correctifs fournis par SonicWall dans le bulletin SNWLID-2026-0008.
2.  **Analyse des logs :** Rechercher les indicateurs de compromission spécifiés par l'éditeur.
3.  **Procédure en cas de compromission :** Si des traces d'exploitation sont détectées, la simple mise à jour est insuffisante. Il est impératif de :
    *   Réinstaller complètement le système.
    *   Réinitialiser l'intégralité des mots de passe (utilisateurs et administrateurs).
    *   Renouveler les jetons TOTP (authentification multifacteur).

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2026-ALE-006/){:target="_blank"}
