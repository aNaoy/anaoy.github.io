---
title: 'Google Links China, Iran, Russia, North Korea to Coordinated Defense Sector Cyber Operations'
date: 2026-02-13
permalink: /posts/2026/02/13/google-links-china-iran-russia-north-korea-to-coordinated-defense-sector-cyber-operations/
tags:
- veille-cyber
- hackernews
---
### Cybersécurité : Le Secteur de la Défense Sous la Lorgnette d'Acteurs Étatiques

Des acteurs malveillants parrainés par les États de Chine, d'Iran, de Corée du Nord et de Russie ciblent de manière coordonnée le secteur industriel de la défense. Ces opérations visent principalement les entités impliquées dans la guerre russo-ukrainienne, exploitent les processus de recrutement, utilisent des appareils connectés comme points d'entrée et exploitent les risques liés à la chaîne d'approvisionnement.

**Points Clés :**

*   **Ciblage par État :** La Chine, l'Iran, la Corée du Nord et la Russie sont identifiés comme parrains d'activités cybernétiques hostiles.
*   **Thèmes Principaux :** L'accent est mis sur les technologies de défense utilisées dans le conflit ukrainien, la compromission du personnel par l'exploitation des offres d'emploi, l'usage d'appareils connectés pour l'accès initial et l'exploitation des failles dans la chaîne de production.
*   **Évasion des Détections :** Les attaquants privilégient les cibles individuelles et les méthodes qui contournent les outils de détection et de réponse aux points d'extrémité (EDR).
*   **Drones et Véhicules Autonomes :** L'intérêt pour ces technologies militaires en pleine évolution est une motivation majeure.
*   **Réseaux Relais (ORB) :** Des groupes liés à la Chine utilisent ces réseaux pour la reconnaissance, complexifiant l'attribution.

**Vulnérabilités et Tactiques Mentionnées (sans CVE spécifiques dans l'article) :**

*   **APT44 (Sandworm) :** Exfiltration de données chiffrées (Signal, Telegram) via des scripts (ex: WAVESIGN).
*   **TEMP.Vermin (UAC-0020) :** Utilisation de malwares (VERMONSTER, SPECTRUM, FIRMACHAGENT) avec des contenus leurres sur la production de drones et la sécurité vidéo.
*   **UNC5125 (FlyingYeti) :**
    *   Utilisation de formulaires Google pour le renseignement sur les opérateurs de drones.
    *   Distribution de malwares (MESSYFORK/COOKBOX) via des applications de messagerie.
    *   Exploitation du trojan bancaire Android Hydra via un site web falsifié (GREYBATTLE).
*   **UNC5792 (UAC-0195) :** Exploitation de la fonction de liaison d'appareils de Signal pour détourner des comptes.
*   **UNC4221 (UAC-0185) :**
    *   Utilisation de malwares Android (STALECOOKIE) imitant la plateforme de gestion de champ de bataille DELTA pour voler des cookies de navigateur.
    *   Utilisation de ClickFix pour délivrer le téléchargeur TINYWHALE, puis le logiciel de gestion à distance MeshAgent.
*   **UNC5976 (Cluster russe) :** Campagnes de phishing délivrant des fichiers de connexion RDP malveillants.
*   **UNC6096 (Cluster russe) :** Utilisation de WhatsApp avec des thèmes DELTA pour livrer un chargeur malveillant. Distribution du malware Android GALLGRAB.
*   **UNC5114 (Cluster russe suspecté) :** Distribution d'une variante du malware Android CraxsRAT, déguisée en mise à jour du système de contrôle de combat Kropyva.
*   **APT45 (Andariel) :** Utilisation du malware SmallTiger contre les secteurs de la défense, des semi-conducteurs et de l'automobile en Corée du Sud.
*   **APT43 (Kimsuky) :** Déploiement d'une backdoor (THINWAVE) via des infrastructures imitant des entités de défense allemandes et américaines.
*   **UNC2970 (Lazarus Group) :** Opération Dream Job ciblant les secteurs aérospatial, de la défense et de l'énergie, utilisant des outils IA pour le renseignement.
*   **UNC1549 (Nimbus Manticore) :** Utilisation de familles de malwares (MINIBIKE, TWOSTROKE, DEEPROOT, CRASHPAD) contre les industries aérospatiale, de l'aviation et de la défense au Moyen-Orient. Orchestration de campagnes "Dream Job".
*   **UNC6446 (Acteur lié à l'Iran) :** Distribution de malwares personnalisés via des applications de création de CV et de tests de personnalité.
*   **APT5 (Keyhole Panda) :** Phishing ciblé contre les employés actuels et anciens d'entreprises de défense.
*   **UNC3236 (Volt Typhoon) :** Activités de reconnaissance sur les portails de connexion de sous-traitants militaires nord-américains, utilisant le framework d'obfuscation ARCMAZE.
*   **UNC6508 (Cluster lié à la Chine) :** Exploitation d'une vulnérabilité REDCap pour installer un malware (INFINITERED) permettant l'accès à distance et le vol d'identifiants.

**Recommandations (implicites basées sur les tactiques observées) :**

*   **Sensibilisation du Personnel :** Former les employés aux techniques de phishing et aux processus de recrutement suspects.
*   **Sécurité des Appareils :** Renforcer la sécurité des appareils connectés, y compris les téléphones mobiles, et surveiller les vulnérabilités des applications de messagerie.
*   **Surveillance des Chaînes d'Approvisionnement :** Évaluer et renforcer la sécurité des partenaires et fournisseurs.
*   **Détection Avancée :** Utiliser des solutions de sécurité capables de détecter les activités inhabituelles et de contourner les EDR traditionnels.
*   **Gestion des Identifiants :** Mettre en place des politiques strictes de gestion des identifiants et de l'authentification multi-facteurs.
*   **Intelligence sur les Menaces :** Rester informé des nouvelles tactiques, techniques et procédures (TTPs) des groupes de menace identifiés.

---
[Source](https://thehackernews.com/2026/02/google-links-china-iran-russia-north.html){:target="_blank"}
