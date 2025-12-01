---
title: '⚡ Weekly Recap: Hot CVEs, npm Worm Returns, Firefox RCE, M365 Email Raid & More'
date: 2025-12-01
permalink: /posts/2025/12/01/weekly-recap-hot-cves-npm-worm-returns-firefox-rce-m365-email-raid-more/
tags:
- veille-cyber
- hackernews
---
**Alertes de Sécurité Numérique : Menaces Répandues et Vulnérabilités Émergentes**

Les cyberattaquants exploitent de plus en plus les outils et les canaux du quotidien pour compromettre les systèmes. Des vers auto-répliquants sur les dépôts de code aux vulnérabilités dans les plateformes de collaboration, la surface d'attaque s'élargit.

**Points Clés et Vulnérabilités :**

*   **Ver npm "Shai-Hulud" :** Une deuxième vague de ce ver auto-répliquant a ciblé le registre npm, affectant plus de 800 packages et 27 000 dépôts GitHub. Son objectif principal est le vol de données sensibles (clés API, identifiants cloud, informations d'authentification npm/GitHub) et la compromission de la chaîne d'approvisionnement. Il utilise le runtime Bun pour exécuter des charges utiles importantes avec plus de discrétion et crée des flux de travail GitHub Actions pour le contrôle et le vol de secrets. L'incident a conduit au vol d'identifiants et à un accès non autorisé à des organisations GitHub.
*   **ToddyCat :** Cet outil d'APT évolue pour voler des données d'e-mails Outlook et des jetons d'accès Microsoft 365. Il capture également des identifiants de navigateur et des archives d'e-mails.
*   **Ransomware Qilin :** Une attaque par la chaîne d'approvisionnement a utilisé un fournisseur de services gérés (MSP) compromis pour déployer le ransomware Qilin sur des dizaines d'entreprises financières en Corée du Sud. Plus d'un million de fichiers ont été volés.
*   **Campagnes d'Espionnage :** La CISA alerte sur l'utilisation active de logiciels espions commerciaux et de chevaux de Troie d'accès à distance (RAT) ciblant des utilisateurs d'applications de messagerie mobile via l'ingénierie sociale. Les cibles principales sont des hauts responsables gouvernementaux et militaires, ainsi que des organisations de la société civile.
*   **Exploitation d'une faille WSUS :** Une faille récemment corrigée dans Microsoft Windows Server Update Services (CVE-2025-59287) a été exploitée pour distribuer le malware ShadowPad.
*   **Faille dans Microsoft Teams Guest Access :** Une vulnérabilité d'architecture fondamentale permet aux attaquants de contourner les protections de Microsoft Defender for Office 365 grâce à la fonctionnalité d'accès invité dans Teams. La protection d'un utilisateur invité dépend de l'environnement d'hébergement, et non de son organisation d'origine.
*   **Vulnérabilités Fluentes :** Plusieurs failles ont été identifiées dans Fluent Bit (CVE-2025-12972, CVE-2025-12970, CVE-2025-12978, CVE-2025-12977, CVE-2025-12969), exposant le cloud.
*   **Failles Tenda :** Vulnérabilités identifiées dans les équipements Tenda (CVE-2025-13207, CVE-2024-24481).
*   **Vulnérabilité vLLM :** La bibliothèque vLLM présente une vulnérabilité critique (CVE-2025-62164).
*   **Failles ASUS :** Des vulnérabilités ont été découvertes dans l'application MyASUS (CVE-2025-59373) et les routeurs ASUS (CVE-2025-59366).
*   **Faille Apache Syncope :** Vulnérabilité dans Apache Syncope (CVE-2025-65998).
*   **Vulnérabilité HashiCorp Vault Terraform Provider :** Une faille dans le fournisseur Terraform de HashiCorp Vault (CVE-2025-13357).
*   **Vulnérabilités NVIDIA :** Plusieurs failles dans NVIDIA Isaac-GR00T (CVE-2025-33183, CVE-2025-33184) et NVIDIA DGX Spark (CVE-2025-33187).
*   **Vulnérabilités GitLab :** Des failles ont été signalées dans GitLab CE/EE (CVE-2025-12571, CVE-2024-9183).
*   **Vulnérabilité Angular HttpClient :** Une faille a été découverte dans le module HttpClient d'Angular (CVE-2025-66035).
*   **Vulnérabilité Next.js :** Une vulnérabilité de déni de service (DoS) non authentifiée a été signalée dans Next.js (sans CVE).
*   **Compromission de Réseaux de Diffusion :** La FCC met en garde les diffuseurs contre la sécurisation de leurs réseaux, suite à des cyberattaques ayant conduit à la diffusion de contenus obscènes via des liaisons studio-émetteur compromises.
*   **Exécution de Code à Distance dans Firefox :** Une vulnérabilité de haut niveau dans le moteur WebAssembly de Firefox (CVE-2025-13016) permet l'exécution de code arbitraire à distance.
*   **Démantèlement de Cryptomixer :** Une opération internationale a permis de démanteler Cryptomixer, un service de mélange de cryptomonnaies soupçonné de faciliter la cybercriminalité et le blanchiment d'argent. Plus de 12 téraoctets de données et 25 millions d'euros en Bitcoin ont été saisis.
*   **Manuels de Piratage Nord-Coréens :** Un homme a été condamné en Corée du Sud pour avoir acheté des outils de piratage auprès d'acteurs nord-coréens.
*   **Usage Malveillant d'IA :** Une campagne cybercriminelle automatisée exploitait les plateformes d'IA pour automatiser des cyberattaques, masquant ainsi une large gamme d'activités illégales.
*   **Jeux Fictifs pour Propager des Malwares :** Des acteurs malveillants utilisent des versions piratées de jeux populaires comme Battlefield 6 pour distribuer des malwares voleurs d'informations et des agents de commande et contrôle (C2).
*   **Collaboration d'Acteurs Étatiques :** Des chevauchements d'infrastructure ont été observés entre des groupes liés à la Corée du Nord (Lazarus Group, Kimsuky) et d'autres acteurs étatiques, suggérant une collaboration accrue.
*   **Robustesse des Modèles d'IA :** Anthropic affirme que son modèle Claude Opus 4.5 est plus résistant aux attaques par injection de prompt que d'autres modèles avancés.
*   **Failles dans les Cadres Photo Numériques Uhale :** De multiples failles critiques ont été découvertes dans les cadres photo numériques Uhale basés sur Android, permettant potentiellement un contrôle total des appareils. La plupart ont été corrigées dans la version 4.2.1 de l'application Uhale.
*   **Exploitation de la Vulnérabilité ZipperDown :** Des acteurs étatiques auraient exploité la vulnérabilité ZipperDown pour cibler des appareils mobiles en Chine dans le cadre de l'Opération South Star.
*   **LLM Malveillants :** Des modèles linguistiques de grande taille (LLM) malveillants tels que WormGPT 4, KawaiiGPT et Xanthorox sont commercialisés pour générer des e-mails de phishing, écrire des malwares polymorphes et automatiser la reconnaissance, en contournant les contraintes éthiques. L'utilisation de ces outils non restreints abaisse le seuil d'entrée pour les acteurs moins qualifiés.

**Recommandations Générales :**

*   **Surveillance Continuelle :** Les outils de sécurité doivent être constamment mis à jour et les vulnérabilités corrigées rapidement, car les attaquants agissent rapidement.
*   **Sécurité de la Chaîne d'Approvisionnement :** Examiner attentivement les dépendances logicielles et les partenaires pour identifier et atténuer les risques potentiels.
*   **Gestion des Identifiants :** Renforcer la gestion des identifiants, y compris les jetons d'accès, et les révoquer régulièrement.
*   **Contrôle d'Accès :** Examiner et resserrer les permissions d'accès, en particulier pour les comptes invités et les accès externes.
*   **Sensibilisation et Formation :** Former les utilisateurs aux techniques d'ingénierie sociale et à l'importance de la prudence lors du téléchargement ou de l'exécution de fichiers.
*   **Mise à Jour des Logiciels :** Appliquer rapidement les correctifs de sécurité pour tous les logiciels et systèmes.
*   **Analyse des Risques :** Évaluer régulièrement les risques liés aux outils et plateformes utilisés, en particulier ceux qui ont des fonctionnalités d'accès invité ou d'intégration de tiers.

---
[Source](https://thehackernews.com/2025/12/weekly-recap-hot-cves-npm-worm-returns.html){:target="_blank"}
