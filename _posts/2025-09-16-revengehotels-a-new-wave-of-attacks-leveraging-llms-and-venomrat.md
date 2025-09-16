---
title: 'RevengeHotels: a new wave of attacks leveraging LLMs and VenomRAT'
date: 2025-09-16
permalink: /posts/2025/09/16/revengehotels-a-new-wave-of-attacks-leveraging-llms-and-venomrat/
tags:
- veille-cyber
- securelist
---
**Des menaces informatiques évoluées : l'IA au service de RevengeHotels et VenomRAT**

Un groupe de cybercriminels, actif depuis 2015 et connu sous le nom de RevengeHotels (TA558), cible principalement le secteur de l'hôtellerie pour voler des données de cartes de crédit. Initialement, ils utilisaient des e-mails de phishing contenant des documents malveillants, exploitant parfois des vulnérabilités connues comme CVE-2017-0199 pour installer divers RAT (Remote Access Trojan). Ces attaques visaient des hôtels en Amérique latine, en Russie, en Biélorussie et en Turquie. Le groupe a ensuite élargi son arsenal avec des RAT tels que XWorm et DesckVBRAT.

Récemment, une nouvelle vague d'attaques a été observée, caractérisée par l'utilisation accrue d'outils sophistiqués, notamment le RAT VenomRAT. Le vecteur d'infection principal reste les e-mails de phishing, souvent à thème de factures ou de fausses candidatures d'emploi, adressés aux employés d'hôtels. Ces e-mails redirigent les victimes vers des sites web malveillants qui téléchargent un script JavaScript. Ce qui distingue ces nouvelles campagnes est l'utilisation apparente d'agents basés sur de grands modèles linguistiques (LLM) pour générer le code des premières étapes de l'infection. Ce code généré par IA se reconnaît à sa clarté, ses commentaires détaillés et l'utilisation de placeholders, contrastant avec le code malveillant plus obfusqué des campagnes précédentes.

Le script initial déclenche une chaîne de téléchargement et d'exécution de scripts PowerShell et de fichiers texte contenant le RAT VenomRAT. VenomRAT, basé sur le code open-source QuasarRAT, est proposé à la vente sur le dark web et offre des fonctionnalités étendues comme un bureau caché (HVNC), un voleur de fichiers, un proxy inverse et un exploit de privilèges utilisateur. Il intègre des mécanismes de protection avancés, incluant une protection contre la terminaison par des outils de sécurité, la persistance via le registre Windows et des boucles de surveillance de processus, et la désactivation de Windows Defender. Il communique avec son serveur de commande et contrôle (C2) via des paquets compressés et chiffrés, et peut se propager via des clés USB en effaçant les journaux d'événements Windows et les identifiants de téléchargement pour échapper à la détection.

Les cibles actuelles se concentrent sur les hôtels brésiliens, mais des campagnes en espagnol visant des pays hispanophones ont également été identifiées, montrant une expansion géographique.

**Points Clés:**

*   **Évolution des TTPs:** Le groupe RevengeHotels adapte ses méthodes en intégrant de nouveaux outils et en exploitant les avancées technologiques.
*   **Utilisation de l'IA:** L'emploi de grands modèles linguistiques pour générer du code malveillant facilite la création de lures plus convaincantes et rend les attaques plus rapides et évolutives.
*   **VenomRAT:** Ce RAT avancé constitue le cœur des nouvelles campagnes, offrant des fonctionnalités robustes pour le contrôle à distance et la persistance.
*   **Ciblage sectoriel:** L'industrie hôtelière et du tourisme demeure la cible principale, avec une expansion géographique vers les marchés hispanophones.
*   **Techniques de dissimulation:** Des méthodes comme l'effacement des journaux et la suppression des identifiants de téléchargement renforcent la furtivité du malware.

**Vulnérabilités Mentionnées:**

*   **CVE-2017-0199:** Vulnérabilité précédemment exploitée pour l'installation de scripts.

**Recommandations:**

*   **Sensibilisation à la phishing:** Renforcer la formation des employés à la détection des e-mails de phishing, en particulier ceux concernant des factures ou des offres d'emploi.
*   **Mises à jour de sécurité:** Assurer l'application des correctifs de sécurité sur tous les systèmes, notamment pour les vulnérabilités connues comme CVE-2017-0199.
*   **Solutions de sécurité:** Déployer et maintenir à jour des solutions antivirus et antimalware avancées capables de détecter les menaces nouvelles et évolutives, y compris les comportements potentiellement liés à l'IA.
*   **Surveillance du réseau:** Mettre en place une surveillance active du trafic réseau pour identifier les communications suspectes avec des serveurs de commande et contrôle.
*   **Gestion des accès:** Appliquer le principe du moindre privilège et surveiller les tentatives d'escalade de privilèges, particulièrement celles impliquant des droits d'administrateur.
*   **Protection des points d'accès:** Sécuriser les environnements de travail, y compris les accès distants et la gestion des périphériques USB.

---
[Source](https://securelist.com/revengehotels-attacks-with-ai-and-venomrat-across-latin-america/117493/){:target="_blank"}
