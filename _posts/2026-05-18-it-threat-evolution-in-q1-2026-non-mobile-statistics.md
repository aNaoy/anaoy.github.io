---
title: 'IT threat evolution in Q1 2026. Non-mobile statistics'
date: 2026-05-18
permalink: /posts/2026/05/18/it-threat-evolution-in-q1-2026-non-mobile-statistics/
tags:
- veille-cyber
- securelist
---
### Évolution des menaces informatiques au premier trimestre 2026

Le premier trimestre 2026 a été marqué par une activité cybercriminelle intense, caractérisée par plus de 343 millions d'attaques en ligne bloquées et près de 15 millions d'objets malveillants détectés localement.

#### Points clés
*   **Ransomware :** Malgré des succès opérationnels des forces de l'ordre (démantèlement du forum RAMP, arrestations liées aux groupes Phobos et BlackCat), le secteur reste très actif. Le groupe **Clop** domine les fuites de données (14,42 %), suivi par **Qilin** et le nouvel acteur émergent, **The Gentlemen**.
*   **Cryptominage :** Plus de 260 000 utilisateurs ont été ciblés par des mineurs de cryptomonnaies.
*   **Menaces macOS :** Recrudescence de campagnes de phishing par appel vidéo frauduleux et découverte d'un kit d'exploitation sophistiqué ciblant iOS/macOS via des téléchargements *drive-by*. Une attaque par chaîne d'approvisionnement a également compromis le package npm "Axios".
*   **IoT :** Augmentation significative des attaques via le protocole SSH, avec une prédominance persistante des variantes du botnet Mirai.

#### Vulnérabilités exploitées
*   **CVE-2026-20131 :** Vulnérabilité zero-day dans le logiciel de gestion de pare-feu Cisco Secure FMC. Exploitée activement par le groupe **Interlock** depuis janvier 2026 pour permettre l'exécution de code Java arbitraire avec des privilèges root.

#### Recommandations
*   **Gestion des correctifs :** Appliquer immédiatement les mises à jour de sécurité pour les équipements réseau critiques, notamment les pare-feu, pour contrer les exploits zero-day.
*   **Sécurisation de la chaîne d'approvisionnement :** Auditer les dépendances logicielles (ex: packages npm) pour prévenir l'injection de backdoors via des bibliothèques tierces.
*   **Renforcement des accès :** Sécuriser les accès à distance (SSH/Telnet) sur les objets connectés (IoT) en désactivant les services inutilisés et en utilisant une authentification forte.
*   **Hygiène numérique :** Sensibiliser les utilisateurs aux techniques d'ingénierie sociale, particulièrement lors de fausses interventions de support technique.

---
[Source](https://securelist.com/malware-report-q1-2026-pc-iot-statistics/119828/){:target="_blank"}
