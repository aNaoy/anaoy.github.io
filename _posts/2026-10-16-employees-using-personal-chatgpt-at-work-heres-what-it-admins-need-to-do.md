---
title: 'Employees using personal ChatGPT at work? Heres what IT admins need to do'
date: 2026-10-16
permalink: /posts/2026/10/16/employees-using-personal-chatgpt-at-work-heres-what-it-admins-need-to-do/
tags:
- veille-cyber
- bleepingcomp
---
### Gestion de l'utilisation de comptes personnels ChatGPT en entreprise

L'usage de comptes ChatGPT personnels sur des appareils professionnels représente un risque majeur de fuite de données confidentielles (documents sensibles, informations clients, identifiants). L'absence de visibilité sur le contenu des requêtes (prompts) rend complexe l'évaluation de l'exposition réelle lors d'un incident.

**Points clés :**
*   **Différenciation des identités :** Les outils de sécurité doivent permettre de distinguer les sessions personnelles des sessions d'entreprise pour identifier précisément qui a transmis quoi.
*   **Le défi de la visibilité :** Sans outils de contrôle au niveau du navigateur, les administrateurs dépendent de la bonne foi des employés pour auditer les fuites de données.
*   **Causes fréquentes :** Le recours au compte personnel est souvent dû à des contraintes techniques (sessions expirées, lenteur du 2FA) plutôt qu'à une volonté de malveillance.

**Vulnérabilités :**
*   **Fuite de données (Data Leakage) :** Risque lié à l'envoi d'informations critiques (données clients, secrets industriels) vers des instances IA non maîtrisées.
*   *Note :* Bien qu'aucune CVE spécifique ne soit citée, cette problématique est classée sous les risques de **Shadow AI** et de mauvaise gestion des données (Data Exfiltration).

**Recommandations :**
1.  **Mise en place de contrôles de flux :** Déployer des outils capables d'analyser et d'intercepter les prompts avant leur envoi depuis le navigateur (ex: solutions de type "AI Scout").
2.  **Configuration de politiques granulaires :** Appliquer des règles adaptées au niveau de risque :
    *   **Avertir (Warn) :** Inciter l'employé à la prudence avant l'envoi.
    *   **Masquer (Redact) :** Supprimer automatiquement les données sensibles (ex: numéros de compte) avant l'envoi.
    *   **Bloquer (Block) :** Empêcher strictement la transmission de données critiques.
3.  **Audit et remédiation :** En cas d'incident, évaluer le périmètre des données exposées, révoquer les accès si nécessaire et s'assurer que l'accès à la solution d'entreprise est fluide et fonctionnel pour éviter les contournements par les employés.
4.  **Sensibilisation :** Clarifier les politiques d'utilisation interne et expliquer pourquoi l'accès "Entreprise" doit être privilégié pour garantir la confidentialité.

---
[Source](https://www.bleepingcomputer.com/news/security/employees-using-personal-chatgpt-at-work-heres-what-it-admins-need-to-do/){:target="_blank"}
