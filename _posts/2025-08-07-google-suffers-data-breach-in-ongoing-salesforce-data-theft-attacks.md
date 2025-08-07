---
title: 'Google suffers data breach in ongoing Salesforce data theft attacks'
date: 2025-08-07
permalink: /posts/2025/08/07/google-suffers-data-breach-in-ongoing-salesforce-data-theft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Des Vagues de Vol de Données Ciblent les CRM d'Entreprise**

Une campagne de cyberattaques généralisée, orchestrée par le groupe ShinyHunters, cible les instances Salesforce de diverses entreprises dans le but d'exfiltrer des données clients. Google a récemment révélé avoir été victime de ces attaques en juin, subissant une brèche de l'une de ses instances Salesforce.

Les acteurs de la menace, identifiés par Google sous les noms de code UNC6040 ou UNC6240, emploient des techniques d'ingénierie sociale, notamment le "vishing" (hameçonnage vocal), pour accéder aux systèmes CRM des entreprises. Une fois l'accès obtenu, ils téléchargent des données clients, puis tentent d'extorquer les entreprises en exigeant une rançon pour éviter la divulgation publique de ces informations.

Les données dérobées lors de l'attaque contre Google se limitaient à des informations commerciales basiques et majoritairement publiques, telles que les noms d'entreprises et les coordonnées. Cependant, la portée de ces attaques est plus large, affectant de nombreuses autres organisations réputées.

**Points Clés :**

*   **Attaque Ciblée :** Les groupes ShinyHunters (également désignés UNC6040/UNC6240 par Google) ciblent spécifiquement les environnements Salesforce.
*   **Méthode d'Attaque :** Utilisation du "vishing" pour mener des attaques d'ingénierie sociale et obtenir un accès non autorisé.
*   **Objectif :** Vol de données clients stockées dans les CRM pour pratiquer l'extorsion.
*   **Impact sur Google :** Une instance Salesforce a été compromise, entraînant le vol d'informations de contact d'entreprises et de notes associées.
*   **Tactique d'Extorsion :** Les attaquants exigent une rançon sous peine de divulguer ou de vendre les données volées sur des forums clandestins.
*   **Amplitude des Attaques :** Plusieurs grandes entreprises ont été touchées, y compris Adidas, Qantas, Allianz Life, Cisco, ainsi que des filiales de LVMH comme Louis Vuitton, Dior et Tiffany & Co.

**Vulnérabilités :**

L'article ne mentionne pas de CVE spécifiques liées à ces attaques. L'exploitation repose sur des vulnérabilités dans les processus d'authentification, potentiellement liées à des informations d'identification compromises ou à des vecteurs d'ingénierie sociale réussis.

**Recommandations :**

Bien que l'article ne détaille pas explicitement les recommandations pour les victimes, les pratiques générales de cybersécurité impliquent :

*   **Renforcement des Mesures de Sécurité Salesforce :** Vérifier et renforcer les contrôles d'accès, l'authentification multifacteur (MFA) et les autorisations des utilisateurs au sein de l'environnement Salesforce.
*   **Sensibilisation et Formation des Employés :** Éduquer le personnel sur les risques du phishing, du vishing et des autres techniques d'ingénierie sociale.
*   **Surveillance et Détection :** Mettre en place une surveillance continue des activités suspectes au sein des systèmes CRM.
*   **Réponse aux Incidents :** Disposer d'un plan de réponse aux incidents de sécurité bien défini pour contenir et gérer rapidement les brèches de données.
*   **Gestion des Identifiants :** Promouvoir des pratiques robustes de gestion des mots de passe et envisager des solutions de gestion des identités et des accès (IAM).

---
[Source](https://www.bleepingcomputer.com/news/security/google-suffers-data-breach-in-ongoing-salesforce-data-theft-attacks/){:target="_blank"}
