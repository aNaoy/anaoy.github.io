---
title: 'Can I have a new password, please? The $400M question.'
date: 2025-09-10
permalink: /posts/2025/09/10/can-i-have-a-new-password-please-the-400m-question/
tags:
- veille-cyber
- bleepingcomp
---
**Sécurité des Plateformes d'Assistance : La Vulnérabilité Humaine Exploiteée**

Une attaque attribuée au groupe Scattered Spider a ciblé Clorox en exploitant des vulnérabilités au niveau des processus d'assistance technique externe. Plutôt que de recourir à des failles techniques complexes, les attaquants ont utilisé l'ingénierie sociale en se faisant passer pour des employés bloqués afin d'obtenir des réinitialisations de mots de passe et d'authentification multifacteur (MFA).

**Points Clés :**

*   **Méthode d'Attaque :** L'ingénierie sociale par téléphone, ciblant les agents du service desk.
*   **Cible :** Le service desk externalisé de Cognizant, gérant le support pour Clorox.
*   **Exploitation :** Les attaquants ont obtenu des réinitialisations d'identifiants et de MFA sans vérifications suffisantes, contournant les procédures de sécurité.
*   **Conséquences :** Désorganisation opérationnelle majeure pour Clorox, incluant l'arrêt de la production, des retards dans le traitement des commandes et des pertes financières estimées à environ 380 millions de dollars.
*   **Facteur Aggravant :** L'externalisation des services d'assistance, combinée à des processus de vérification faibles chez le prestataire, a amplifié le risque. Les prestataires peuvent avoir des privilèges étendus et des flux de travail rapides ("fast-path") qui, s'ils sont mal gérés, peuvent affecter de multiples clients.

**Vulnérabilités (non spécifiées avec CVE mais description du problème) :**

*   **Vérification d'Identité Insuffisante :** Les agents du service desk ont été convaincus par des appels téléphoniques de réinitialiser les informations d'identification et le MFA sans vérifications hors bande appropriées.
*   **"Process Drift" et Manque de Rigueur :** Face à un volume élevé d'appels, les agents peuvent privilégier la résolution rapide au détriment de la stricte application des procédures de sécurité.
*   **Manque de Visibilité :** Les actions des prestataires externes peuvent ne pas être entièrement intégrées aux systèmes de surveillance (SIEM) du client, retardant la détection des incidents.

**Recommandations :**

Pour renforcer la sécurité des plateformes d'assistance et prévenir de tels incidents :

*   **Vérification Hors Bande :** Imposer des méthodes de vérification robustes pour toute réinitialisation à distance, comme un rappel vers un numéro d'entreprise validé, un jeton envoyé par email à une adresse professionnelle, ou un défi cryptographique.
*   **Seuils d'Approbation :** Exiger une approbation à deux niveaux pour les réinitialisations à haut risque (MFA, groupes d'administration, comptes de service) avec notification automatique du manager.
*   **Sessions Temporaires et Isolation :** Utiliser des sessions privilégiées de courte durée pour les tâches de remédiation et révoquer les sessions prolongées suspectes.
*   **Télémétrie et Confinement Automatisés :** Journaliser systématiquement toutes les réinitialisations dans une piste d'audit immuable, alerter sur les schémas de réinitialisation anormaux et révoquer automatiquement les jetons de rafraîchissement en cas de séquences suspectes.
*   **Détection et Règles :** Mettre en place des règles de détection basées sur des modèles d'activité suspects (par exemple, plusieurs réinitialisations MFA pour des utilisateurs du même département dans un laps de temps court) pour déclencher des actions de confinement automatisées.
*   **Gouvernance Opérationnelle :** Inclure dans les contrats avec les prestataires des exigences strictes concernant les contrôles techniques, l'auditabilité (preuves par logs et tests annuels), des accords de niveau de service (SLA) pour la détection et la réponse aux incidents, et des simulations de tests d'ingénierie sociale.
*   **Formation Continue :** Effectuer des simulations régulières d'appels téléphoniques auprès des équipes d'assistance (internes et prestataires) pour mesurer les faiblesses et intégrer des formations correctives.

---
[Source](https://www.bleepingcomputer.com/news/security/can-i-have-a-new-password-please-the-400m-question/){:target="_blank"}
