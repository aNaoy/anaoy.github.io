---
title: '9 Critical IP KVM Flaws Enable Unauthenticated Root Access Across Four Vendors'
date: 2026-03-19
permalink: /posts/2026/03/19/9-critical-ip-kvm-flaws-enable-unauthenticated-root-access-across-four-vendors/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les dispositifs IP KVM : Risques et mesures de protection

Des chercheurs d'Eclypsium ont identifié neuf failles de sécurité majeures affectant des dispositifs IP KVM (Keyboard, Video, Mouse) de quatre constructeurs (GL-iNet, Angeet/Yeeso, Sipeed et JetKVM). Ces failles permettent à des attaquants non authentifiés de prendre le contrôle total des systèmes connectés en contournant les protections au niveau du BIOS/UEFI.

**Points clés :**
*   **Risque majeur :** La compromission d'un KVM offre un accès physique virtuel à l'hôte. Un attaquant peut injecter des frappes clavier, contourner le chiffrement des disques ou le "Secure Boot", et installer des backdoors persistantes indétectables par les logiciels de sécurité de l'OS.
*   **Faiblesses structurelles :** Absence de signature de firmware, défauts de contrôle d'accès, interfaces de débogage exposées et absence de protection contre le brute-force.

**Vulnérabilités répertoriées :**

| CVE | Score CVSS | Dispositif | Problématique |
| :--- | :--- | :--- | :--- |
| **CVE-2026-32290** | 4.2 | GL-iNet | Vérification insuffisante du firmware |
| **CVE-2026-32291** | 7.6 | GL-iNet | Accès root via UART |
| **CVE-2026-32292** | 5.3 | GL-iNet | Protection brute-force insuffisante |
| **CVE-2026-32293** | 3.1 | GL-iNet | Provisionnement non sécurisé |
| **CVE-2026-32294** | 6.7 | JetKVM | Vérification de mise à jour insuffisante |
| **CVE-2026-32295** | 7.3 | JetKVM | Limitation de débit (rate limiting) insuffisante |
| **CVE-2026-32296** | 5.4 | Sipeed | Exposition d'un point de configuration |
| **CVE-2026-32297** | 9.8 | Angeet ES3 | Absence d'authentification (code arbitraire) |
| **CVE-2026-32298** | 8.8 | Angeet ES3 | Injection de commandes OS |

**Recommandations :**
*   **Segmentation réseau :** Isoler impérativement les dispositifs KVM sur un VLAN de gestion dédié.
*   **Accès restreint :** Bloquer tout accès direct à ces appareils depuis Internet. Utiliser des outils de scan (type Shodan) pour vérifier l'exposition externe.
*   **Durcissement :** Activer l'authentification multifacteur (MFA) si supportée et mettre à jour le firmware dès que les correctifs sont disponibles.
*   **Surveillance :** Monitorer le trafic réseau entrant et sortant des dispositifs KVM pour détecter toute activité suspecte.

---
[Source](https://thehackernews.com/2026/03/9-critical-ip-kvm-flaws-enable.html){:target="_blank"}
