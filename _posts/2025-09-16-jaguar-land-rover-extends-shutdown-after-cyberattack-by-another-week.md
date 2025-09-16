---
title: 'Jaguar Land Rover extends shutdown after cyberattack by another week'
date: 2025-09-16
permalink: /posts/2025/09/16/jaguar-land-rover-extends-shutdown-after-cyberattack-by-another-week/
tags:
- veille-cyber
- bleepingcomp
---
**Impact d'une cyberattaque sur Jaguar Land Rover**

Jaguar Land Rover (JLR) a étendu la suspension de sa production d'une semaine supplémentaire suite à une cyberattaque qui a perturbé ses systèmes fin août. Les opérations ne devraient reprendre que le 24 septembre 2025.

L'entreprise a confirmé que des données ont été dérobées lors de l'incident. Bien qu'aucune opération de rançongiciel n'ait encore revendiqué l'attaque, un groupe se nommant "Scattered Lapsus$ Hunters" a affirmé en être responsable. Ce groupe, qui aurait des liens avec les groupes Scattered Spider, Lapsus$ et ShinyHunters, affirme également avoir déployé un rançongiciel sur les systèmes compromis de JLR. Ils ont par le passé revendiqué des attaques similaires contre des entreprises de renom telles que Salesforce, Google, Cloudflare, Palo Alto Networks, Tenable et Proofpoint, utilisant des techniques d'ingénierie sociale et des jetons OAuth compromis.

**Points Clés :**

*   Prolongation de la suspension de production de JLR d'une semaine.
*   Vol de données confirmé lors de la cyberattaque.
*   Revendication de l'attaque par le groupe "Scattered Lapsus$ Hunters".
*   Utilisation présumée de rançongiciel par les attaquants.
*   Liens potentiels du groupe d'attaquants avec d'autres groupes cybercriminels connus.
*   Méthodes d'attaque similaires utilisées précédemment contre d'autres grandes entreprises.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (avec CVE) n'est explicitement mentionnée dans l'article. Cependant, les méthodes d'attaque évoquées suggèrent des failles potentielles dans :

*   Les défenses contre l'ingénierie sociale.
*   La gestion des jetons d'authentification (OAuth tokens), potentiellement liés à des intégrations tierces comme Salesloft et Drift.
*   La sécurité des systèmes internes (mention d'un système SAP compromis).

**Recommandations :**

Bien que l'article ne contienne pas de recommandations directes pour JLR, les informations fournies impliquent les actions suivantes :

*   **Renforcer les défenses contre l'ingénierie sociale :** Former le personnel à reconnaître et signaler les tentatives de phishing et autres tactiques d'ingénierie sociale.
*   **Sécuriser la gestion des accès et des identifiants :** Revoir et renforcer la sécurité des jetons OAuth et des autres mécanismes d'authentification, en particulier pour les intégrations avec des services tiers.
*   **Mettre à jour et sécuriser les systèmes critiques :** S'assurer que les systèmes internes, y compris les ERP comme SAP, sont correctement patchés et configurés pour prévenir les accès non autorisés.
*   **Mener une investigation forensique approfondie :** Continuer l'enquête pour identifier précisément la cause racine de la compromission, les points d'entrée et l'étendue complète des dommages.
*   **Mettre en œuvre des plans de reprise après sinistre :** Avoir des plans solides pour une reprise contrôlée et sécurisée des opérations après un incident majeur.

---
[Source](https://www.bleepingcomputer.com/news/security/jaguar-land-rover-extends-shutdown-after-cyberattack-by-another-week/){:target="_blank"}
