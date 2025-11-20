---
title: 'New SonicWall SonicOS flaw allows hackers to crash firewalls'
date: 2025-11-20
permalink: /posts/2025/11/20/new-sonicwall-sonicos-flaw-allows-hackers-to-crash-firewalls/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilité critique dans SonicOS : Risque de déni de service sur les pare-feux**

Une faille de sécurité critique a été identifiée dans le logiciel SonicOS de SonicWall, affectant le service SSLVPN. Cette vulnérabilité, référencée CVE-2025-40601, permet à un attaquant distant non authentifié de provoquer un déni de service (DoS), pouvant entraîner le crash des pare-feux concernés.

**Points Clés :**

*   **Nature de la vulnérabilité :** Dépassement de tampon basé sur la pile (stack-based buffer overflow).
*   **Impact :** Déni de service (DoS), potentiellement entraînant un crash du pare-feu.
*   **Versions affectées :**
    *   Pare-feux matériels et virtuels Gen7.
    *   Pare-feux Gen8.
*   **Versions non affectées :** Pare-feux Gen6, produits SSL VPN SMA 1000 et SMA 100.
*   **Exploitation actuelle :** SonicWall n'a pas connaissance d'exploitation active dans la nature ni de publication de preuve de concept.

**Vulnérabilités identifiées :**

*   **CVE-2025-40601 :** Vulnérabilité de déni de service dans le service SSLVPN de SonicOS.

**Recommandations :**

*   **Mise à jour immédiate :** Appliquer les correctifs publiés par SonicWall.
    *   Pour les pare-feux Gen7 : Versions 7.3.1-7013 et supérieures.
    *   Pour les pare-feux Gen8 : Versions 8.0.3-8011 et supérieures.
*   **Solutions de contournement (si la mise à jour n'est pas immédiate) :**
    *   Désactiver le service SonicOS SSLVPN.
    *   Restreindre l'accès à l'appliance du pare-feu SonicWall à des sources de confiance via la modification des règles.

Par ailleurs, deux vulnérabilités affectant les appliances de sécurité email de SonicWall ont été corrigées (CVE-2025-40604 pour l'exécution de code arbitraire et CVE-2025-40605 pour l'accès à des informations restreintes), et une mise à jour précédente avait corrigé une faille liée au rootkit OVERSTEP sur les appareils SMA 100.

---
[Source](https://www.bleepingcomputer.com/news/security/new-sonicwall-sonicos-flaw-allows-hackers-to-crash-firewalls/){:target="_blank"}
