---
title: 'Citrix Patches Six NetScaler Flaws Allowing File Read and Denial-of-Service'
date: 2026-07-01
permalink: /posts/2026/07/01/citrix-patches-six-netscaler-flaws-allowing-file-read-and-denial-of-service/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques et correctifs pour Citrix NetScaler

Citrix a publié des correctifs pour six vulnérabilités affectant ses solutions NetScaler ADC et NetScaler Gateway, permettant potentiellement la lecture arbitraire de fichiers ou le déclenchement de dénis de service (DoS). Aucune exploitation active n'a été signalée à ce jour.

#### Points clés
* Les failles touchent divers composants, notamment SAML, la gestion HTTP/2 et les profils TCP.
* La fragilité de la gestion mémoire dans les appliances NetScaler reste une préoccupation majeure pour la sécurité.
* Les correctifs sont disponibles pour les versions 14.1, 13.1, ainsi que leurs variantes FIPS et NDcPP.

#### Vulnérabilités répertoriées
* **CVE-2026-8451 (CVSS 8.8) :** Lecture mémoire hors limites via des requêtes SAML malformées.
* **CVE-2026-8452 (CVSS 8.8) :** Dépassement mémoire provoquant un DoS (Gateway/AAA).
* **CVE-2026-8655 (CVSS 8.8) :** Dépassement mémoire provoquant un DoS (Load Balancing Oracle, DNS Proxy/Resolver).
* **CVE-2026-13474 (CVSS 8.7) :** Déni de service via des requêtes HTTP/2 malformées.
* **CVE-2026-10816 (CVSS 7.7) :** Lecture arbitraire de fichiers sans authentification.
* **CVE-2026-10817 (CVSS 6.9) :** Lecture mémoire hors limites liée aux profils TCP.

#### Recommandations
1. **Mise à jour immédiate :** Appliquez les versions corrigées (14.1-72.61, 13.1-63.18, ou versions ultérieures selon la configuration).
2. **Configuration spécifique (CVE-2026-13474) :**
   * Pour les appliances n'utilisant pas de profils HTTP stricts (où la valeur par défaut est 0), il est impératif de configurer manuellement le paramètre `Http2SmallWndTimeout` à 30 secondes via la commande suivante :
     `set ns httpProfile <nom_du_profil> -http2SmallWndTimeout 30`

---
[Source](https://thehackernews.com/2026/07/citrix-patches-six-netscaler-flaws.html){:target="_blank"}
