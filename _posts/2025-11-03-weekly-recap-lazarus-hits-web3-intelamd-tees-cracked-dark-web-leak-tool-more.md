---
title: '⚡ Weekly Recap: Lazarus Hits Web3, Intel/AMD TEEs Cracked, Dark Web Leak Tool & More'
date: 2025-11-03
permalink: /posts/2025/11/03/weekly-recap-lazarus-hits-web3-intelamd-tees-cracked-dark-web-leak-tool-more/
tags:
- veille-cyber
- hackernews
---
## Tendances de la Cybersécurité : Attaques sophistiquées et nouvelles vulnérabilités

La scène de la cybersécurité continue d'évoluer rapidement, avec des acteurs malveillants employant des tactiques de plus en plus avancées pour exploiter les vulnérabilités. Cette semaine a vu des menaces toucher divers secteurs, des environnements Web3 aux systèmes matériels de confiance, en passant par les infrastructures critiques et les appareils mobiles.

**Points Clés :**

*   **Sophistication des Attaques :** Les cybercriminels utilisent des techniques furtives, exploitent des failles logicielles rapidement après leur découverte, et détournent des outils légitimes ("living-off-the-land") pour masquer leurs activités.
*   **Ciblage Diversifié :** Les attaques visent un large éventail de cibles, incluant les secteurs Web3, les entreprises, les gouvernements, et même les particuliers via des escroqueries ciblées.
*   **Importance de la Réduction de la Surface d'Attaque :** Il est souligné que les menaces peuvent provenir de ce qui est déjà présent dans un système, rendant la gestion de la surface d'attaque plus cruciale que jamais.

**Vulnérabilités Notables (avec CVE si possible) :**

*   **Motex Lanscope Endpoint Manager :** CVE-2025-61932 (score CVSS 9.3) exploitée pour déployer le backdoor Gokcpdoor par le groupe Tick.
*   **Intel et AMD TEEs (Trusted Execution Environments) :** Attaque par canal auxiliaire "TEE.Fail" capable d'extraire des secrets et de contourner les mécanismes de sécurité de SGX, TDX (Intel) et SEV-SNP (AMD). Nécessite un accès physique et des privilèges root.
*   **Apache ActiveMQ :** CVE-2023-46604 exploitée par le groupe Kinsing pour des attaques de cryptojacking.
*   **LUKS2 Disk Encryption (utilisé dans plusieurs systèmes de calcul confidentiel) :** CVE-2025-59054 et CVE-2025-58356, permettant l'extraction et la modification de données confidentielles sur des disques chiffrés, nécessitant un accès en écriture aux disques.
*   **QNAP NetBak PC Agent :** CVE-2025-55315.
*   **OpenVPN :** CVE-2025-10680.
*   **Apache Tomcat :** CVE-2025-55752, CVE-2025-55754.
*   **Ubiquiti UniFi Access :** CVE-2025-52665.
*   **HashiCorp Vault :** CVE-2025-12044, CVE-2025-11621.
*   **Dell Storage Manager :** CVE-2025-43995.
*   **Veeder-Root TLS4B Automatic Tank Gauge System :** CVE-2025-5842.
*   **XWiki :** CVE-2025-24893.
*   **Docker Compose :** CVE-2025-62725.
*   **Google Messages for Wear OS :** CVE-2025-12080.
*   **LiteSpeed Cache plugin :** CVE-2025-12450.
*   **Anti-Malware Security and Brute-Force Firewall plugin (WordPress) :** CVE-2025-11705.
*   **Microsoft Windows Cloud Files Minifilter driver :** CVE-2025-55680.
*   **King Addons for Elementor plugin (WordPress) :** CVE-2025-6325, CVE-2025-6327.
*   **Quiz and Survey Master plugin (WordPress) :** CVE-2025-49401.
*   **Claroty Secure Remote Access :** CVE-2025-54603.
*   **Progress MOVEit Transfer :** CVE-2025-10932.

**Recommandations :**

*   **Surveillance Active et Réduction de la Surface d'Attaque :** Utiliser des outils pour cartographier et réduire activement les expositions en ligne (EasyEASM, Microsoft Attack Surface Analyzer, ASRGEN).
*   **Mises à Jour Régulières :** Appliquer rapidement les correctifs pour les vulnérabilités découvertes, car les exploitants agissent vite.
*   **Protection des Environnements Sensibles :** Renforcer la sécurité des TEEs et des systèmes critiques, en étant conscient des attaques par canal auxiliaire.
*   **Vigilance face au Phishing et à l'Ingénierie Sociale :** Être attentif aux fausses offres d'emploi, aux invitations de réunion trompeuses, et aux leurres de type "ClickFix" ou reçus de virements bancaires frauduleux, même s'ils proviennent de plateformes comme LinkedIn.
*   **Sécurisation des Outils de Développement :** Examiner attentivement les extensions VS Code et les paquets npm pour détecter les logiciels malveillants cachés.
*   **Diversification des Méthodes d'Authentification :** Adopter des solutions comme les passkeys pour sécuriser les sauvegardes chiffrées (ex: WhatsApp).
*   **Utilisation d'Outils de Sécurité Spécialisés :** Considérer des outils comme runZeroHound pour visualiser les chemins d'attaque potentiels dans le réseau, et DroidRun pour l'analyse de malware Android en sandbox.
*   **Application des Stratégies de Détection :** Se référer aux mises à jour du framework MITRE ATT&CK pour améliorer les capacités de détection.

---
[Source](https://thehackernews.com/2025/11/weekly-recap-lazarus-hits-web3-intelamd.html){:target="_blank"}
