---
title: 'CISA: SafePay ransomware hit over 600 critical infrastructure orgs'
date: 2026-10-21
permalink: /posts/2026/10/21/cisa-safepay-ransomware-hit-over-600-critical-infrastructure-orgs/
tags:
- veille-cyber
- bleepingcomp
---
### Offensive d'envergure du ransomware SafePay contre les infrastructures critiques

Depuis août 2024, le groupe de ransomware SafePay a compromis plus de 600 organisations d'infrastructures critiques à travers le monde (Amérique du Nord, Amérique du Sud, Europe, Australie). Contrairement aux modèles basés sur des affiliés, SafePay opère de manière indépendante et pratique la double extorsion (chiffrement des données et menace de divulgation des informations volées).

**Points clés :**
* **Opérations actives :** Le groupe s'est imposé comme l'une des menaces les plus prolifiques depuis 2025, comblant le vide laissé par des groupes comme BlackCat ou LockBit.
* **Vecteurs d'accès initial :** Utilisation d'identifiants exposés, attaques par force brute sur les mots de passe et exploitation de VPN (particulièrement via des adresses IP du fournisseur Mullvad).
* **Techniques de compromission :** Usage de comptes hameçonnés, exploitation automatisée de vulnérabilités sur les équipements de périphérie (Edge devices) et suppression des clichés instantanés (shadow copies) ainsi que des sauvegardes sur les systèmes NAS pour entraver la restauration.

**Vulnérabilités :**
Bien qu'aucune CVE spécifique ne soit nommée dans l'article, les autorités (CISA, FBI, NCA) soulignent que le groupe cible activement les vulnérabilités répertoriées dans le catalogue **CISA Known Exploited Vulnerabilities (KEV)** affectant les VPN, les pare-feux et autres dispositifs exposés sur Internet.

**Recommandations :**
* **Renforcement de l'identité :** Implémenter l'authentification multifacteur (MFA) et des politiques robustes de gestion des accès (ICAM).
* **Gestion des privilèges :** Restreindre les outils et droits administratifs pour limiter les mouvements latéraux au sein du réseau.
* **Maintien en conditions de sécurité :** Appliquer rigoureusement les correctifs de sécurité, en priorité sur les équipements de périphérie (VPN, pare-feux).
* **Réponse aux incidents :** Ne pas payer la rançon (sans garantie de récupération) et signaler impérativement les attaques aux autorités compétentes.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-and-fbi-safepay-ransomware-has-hit-over-600-critical-infrastructure-organizations/){:target="_blank"}
