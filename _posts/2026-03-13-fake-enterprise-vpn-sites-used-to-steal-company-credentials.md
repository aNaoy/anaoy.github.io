---
title: 'Fake enterprise VPN sites used to steal company credentials'
date: 2026-03-13
permalink: /posts/2026/03/13/fake-enterprise-vpn-sites-used-to-steal-company-credentials/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de phishing par empoisonnement SEO : vol d'identifiants VPN

Le groupe cybercriminel Storm-2561 mène une campagne de distribution de faux clients VPN d'entreprises (Ivanti, Cisco, Fortinet, Sophos, etc.) via des techniques d'empoisonnement du référencement (SEO poisoning). En manipulant les résultats de recherche, les attaquants redirigent les utilisateurs vers des sites frauduleux imitant les plateformes légitimes pour leur faire télécharger des installateurs malveillants.

**Points clés :**
*   **Mode opératoire :** L'installateur déploie un infostealer (variante de *Hyrax*) qui capture les identifiants de connexion et les fichiers de configuration VPN (*connectionsstore.dat*).
*   **Persistance :** Une fois les données dérobées, le malware simule une erreur d'installation et redirige la victime vers le site officiel pour ne pas éveiller de soupçons, tout en installant une persistance via la clé de registre `RunOnce`.
*   **Légitimité apparente :** Le logiciel malveillant utilisait un certificat numérique légitime (désormais révoqué) pour éviter les alertes de sécurité lors de l'exécution.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle (CVE) spécifique, mais d'une faille humaine exploitée par l'ingénierie sociale et le détournement de confiance envers les sites de téléchargement.

**Recommandations :**
*   **Sécurité des terminaux :** Activer la protection fournie par le cloud dans Microsoft Defender et configurer l'EDR (Endpoint Detection and Response) en mode blocage.
*   **Authentification :** Imposer systématiquement l'authentification multifacteur (MFA) pour tout accès VPN.
*   **Hygiène numérique :** Utiliser des navigateurs protégés (SmartScreen activé) et s'assurer que les téléchargements de logiciels d'entreprise s'effectuent exclusivement via les portails officiels ou les déploiements gérés par l'équipe IT.
*   **Surveillance :** Analyser les indicateurs de compromission (IoCs) fournis par Microsoft pour identifier toute trace de *Pulse.exe* ou de fichiers suspects dans les répertoires d'installation courants.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-enterprise-vpn-downloads-used-to-steal-company-credentials/){:target="_blank"}
