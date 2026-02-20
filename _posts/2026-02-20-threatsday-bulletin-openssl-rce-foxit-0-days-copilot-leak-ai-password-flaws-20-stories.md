---
title: 'ThreatsDay Bulletin: OpenSSL RCE, Foxit 0-Days, Copilot Leak, AI Password Flaws & 20+ Stories'
date: 2026-02-20
permalink: /posts/2026/02/20/threatsday-bulletin-openssl-rce-foxit-0-days-copilot-leak-ai-password-flaws-20-stories/
tags:
- veille-cyber
- hackernews
---
## Point d'Actu Cybersécurité : Évolutions des Menaces et Vulnérabilités

Les menaces cybernétiques continuent d'évoluer à un rythme rapide, impactant diverses plateformes et industries. Les nouvelles tactiques des attaquants et l'apparition de nouvelles vulnérabilités exigent une vigilance constante de la part des défenseurs.

### Points Clés :

*   **Android 17** introduit des améliorations de confidentialité avec la dépréciation de `usesCleartextTraffic` et le support de la cryptographie hybride HPKE pour des communications sécurisées.
*   **LockBit 5.0** étend sa portée aux systèmes Linux et ESXi, démontrant des techniques avancées d'évasion de défense.
*   La tactique d'ingénierie sociale **ClickFix** évolue pour cibler les utilisateurs macOS via des couches d'obfuscation imbriquées et des attaques par typosquatting.
*   Le **ransomware industriel** est en forte augmentation, ciblant particulièrement les secteurs de la fabrication et du transport.
*   L'utilisation abusive de **logiciels de gestion et de surveillance à distance (RMM)** a connu une explosion, représentant une part significative des incidents.
*   Des **véhicules chinois** sont interdits d'entrée sur les bases militaires polonaises par mesure de sécurité nationale.
*   Des attaques par **DKIM replay** exploitent des factures et notifications légitimes pour contourner la sécurité email.
*   Des **campagnes de phishing ciblent les entreprises du Fortune 500** via des bots Telegram pour voler des identifiants.
*   Des **logiciels d'entraînement à la sécurité mal configurés** exposent des vulnérabilités dans le cloud.
*   Les **mots de passe générés par IA** présentent des faiblesses intrinsèques dues à leur nature prédictive.

### Vulnérabilités Identifiées :

*   **CVE-2025-15467 (OpenSSL)** : Vulnérabilité de dépassement de tampon dans le traitement des données CMS, permettant l'exécution de code à distance sous certaines conditions.
*   **CVE-2025-11187 (OpenSSL)** : Vulnérabilité de dépassement de tampon basée sur la pile due à un manque de validation.
*   **CVE-2021-22175 (GitLab)** : Vulnérabilité de Server-Side Request Forgery (SSRF) permettant l'accès au réseau interne lors de la configuration des webhooks.
*   **CVE-2026-1281 et CVE-2026-1340 (Ivanti Endpoint Manager Mobile - EPMM)** : Vulnérabilités critiques permettant l'exécution de code à distance par des attaquants non authentifiés.
*   **CVE-2025-70401, CVE-2025-70402, CVE-2025-66500 (Foxit / Apryse PDF engines)** : Vulnérabilités dans le traitement des entrées non fiables, pouvant mener à la prise de contrôle de compte, au vol de données et à l'exécution de JavaScript arbitraire.

### Recommandations :

*   **Mettre à jour les applications et les systèmes** : Appliquer les correctifs dès qu'ils sont disponibles, notamment pour OpenSSL, GitLab, Ivanti EPMM et les moteurs PDF Foxit/Apryse.
*   **Renforcer la sécurité des communications** : Migrer vers des configurations réseau sécurisées et envisager des solutions comme la cryptographie hybride pour les applications critiques.
*   **Être vigilant face aux techniques d'ingénierie sociale** : Se méfier des liens suspects, des demandes d'informations inattendues et des installateurs provenant de sources non fiables, en particulier sur macOS.
*   **Sécuriser les environnements industriels (OT/ICS)** : Mettre en œuvre des mesures de sécurité robustes pour protéger les systèmes de contrôle industriel contre les attaques par ransomware.
*   **Revoir l'utilisation des RMM** : S'assurer que l'utilisation des logiciels RMM est correctement configurée et surveillée pour détecter toute activité malveillante.
*   **Évaluer la fiabilité des outils IA** : Ne pas utiliser les grands modèles de langage (LLM) pour générer des mots de passe ; privilégier les méthodes de génération sécurisées et éprouvées.
*   **Renforcer la sécurité des comptes machines** : Appliquer le principe de moindre privilège et désactiver la délégation pour les comptes machines sensibles afin de limiter le risque d'escalade de privilèges.
*   **Surveiller activement les journaux et les indicateurs de compromission** : Maintenir une surveillance continue des systèmes pour détecter toute exploitation ou activité suspecte, même sur des périodes anciennes.

---
[Source](https://thehackernews.com/2026/02/threatsday-bulletin-openssl-rce-foxit-0.html){:target="_blank"}
