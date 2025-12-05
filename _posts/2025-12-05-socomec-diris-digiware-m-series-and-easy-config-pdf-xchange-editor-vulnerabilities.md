---
title: 'Socomec DIRIS Digiware M series and Easy Config, PDF XChange Editor vulnerabilities'
date: 2025-12-05
permalink: /posts/2025/12/05/socomec-diris-digiware-m-series-and-easy-config-pdf-xchange-editor-vulnerabilities/
tags:
- veille-cyber
- zerodaysfans
---
**Sécurité des logiciels : vulnérabilités corrigées dans PDF XChange Editor et les produits Socomec**

Des failles de sécurité ont été découvertes et corrigées dans le logiciel PDF XChange Editor et dans plusieurs produits de Socomec, notamment la série DIRIS Digiware M et le système Easy Config. Ces vulnérabilités ont été traitées selon la politique de divulgation des vulnérabilités tierces de Cisco.

**Points Clés :**

*   **PDF XChange Editor :** une vulnérabilité de lecture hors limites (TALOS-2025-2280 / CVE-2025-58113) a été identifiée dans la fonctionnalité EMF. Elle pourrait permettre à un attaquant de divulguer des informations sensibles en utilisant un fichier EMF spécialement conçu.
*   **Socomec DIRIS Digiware M Series (version 1.6.9) :** Neuf vulnérabilités ont été découvertes. Celles-ci incluent la transmission en clair (TALOS-2024-2115 / CVE-2024-48894), le falsification de requête intersite (TALOS-2024-2116 / CVE-2024-53684), et plusieurs vulnérabilités de déni de service (TALOS-2024-2118 / CVE-2024-49572, TALOS-2024-2119 / CVE-2024-48882, TALOS-2025-2138 / CVE-2025-20085, TALOS-2025-2139 / CVE-2025-23417, TALOS-2025-2248 / CVE-2025-54848-CVE-2025-54851, TALOS-2025-2251 / CVE-2025-55221-CVE-2025-55222, TALOS-2025-2152 / CVE-2025-26858). Certaines de ces vulnérabilités de déni de service peuvent également affaiblir les identifiants, restaurant les identifiants par défaut.
*   **Socomec Easy Config System :** une vulnérabilité de contournement d'authentification (TALOS-2024-2117 / CVE-2024-45370) a été détectée dans la gestion des profils utilisateurs, permettant un accès non autorisé via la modification d'une base de données locale.

**Vulnérabilités Identifiées :**

*   **PDF XChange Editor :**
    *   TALOS-2025-2280 (CVE-2025-58113) : Lecture hors limites
*   **Socomec DIRIS Digiware M Series :**
    *   TALOS-2024-2115 (CVE-2024-48894) : Transmission en clair
    *   TALOS-2024-2116 (CVE-2024-53684) : Falsification de requête intersite (CSRF)
    *   TALOS-2024-2118 (CVE-2024-49572) : Déni de service
    *   TALOS-2024-2119 (CVE-2024-48882) : Déni de service
    *   TALOS-2025-2138 (CVE-2025-20085) : Déni de service
    *   TALOS-2025-2139 (CVE-2025-23417) : Déni de service
    *   TALOS-2025-2248 (CVE-2025-54848-CVE-2025-54851) : Déni de service (Modbus TCP/RTU over TCP)
    *   TALOS-2025-2251 (CVE-2025-55221-CVE-2025-55222) : Déni de service (Modbus TCP/RTU over TCP USB)
    *   TALOS-2025-2152 (CVE-2025-26858) : Dépassement de tampon (Modbus TCP)
*   **Socomec Easy Config System :**
    *   TALOS-2024-2117 (CVE-2024-45370) : Contournement d'authentification

**Recommandations :**

Bien que les vulnérabilités aient été corrigées par les éditeurs respectifs, il est conseillé aux utilisateurs de s'assurer qu'ils disposent des dernières versions et des correctifs de sécurité pour PDF XChange Editor et les produits Socomec mentionnés. Pour la détection des tentatives d'exploitation, les ensembles de règles Snort les plus récents sont disponibles sur Snort.org.

---
[Source](https://blog.talosintelligence.com/socomec-diris-digiware-m-series-and-easy-config-pdf-xchange-editor-vulnerabilities/){:target="_blank"}
