---
title: 'Iran-Linked Hackers Hits Israeli Sectors with New MuddyViper Backdoor in Targeted Attacks'
date: 2025-12-02
permalink: /posts/2025/12/02/iran-linked-hackers-hits-israeli-sectors-with-new-muddyviper-backdoor-in-targeted-attacks/
tags:
- veille-cyber
- hackernews
---
**Vague Viper : Une Nouvelle Menace Iranienne Cible Israël**

Des acteurs étatiques iraniens, affiliés au groupe de cyberespionnage MuddyWater (également connu sous les noms de Mango Sandstorm ou TA450), ont lancé une campagne de cyberattaques ciblées contre des entités israéliennes. Les secteurs visés incluent l'éducation, l'ingénierie, les gouvernements locaux, l'industrie manufacturière, la technologie, le transport et les services publics. Une entreprise technologique égyptienne a également été ciblée.

Ces attaques reposent sur des techniques classiques telles que le spear-phishing et l'exploitation de vulnérabilités connues dans les infrastructures VPN. Cependant, la particularité de cette campagne réside dans le déploiement d'un nouveau cheval de Troie, nommé MuddyViper, non documenté jusqu'à présent. Ce dernier, associé à un chargeur nommé Fooder, permet aux attaquants de collecter des informations système, d'exécuter des fichiers et des commandes, de transférer des fichiers et d'exfiltrer des identifiants Windows ainsi que des données de navigation. MuddyViper peut exécuter une vingtaine de commandes, facilitant ainsi l'accès et le contrôle furtifs des systèmes compromis.

Parmi les autres outils utilisés par le groupe, on retrouve des RATs (outils d'administration à distance) tels que Blackout, AnchorRat et CannonRat, le virus d'infection de fichiers Neshta, et un framework de commande et contrôle (C2) nommé Sad C2, capable de déployer le RAT BlackPearl. Les variantes du chargeur Fooder peuvent aussi déployer des proxys de tunneling inverse go-socks5 et l'outil open-source HackBrowserData pour voler des données de navigation.

D'autres malwares notables incluent VAXOne (un cheval de Troie imitant des services légitimes), CE-Notes et Blub (voleurs de données de navigation visant à contourner les mécanismes de sécurité), et LP-Notes (un voleur d'identifiants affichant de fausses fenêtres de sécurité Windows).

L'évolution de ces techniques, notamment l'utilisation de composants inédits comme Fooder et MuddyViper, témoigne d'une sophistication accrue de MuddyWater dans sa quête de discrétion, de persistance et de capacités de vol d'identifiants.

**Points Clés :**

*   **Acteurs :** MuddyWater (Mango Sandstorm, TA450), affilié au ministère iranien de la Sécurité et du renseignement (MOIS).
*   **Cibles :** Secteurs académique, ingénierie, gouvernement local, manufacturier, technologique, transport et utilités en Israël. Une entreprise technologique égyptienne également touchée.
*   **Nouvelle Menace :** Cheval de Troie "MuddyViper", non documenté précédemment.
*   **Méthodes d'Attaque :** Spear-phishing, exploitation de vulnérabilités VPN, déploiement d'outils de gestion à distance légitimes.
*   **Chargeur :** Fooder, conçu pour décrypter et exécuter MuddyViper, et peut également déployer des proxys et l'outil HackBrowserData.
*   **Capacités de MuddyViper :** Collecte d'informations système, exécution de commandes, transfert de fichiers, exfiltration d'identifiants et de données de navigation.

**Vulnérabilités :**

L'article mentionne l'exploitation de "vulnérabilités connues dans les infrastructures VPN", mais ne spécifie aucune CVE particulière pour ces attaques.

**Recommandations :**

Bien que l'article ne propose pas de liste de recommandations explicites, les pratiques de sécurité standard s'appliquent :

*   **Renforcer la sécurité des infrastructures VPN :** S'assurer que les VPN sont à jour et corrigés contre les vulnérabilités connues.
*   **Sensibilisation au Spear-Phishing :** Former les employés à identifier et signaler les emails suspects, en particulier ceux contenant des pièces jointes ou des liens.
*   **Mise à jour des Systèmes :** Maintenir tous les systèmes d'exploitation, logiciels et applications à jour pour corriger les vulnérabilités connues.
*   **Surveillance et Détection :** Mettre en place des outils de surveillance réseau et des systèmes de détection d'intrusion pour identifier rapidement les activités suspectes.
*   **Gestion des Accès :** Appliquer le principe du moindre privilège pour limiter l'impact potentiel d'une compromission.

---
[Source](https://thehackernews.com/2025/12/iran-linked-hackers-hits-israeli_2.html){:target="_blank"}
