---
title: 'French Tax Data Theft Using Stolen Staff Passwords Went Undetected for Seven Weeks'
date: 2026-09-29
permalink: /posts/2026/09/29/french-tax-data-theft-using-stolen-staff-passwords-went-undetected-for-seven-weeks/
tags:
- veille-cyber
- hackernews
---
### Cyberattaque contre la DGFIP : vol de données fiscales par usurpation d'identité

Une intrusion informatique a permis à un attaquant d'accéder aux données de plus de 350 000 particuliers et 250 000 entreprises via l'outil « E-Contact » de l'administration fiscale française (DGFIP). L'attaque, restée indétectable pendant sept semaines entre juin et juillet, n'était pas sophistiquée mais a exploité des failles structurelles.

#### Points clés
*   **Mode opératoire :** L'attaquant a utilisé des identifiants (mots de passe) de personnels de la DGFIP, probablement volés via des logiciels malveillants (*infostealers*) sur des appareils personnels non gérés.
*   **Vecteurs d'accès :** Utilisation du portail interne PIGP et de la passerelle ADER (connectée au réseau interministériel RIE). Un second accès a été obtenu via le portail APEX en compromettant le poste de travail d'un notaire/géomètre partenaire.
*   **Défaillance de surveillance :** Le centre opérationnel de sécurité (SOC) a détecté des activités suspectes et réinitialisé des mots de passe, mais n'a pas mis fin aux sessions actives, permettant à l'attaquant de poursuivre l'exfiltration de données. L'absence de journalisation sur les applications métier et de corrélation des alertes a empêché la détection précoce.

#### Vulnérabilités identifiées
*   **Absence d'authentification multifacteur (MFA) :** Accès basés uniquement sur des mots de passe.
*   **Faiblesse du cloisonnement réseau :** Accès non restreint aux applications sensibles depuis le réseau interministériel.
*   **Gestion des sessions :** La réinitialisation d'un mot de passe ne terminait pas les sessions ouvertes, permettant la persistance.
*   **Usage d'appareils personnels :** Accès aux outils professionnels depuis des machines non sécurisées par l'administration.
*   **Déficit de monitoring :** Absence de surveillance des volumes de données extraits et absence de quotas de requêtes.

#### Recommandations de l'ANSSI
*   **Renforcement de l'authentification :** Généraliser le MFA avec des jetons matériels ou des applications d'authentification (bannir le code par mail).
*   **Gestion des sessions :** Révoquer systématiquement toutes les sessions actives lors d'une réinitialisation de mot de passe.
*   **Audit et Journalisation :** Intégrer les logs de toutes les applications métier dans un SIEM (outil de gestion des événements de sécurité).
*   **Contrôle des flux :** Instaurer des quotas stricts sur le nombre de requêtes et le volume de données consultables.
*   **Politique d'accès :** Interdire formellement l'accès aux ressources de travail depuis des appareils personnels.
*   **Réaction sur incident :** En cas de compromission, effectuer une analyse rétrospective complète de l'activité du compte suspect depuis la date supposée de l'intrusion.

---
[Source](https://thehackernews.com/2026/09/french-tax-data-theft-using-stolen.html){:target="_blank"}
