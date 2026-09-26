---
title: 'U.S. Soldier Gets 70 Months in Prison for AT&T, Verizon Extortions'
date: 2026-09-26
permalink: /posts/2026/09/26/us-soldier-gets-70-months-in-prison-for-att-verizon-extortions/
tags:
- veille-cyber
- krebs
---
### Condamnation d'un soldat américain pour cybercriminalité et extorsion

Cameron John Wagenius, un soldat de l'armée américaine en poste en Corée du Sud, a été condamné à 70 mois de prison fédérale et au paiement de près de 300 000 $ de dédommagements. Sous le pseudonyme « Kiberphant0m », il a orchestré le piratage de plusieurs entreprises de télécommunications, dont AT&T et Verizon, compromettant les métadonnées de plus de 100 millions d'utilisateurs.

**Points clés :**
*   **Méthode d'intrusion :** Le groupe a ciblé des entreprises utilisant la plateforme **Snowflake** via des identifiants exposés, profitant de l'absence d'authentification multifacteur (MFA) à l'époque.
*   **Mode opératoire :** Wagenius pratiquait l'extorsion en menaçant de publier des données sensibles, allant jusqu'à prétendre posséder des documents classifiés de la NSA.
*   **Récidive carcérale :** Durant sa détention en attente de jugement, Wagenius a tenté d'utiliser des outils d'IA via les systèmes de messagerie de la prison pour identifier des vulnérabilités exploitables et concevoir des dispositifs radio artisanaux.
*   **Résultats financiers :** Malgré l'ampleur des données dérobées, ses gains réels s'élèvent à seulement 1 500 dollars environ.

**Vulnérabilités mentionnées :**
*   **Absence de MFA :** L'oubli de l'authentification forte sur les comptes Snowflake a été le vecteur principal d'accès initial.
*   **CVE-2023-45208 :** Une vulnérabilité de type « injection de commande » affectant les équipements réseau D-Link, que le suspect a cherché à exploiter depuis sa cellule.

**Recommandations :**
*   **Généralisation du MFA :** Imposer l'authentification multifacteur sur tous les accès, particulièrement sur les plateformes de stockage de données cloud.
*   **Gestion des accès :** Sécuriser les identifiants pour éviter qu'ils ne soient exposés ou réutilisés (Credential Stuffing).
*   **Vigilance face à l'IA :** Mettre en place des protocoles de filtrage sur l'usage des outils d'IA générative dans des environnements contrôlés afin de prévenir les techniques de « prompt injection » visant à contourner les protections contre la génération de code malveillant.

---
[Source](https://krebsonsecurity.com/2026/09/u-s-soldier-gets-70-months-in-prison-for-att-verizon-extortions/){:target="_blank"}
