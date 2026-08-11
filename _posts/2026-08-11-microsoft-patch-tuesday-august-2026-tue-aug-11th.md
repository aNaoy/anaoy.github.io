---
title: 'Microsoft Patch Tuesday August 2026, (Tue, Aug 11th)'
date: 2026-08-11
permalink: /posts/2026/08/11/microsoft-patch-tuesday-august-2026-tue-aug-11th/
tags:
- veille-cyber
- sans-isc
---
### Analyse des correctifs Microsoft (Août 2026)

Le Patch Tuesday d'août 2026 corrige 418 vulnérabilités, dont 62 sont classées comme critiques. Le déploiement doit être priorisé pour contrer une vulnérabilité déjà exploitée et deux failles de type "zero-day" divulguées publiquement.

#### Points clés
*   **Exploitation active :** Une faille d'élévation de privilèges dans le pilote WinSock est activement exploitée.
*   **Zero-days :** Deux vulnérabilités (User Profile Service et Windows Container Isolation) ont été rendues publiques sans preuve d'exploitation active au moment de la publication.
*   **Risques critiques :** Plusieurs vulnérabilités d'exécution de code à distance (RCE) affectant les services QUIC et DNS présentent un risque majeur, avec un score CVSS de 9.8.

#### Vulnérabilités majeures
*   **CVE-2026-68820 (WinSock) :** Élévation de privilèges (CVSS 7.0). Permet à un utilisateur authentifié localement d'obtenir les privilèges SYSTEM via une condition de *race condition*. **Exploitation confirmée.**
*   **CVE-2026-62832 (User Profile Service) :** Élévation de privilèges (CVSS 7.8). Issue de type "link following" permettant d'accéder aux données d'un autre utilisateur ou d'obtenir des privilèges administrateur. **Divulguée publiquement.**
*   **CVE-2026-72971 (UnionFS) :** Faille de manipulation (tampering) dans le pilote de conteneurs (CVSS 5.5). Permet l'altération de fichiers via une résolution de lien incorrecte. **Divulguée publiquement.**
*   **CVE-2026-62815 (Microsoft QUIC) :** RCE (CVSS 9.8). Faille de type *use-after-free* exploitable à distance sans authentification par l'envoi de paquets malveillants.
*   **CVE-2026-62878 (Windows DNS Server) :** RCE (CVSS 9.8). Dépassement de tampon sur la pile, exploitable à distance par un attaquant non authentifié.

#### Recommandations
1.  **Priorité absolue :** Appliquer immédiatement les correctifs pour **CVE-2026-68820** sur tous les systèmes Windows, particulièrement ceux accessibles par des utilisateurs non approuvés.
2.  **Gestion des zero-days :** Appliquer les correctifs pour le **User Profile Service (CVE-2026-62832)** et le **pilote UnionFS (CVE-2026-72971)**. Limiter la réutilisation des comptes locaux.
3.  **Protection réseau :** Appliquer en priorité les mises à jour pour les serveurs DNS et les services exposant le protocole QUIC. En attendant le patch, restreindre l'accès à ces services aux réseaux de confiance et bloquer le trafic entrant inutile via pare-feu.
4.  **Surveillance :** Monitorer l'activité des services de profils (chargement suspect de ruches de registre) et les anomalies sur les serveurs DNS (plantages, trafic inhabituel).

---
[Source](https://isc.sans.edu/diary/rss/33236){:target="_blank"}
