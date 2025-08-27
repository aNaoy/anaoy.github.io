---
title: 'ShadowSilk Hits 35 Organizations in Central Asia and APAC Using Telegram Bots'
date: 2025-08-27
permalink: /posts/2025/08/27/shadowsilk-hits-35-organizations-in-central-asia-and-apac-using-telegram-bots/
tags:
- veille-cyber
- hackernews
---
**ShadowSilk : Une menace persistante ciblant l'Asie Centrale et l'APAC**

Une campagne de cybersécurité, baptisée ShadowSilk, cible activement des organisations gouvernementales en Asie Centrale et dans la région Asie-Pacifique (APAC), ainsi que des entités dans les secteurs de l'énergie, de la fabrication, du commerce de détail et des transports. Près de trente-cinq victimes ont été identifiées, notamment en Ouzbékistan, au Kirghizistan, au Myanmar, au Tadjikistan, au Pakistan et au Turkménistan.

Cette menace affiche des liens avec les groupes YoroTrooper, SturgeonPhisher et Silent Lynx, suggérant une possible collaboration entre des développeurs russophones et des opérateurs sinophones. L'objectif principal de ces intrusions est l'exfiltration de données.

L'exploitation de vulnérabilités publiques dans Drupal (CVE-2018-7600, CVE-2018-76020) et le plugin WordPress WP-Automatic (CVE-2024-27956) a été observée. ShadowSilk utilise également un ensemble d'outils incluant des techniques de reconnaissance et de test d'intrusion comme FOFA, Fscan, Gobuster, Dirsearch, Metasploit et Cobalt Strike. L'arsenal s'enrichit de panels web issus du darknet (JRAT, Morf Project) pour la gestion des appareils compromis et d'un outil sur mesure pour voler les identifiants de connexion du navigateur Chrome. Les attaquants n'hésitent pas à compromettre des sites web légitimes pour héberger leurs charges utiles malveillantes.

Pour maintenir leur présence, les acteurs de la menace modifient le registre Windows afin d'assurer l'exécution automatique des malwares après redémarrage. L'accès initial s'effectue généralement par le biais d'e-mails d'hameçonnage ciblé, délivrant des archives protégées par mot de passe contenant un chargeur personnalisé. Ce dernier masque le trafic de commande et de contrôle (C2) derrière des bots Telegram, rendant la détection plus difficile. Une fois à l'intérieur d'un réseau, ShadowSilk déploie des web shells (ANTSWORD, Behinder, Godzilla, FinalShell), des outils post-exploitation basés sur Sharp, et des utilitaires de tunneling (Resocks, Chisel) pour le déplacement latéral, l'escalade de privilèges et l'exfiltration de données. Un cheval de Troie d'accès à distance (RAT) basé sur Python est également utilisé pour recevoir des commandes et exfiltrer des données via des bots Telegram, déguisant ainsi l'activité malveillante en communication légitime. Des modules Cobalt Strike et Metasploit sont employés pour capturer des captures d'écran et des images de webcam. Un script PowerShell personnalisé scanne des fichiers selon une liste d'extensions prédéfinie, les archive puis les transfère vers un serveur externe.

**Points clés :**

*   **Cible :** Organisations gouvernementales, secteurs de l'énergie, fabrication, commerce de détail, transport en Asie Centrale et APAC.
*   **Victimes notables :** Ouzbékistan, Kirghizistan, Myanmar, Tadjikistan, Pakistan, Turkménistan.
*   **Objectif principal :** Exfiltration de données.
*   **Méthodes d'accès initial :** E-mails d'hameçonnage ciblé.
*   **Techniques de persistance :** Modification du registre Windows.
*   **Communication C2 :** Bots Telegram.
*   **Outils utilisés :** Chargeur personnalisé, web shells (ANTSWORD, Behinder, Godzilla, FinalShell), outils Sharp, utilitaires de tunneling (Resocks, Chisel), JRAT, Morf Project, outil de vol de mots de passe Chrome.
*   **Liens avec d'autres groupes :** YoroTrooper, SturgeonPhisher, Silent Lynx.
*   **Langues utilisées par les attaquants :** Russe et Chinois.

**Vulnérabilités exploitées :**

*   Drupal : CVE-2018-7600, CVE-2018-76020
*   Plugin WordPress WP-Automatic : CVE-2024-27956

**Recommandations (implicites dans la description des techniques) :**

*   Renforcer la sécurité des e-mails et la sensibilisation des utilisateurs à l'hameçonnage.
*   Appliquer les correctifs de sécurité pour les logiciels, notamment Drupal et les plugins WordPress.
*   Surveiller et sécuriser les configurations du registre Windows.
*   Mettre en place des solutions de sécurité réseau capables de détecter les communications C2 suspectes, y compris celles utilisant des plateformes de messagerie populaires.
*   Effectuer des audits de sécurité réguliers et des tests de pénétration pour identifier et corriger les vulnérabilités.
*   Surveiller activement l'infrastructure réseau et les journaux d'événements pour détecter toute activité suspecte.
*   Sécuriser les informations d'identification des utilisateurs, y compris celles stockées dans les navigateurs.

---
[Source](https://thehackernews.com/2025/08/shadowsilk-hits-36-government-targets.html){:target="_blank"}
