---
title: 'SonicWall Warns Gen 6 Firewalls Wont Get Security Patches, Even for Critical Flaws'
date: 2026-11-20
permalink: /posts/2026/11/20/sonicwall-warns-gen-6-firewalls-wont-get-security-patches-even-for-critical-flaws/
tags:
- veille-cyber
- hackernews
---
### Fin de support critique pour les pare-feu SonicWall Gen 6

SonicWall exhorte ses clients à retirer immédiatement tous les pare-feu de génération 6 (Gen 6) de leurs environnements de production. Ces équipements ne reçoivent plus aucune mise à jour de sécurité, laissant les organisations vulnérables face à des attaques automatisées et assistées par l'IA, de plus en plus fréquentes contre les périphériques de périphérie (edge).

**Points clés :**
*   **Risque accru :** Les dispositifs exposés sur internet sont activement ciblés par les attaquants qui exploitent la vélocité des outils d'automatisation pour compromettre les infrastructures réseau.
*   **Vulnérabilité des équipements réseau :** Environ 23 % des vulnérabilités (CVE) découvertes récemment ciblent directement les équipements réseau, offrant aux attaquants un point d'entrée privilégié pour le vol d'identifiants, le mouvement latéral et le déploiement de ransomwares.
*   **Produits concernés :** L'ensemble de la gamme Gen 6 est impacté, incluant les séries TZ (ex: TZ300, TZ600), NSA (ex: NSA 2600, 6600), SOHO, SuperMassive, NSsp et les versions virtuelles (NSv).

**Recommandations :**
1.  **Migration immédiate :** Remplacer les unités Gen 6 par des modèles Gen 8 fonctionnant sous SonicOS 8.
2.  **Mesures d'urgence (en attendant le remplacement) :**
    *   Désactiver la gestion WAN (HTTPS, SSH, SNMP).
    *   Désactiver ou restreindre strictement l'accès SSL VPN aux adresses IP sources connues.
    *   Imposer l'authentification multifacteur (MFA) sur tous les comptes et réinitialiser les mots de passe locaux.
    *   Fermer les interfaces et services inutilisés.
    *   Renforcer la surveillance des journaux (logs) pour détecter toute activité inhabituelle.

---
[Source](https://thehackernews.com/2026/11/sonicwall-warns-gen-6-firewalls-wont.html){:target="_blank"}
