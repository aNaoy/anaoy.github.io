---
title: 'IT threat evolution in Q3 2025. Non-mobile statistics'
date: 2025-11-19
permalink: /posts/2025/11/19/it-threat-evolution-in-q3-2025-non-mobile-statistics/
tags:
- veille-cyber
- securelist
---
## Évolution des menaces informatiques au T3 2025 : Un panorama des attaques

Le troisième trimestre 2025 a vu une intensification des cyberattaques, avec des millions d'incidents bloqués par les solutions de sécurité. Les ransomwares restent une menace majeure, tandis que les logiciels malveillants ciblant les appareils IoT et macOS continuent d'évoluer.

**Chiffres clés :**

*   Plus de 389 millions d'attaques bloquées par des ressources en ligne.
*   52 millions de liens uniques détectés comme malveillants par le Web Anti-Virus.
*   Plus de 21 millions d'objets malveillants ou potentiellement indésirables bloqués par le File Anti-Virus.
*   2 200 nouvelles variantes de ransomwares identifiées.
*   Près de 85 000 utilisateurs ont subi des attaques de ransomwares.
*   15% des victimes de ransomwares dont les données ont été publiées étaient liées au groupe Qilin.
*   Plus de 254 000 utilisateurs ciblés par des mineurs de cryptomonnaies.

**Points clés et vulnérabilités :**

*   **Ransomware :**
    *   Les forces de l'ordre ont mené des actions significatives, incluant des arrestations et des saisies de fonds liés à des groupes comme HardBit, LockerGoga, MegaCortex, Nefilim et Zeppelin. Une opération internationale a démantelé l'infrastructure du ransomware BlackSuit.
    *   **Vulnérabilités exploitées :**
        *   CVE-2024-40766 : Permet un accès non autorisé aux VPN SSL SonicWall, même après application de correctifs, permettant le vol d'identifiants et le contournement de l'authentification multifacteur.
        *   Exploitation de la chaîne de vulnérabilités ToolShell sur les serveurs Microsoft SharePoint, menant à la découverte du ransomware 4L4MD4R.
    *   **Intelligence Artificielle dans le développement de ransomwares :** Des acteurs malveillants utilisent des IA comme Claude pour créer des plateformes Ransomware-as-a-Service (RaaS). PromptLock, un nouveau ransomware, utilise un LLM pour générer dynamiquement des scripts Lua pour le vol de données et le chiffrement.

*   **Attaques sur VMware :** Le groupe Scattered Spider (UNC3944) cible les environnements virtuels VMware en se faisant passer pour des employés pour réinitialiser les mots de passe Active Directory, puis déploie des ransomwares.

*   **Attaques sur macOS :** L'activité du spyware PasivRobber a augmenté. De fausses extensions pour l'environnement de développement Cursor AI ont été utilisées pour distribuer des cryptostealers et des backdoors, notamment via des charges utiles Rust. Le backdoor modulaire ChillyHell, signé avec un certificat valide, a été observé. Les nouvelles versions du spyware XCSSET, qui cible les développeurs, intègrent des modules pour le vol de données et la persistance.

*   **Menaces IoT :** Les attaques via le protocole SSH ont légèrement augmenté, tandis que celles utilisant Telnet sont restées dominantes, principalement depuis la Chine. Les botnets Mirai et Gafgyt sont les plus actifs.

*   **Attaques via Web Ressources :** Panama, le Bangladesh et le Tadjikistan figurent parmi les pays les plus exposés aux infections par des malwares via le web.

*   **Menaces Locales :** Le Turkménistan, le Yémen et l'Afghanistan présentent les risques les plus élevés d'infection locale, souvent liés à des objets malveillants présents sur des fichiers ou des supports amovibles.

**Recommandations :**

*   **Mise à jour des systèmes :** Appliquer les correctifs de sécurité, notamment pour les VPN SSL SonicWall (réinitialisation des mots de passe et mise à jour du firmware SonicOS recommandée).
*   **Renforcement de la sécurité des accès :** Utiliser des mots de passe forts et l'authentification multifacteur.
*   **Vigilance accrue :** Être attentif aux emails suspects, aux extensions malveillantes et aux fausses demandes de support technique.
*   **Sécurisation des environnements virtuels :** Mettre en place des mesures de sécurité spécifiques pour les environnements VMware.
*   **Protection des appareils IoT :** Sécuriser les appareils connectés et surveiller les activités suspectes.
*   **Sensibilisation aux risques :** Éduquer les utilisateurs sur les dangers des attaques par phishing, des téléchargements malveillants et des supports amovibles infectés.
*   **Surveillance des vulnérabilités :** Suivre les annonces de vulnérabilités et appliquer les correctifs rapidement.

Ces données soulignent la complexité croissante du paysage des menaces et la nécessité d'une approche de sécurité multicouche et proactive.

---
[Source](https://securelist.com/malware-report-q3-2025-pc-iot-statistics/118020/){:target="_blank"}
