---
title: 'GreyVibe hackers use ChatGPT, Gemini to power cyberattacks'
date: 2026-05-29
permalink: /posts/2026/05/29/greyvibe-hackers-use-chatgpt-gemini-to-power-cyberattacks/
tags:
- veille-cyber
- bleepingcomp
---
### GreyVibe : L’IA au service de campagnes d'espionnage hybrides

Le groupe de cybermenaces **GreyVibe**, actif depuis août 2025 et aligné sur les intérêts russes, cible prioritairement les secteurs militaire, gouvernemental et civil en Ukraine. Ce groupe se distingue par l'utilisation intensive d'outils d'intelligence artificielle générative (ChatGPT, Gemini, Ideogram) pour concevoir des leurres sophistiqués et automatiser le développement de malwares personnalisés.

#### Points clés
*   **Nature hybride :** Le groupe mélange des techniques d'espionnage étatique et des pratiques cybercriminelles (utilisation d'un mineur de cryptomonnaie, manque de discipline opérationnelle, liens possibles avec d'anciens membres du groupe TrickBot).
*   **Stratégies d'attaque diversifiées :** Utilisation de sites de rencontres frauduleux, de fausses pages de CAPTCHA (Cloudflare), de leurres imitant le matériel militaire (drones FPV) et de communications factices liées à des terminaux militaires.
*   **Outils automatisés :** Emploi d'obfuscateurs personnalisés (LOOKVALPS, DAYLIGHT, etc.) et de RAT (Remote Access Trojans) développés avec l'aide d'IA.

#### Vulnérabilités exploitées
L'article ne mentionne pas de CVE spécifiques, car les vecteurs d'attaque reposent principalement sur l'ingénierie sociale et l'exécution de scripts malveillants :
*   **Phishing et téléchargements malveillants :** Utilisation d'archives piégées (.zip/.rar) via Google Drive ou 4sync.
*   **Technique "ClickFix" :** Manipulation des victimes via de fausses vérifications de sécurité pour exécuter des commandes malveillantes.
*   **Accès à distance :** Exploitation de PowerShell pour le déploiement de RAT (LegionRelay, PhantomRelay) permettant l'exfiltration de données, la capture d'écran et la prise de contrôle via RDP.

#### Malwares identifiés
*   **LegionRelay & PhantomRelay :** RAT PowerShell pour le vol de données et l'espionnage.
*   **FallSpy :** Spyware Android pour la collecte massive d'informations (appels, géolocalisation, contacts).

#### Recommandations
*   **Surveillance des IoC :** Intégrer les indicateurs de compromission (IoC) fournis par WithSecure dans les solutions de sécurité (disponibles sur leur GitHub officiel).
*   **Sensibilisation :** Former les utilisateurs à la méfiance face aux sites de recrutement ou d'information militaires non officiels et aux fausses pages de vérification "CAPTCHA".
*   **Filtrage :** Renforcer les politiques de filtrage des emails et limiter l'exécution de scripts PowerShell non autorisés dans les environnements critiques.

---
[Source](https://www.bleepingcomputer.com/news/security/greyvibe-hackers-use-chatgpt-gemini-to-power-cyberattacks/){:target="_blank"}
