---
title: 'WIRTE Leverages AshenLoader Sideloading to Install the AshTag Espionage Backdoor'
date: 2025-12-11
permalink: /posts/2025/12/11/wirte-leverages-ashenloader-sideloading-to-install-the-ashtag-espionage-backdoor/
tags:
- veille-cyber
- hackernews
---
### Les activités d'espionnage du groupe WIRTE

Le groupe cybercriminel avancé et persistant (APT) WIRTE, également connu sous le nom d'Ashen Lepus, cible des entités gouvernementales et diplomatiques au Moyen-Orient depuis au moins 2018. Ses activités, qui se recoupent avec celles du groupe Gaza Cyber Gang (affilié au Hamas), sont axées sur l'espionnage et la collecte d'informations.

La campagne d'attaque récente utilise une nouvelle suite logicielle malveillante appelée AshTag. Celle-ci est déployée via des e-mails de phishing contenant des documents leurres, souvent liés à des affaires géopolitiques régionales. Ces emails incitent les victimes à télécharger une archive qui, une fois ouverte, exploite une technique de "sideloading" (chargement latéral) pour installer AshTag. Le processus implique le chargement d'une DLL malveillante (AshenLoader) par un binaire légitime renommé. Cette DLL contacte ensuite un serveur externe pour télécharger et exécuter d'autres composants, dont un chargeur (AshenStager) qui lance le backdoor AshTag en mémoire vive, rendant sa détection plus difficile.

AshTag est un backdoor modulaire .NET conçu pour assurer la persistance, exécuter des commandes à distance et se dissimuler sous l'apparence d'un utilitaire légitime (VisualServer). Il est géré par un orchestrateur (AshenOrchestrator) et peut télécharger des modules supplémentaires pour diverses fonctions, telles que la capture d'écran, l'exploration de fichiers, ou la collecte d'informations système.

Le groupe a été observé exfiltrant des documents sensibles, notamment des informations diplomatiques, à l'aide d'outils comme Rclone. L'activité de WIRTE est restée soutenue, y compris pendant des périodes de conflit régional, démontrant une intention continue de collecte de renseignements.

**Points clés:**

*   **Acteur:** WIRTE (Ashen Lepus), groupe lié au Hamas.
*   **Cibles:** Entités gouvernementales et diplomatiques au Moyen-Orient (historiquement Palestine, Jordanie, Irak, Arabie Saoudite, Égypte; plus récemment Oman et Maroc).
*   **Objectif principal:** Espionnage et collecte de renseignements.
*   **Méthode d'infection initiale:** E-mails de phishing avec des leurres géopolitiques.
*   **Malware principal:** AshTag (backdoor modulaire .NET).
*   **Technique d'installation:** Chargement latéral (sideloading) via AshenLoader et AshenStager.
*   **Fonctionnalités d'AshTag:** Persistance, exécution de commandes, collecte de données, capture d'écran, exploration de fichiers.
*   **Exfiltration de données:** Utilisation d'outils comme Rclone.
*   **Persistance:** Le groupe est resté actif même pendant les conflits régionaux.

**Vulnérabilités (non spécifiées par CVE dans l'article):**

L'article ne mentionne pas de vulnérabilités spécifiques exploitées par des numéros CVE. L'infection semble se produire par le biais d'ingénierie sociale (phishing) et d'un mécanisme de chargement latéral de DLL qui exploite le fonctionnement normal des applications Windows pour exécuter du code malveillant.

**Recommandations (implicites basées sur les méthodes d'attaque):**

*   **Sensibilisation à la sécurité:** Former les utilisateurs à reconnaître et signaler les e-mails de phishing suspects.
*   **Prudence avec les téléchargements:** Être extrêmement prudent lors de l'ouverture d'archives ou de l'exécution de fichiers provenant de sources non fiables.
*   **Surveillance du réseau:** Mettre en place une surveillance pour détecter les communications suspectes avec des serveurs externes ou l'utilisation d'outils d'exfiltration comme Rclone.
*   **Gestion des logiciels:** Maintenir à jour les systèmes d'exploitation et les logiciels, bien que l'article ne détaille pas d'exploitation de vulnérabilités logicielles connues.
*   **Protection des points d'extrémité:** Utiliser des solutions de sécurité robustes qui peuvent détecter les comportements malveillants et le chargement latéral de DLL.

---
[Source](https://thehackernews.com/2025/12/wirte-leverages-ashenloader-sideloading.html){:target="_blank"}
