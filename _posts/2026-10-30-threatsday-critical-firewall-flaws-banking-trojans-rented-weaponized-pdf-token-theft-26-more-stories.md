---
title: 'ThreatsDay: Critical Firewall Flaws, Banking Trojans Rented, Weaponized PDF, Token Theft + 26 More Stories'
date: 2026-10-30
permalink: /posts/2026/10/30/threatsday-critical-firewall-flaws-banking-trojans-rented-weaponized-pdf-token-theft-26-more-stories/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces : IA, vulnérabilités critiques et compromissions

Le paysage actuel de la cybersécurité est marqué par une recrudescence d'attaques exploitant des erreurs humaines, des outils d'IA détournés et des vulnérabilités non corrigées. Les attaquants allient techniques sophistiquées et négligences de configuration pour maximiser l'impact de leurs campagnes.

#### Points clés
*   **Détournement de l'IA :** Des acteurs malveillants usurpent l'identité de robots IA (ChatGPT, Claude, etc.) pour automatiser la recherche de secrets (clés API, fichiers `.env`) sur le web.
*   **Évolution des Infostealers :** Les logiciels de vol de données (StealC, Icarus) mutent en chevaux de Troie d'accès à distance (RAT), intégrant des capacités de contrôle en temps réel et de détournement de session.
*   **Abus de confiance :** Les attaquants exploitent des composants logiciels légitimes (ex: outils de gestion de caméras, MDM) pour maintenir une présence persistante et furtive sur les réseaux.
*   **Campagnes d'extorsion :** L'usage de l'IA pour générer des scripts d'attaque et des ransomwares devient un modèle économique rentable et scalable ("Ransomware-as-a-Service").

#### Vulnérabilités critiques identifiées
*   **CVE-2026-42589 :** RCE dans Gotenberg (CVSS 9.8), activement exploitée pour déployer des reverse shells.
*   **CVE-2026-80097 (AuthMask) :** Faille dans Microsoft Authenticator permettant le vol de jetons d'accès via des applications Android malveillantes.
*   **CVE-2026-93348 :** RCE dans le chargeur de modèles d'Unsloth, permettant l'exécution de code arbitraire lors du chargement de configurations.
*   **CVE-2025-70795 :** Pilote vulnérable (Safetica) utilisé par le ransomware "The Gentlemen" pour neutraliser les solutions de sécurité (EDR).
*   **PHP2Shell (CVE-2026-109618 / CVE-2026-109619) :** Tentatives d'exploitation massives détectées sur WordPress, bien qu'aucune compromission confirmée n'ait été rapportée à ce jour.

#### Recommandations stratégiques
1.  **Gestion stricte des secrets :** Auditer régulièrement les dépôts de code publics et privés pour éviter l'exposition de clés API, de mots de passe ou de jetons d'accès.
2.  **Sécurité de l'IA :** Interdire le partage de données sensibles (identifiants, documents confidentiels) avec des outils d'IA générative tiers.
3.  **Renforcement des accès :** Appliquer les correctifs de sécurité sans délai, particulièrement sur les équipements réseau (Fortinet) et les services exposés (Gotenberg).
4.  **Limitation des privilèges :** Adopter des politiques de permissions granulaires sur mobile (notamment pour l'accès aux contacts) et surveiller les outils de gestion de périphériques (MDM).
5.  **Vigilance sur les fichiers :** Se méfier des PDF contenant des objets `/OpenAction` ou `/Launch` utilisés comme vecteurs d'infection initiale.

---
[Source](https://thehackernews.com/2026/10/threatsday-critical-firewall-flaws.html){:target="_blank"}
