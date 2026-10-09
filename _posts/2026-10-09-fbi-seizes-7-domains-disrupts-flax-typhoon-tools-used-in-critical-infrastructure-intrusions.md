---
title: 'FBI Seizes 7 Domains, Disrupts Flax Typhoon Tools Used in Critical Infrastructure Intrusions'
date: 2026-10-09
permalink: /posts/2026/10/09/fbi-seizes-7-domains-disrupts-flax-typhoon-tools-used-in-critical-infrastructure-intrusions/
tags:
- veille-cyber
- hackernews
---
### Démantèlement des infrastructures du groupe Flax Typhoon par le FBI

Le FBI et le département de la Justice des États-Unis ont neutralisé les outils cybernétiques du groupe **Flax Typhoon** (également connu sous les noms d'Ethereal Panda ou RedJuliett), une entité liée à la société pékinoise *Integrity Technology Group*. Cette opération a consisté à saisir sept domaines utilisés pour le pilotage de botnets et la réalisation d'activités malveillantes contre des infrastructures critiques mondiales.

#### Points clés
*   **Mode opératoire :** Le groupe exploitait un botnet massif (basé sur une variante de Mirai et géré par l'application "Sparrow") composé de plus d'un million d'appareils IoT et SOHO infectés.
*   **Outils identifiés :**
    *   **Microscan :** Un outil de reconnaissance et de scan de vulnérabilités contenant plus de 1 300 scripts de test.
    *   **FishHub :** Un outil dédié au hameçonnage ciblé (*spear-phishing*) et au déploiement de charges utiles.
*   **Cibles :** Les attaques ont visé des secteurs critiques, notamment l'énergie (USA), des aéroports (Japon, Pologne), des ONG et des établissements d'enseignement supérieur (Taïwan).
*   **Persistence et techniques :** Utilisation du logiciel VPN *SoftEther* pour le maintien des accès, recours à *EBurst* pour le bruteforce sur Microsoft 365, et exploitation de failles via des outils open source (BBScan, dirsearch, NMAP, etc.).

#### Vulnérabilités exploitées
Bien que les CVE spécifiques ne soient pas listées, l'article souligne que le scanner *Microscan* automatise l'exploitation de vulnérabilités connues dans :
*   **Services et applications :** OpenSSL, Oracle WebLogic, Rejetto, WordPress, Juniper ScreenOS, Jenkins et Apache Struts.
*   **Techniques :** Cross-Site Scripting (XSS) pour la collecte d'identifiants.

#### Recommandations
*   **Sécurisation des dispositifs IoT :** Mettre régulièrement à jour les firmwares des équipements SOHO et IoT pour prévenir leur intégration dans des botnets de type Mirai.
*   **Hygiène des accès :** Appliquer une authentification multifacteur (MFA) robuste sur les environnements cloud (Microsoft 365) pour contrer les outils de bruteforce comme *EBurst*.
*   **Surveillance réseau :** Surveiller les communications sortantes vers des serveurs C2 suspects et limiter l'utilisation de logiciels d'accès distant non autorisés (ex: SoftEther).
*   **Protection contre le phishing :** Renforcer la sensibilisation des utilisateurs face aux campagnes de spear-phishing et restreindre les capacités d'exécution de scripts non approuvés sur les postes de travail.

---
[Source](https://thehackernews.com/2026/10/fbi-seizes-7-domains-disrupts-flax.html){:target="_blank"}
