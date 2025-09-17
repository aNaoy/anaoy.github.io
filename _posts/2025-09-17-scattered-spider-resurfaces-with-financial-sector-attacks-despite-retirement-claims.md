---
title: 'Scattered Spider Resurfaces With Financial Sector Attacks Despite Retirement Claims'
date: 2025-09-17
permalink: /posts/2025/09/17/scattered-spider-resurfaces-with-financial-sector-attacks-despite-retirement-claims/
tags:
- veille-cyber
- hackernews
---
**Le Retour de Scattered Spider : Une Menace Persistante pour le Secteur Financier**

Des recherches récentes suggèrent que le groupe de cybercriminalité connu sous le nom de Scattered Spider, malgré des affirmations antérieures de cessation d'activités, est de retour et cible activement le secteur financier. Cette activité s'est manifestée par la création de noms de domaine trompeurs orientés vers ce secteur et une intrusion ciblée dans une institution bancaire américaine non nommée.

**Points Clés :**

*   **Focus sur le Secteur Financier :** Des indices indiquent un recentrage de Scattered Spider vers les institutions financières.
*   **Méthodes d'Accès Initial :** L'ingénierie sociale via un compte exécutif a été utilisée pour réinitialiser des mots de passe via Azure Active Directory Self-Service Password Management.
*   **Progression dans le Réseau :** L'accès à des documents sensibles, la mobilité latérale via Citrix et VPN, et la compromission d'infrastructure VMware ESXi ont été observés.
*   **Élévation de Privilèges et Évasion :** La réinitialisation du mot de passe d'un compte de service Veeam, l'attribution de permissions d'administrateur global Azure, et le déplacement de machines virtuelles ont été utilisés pour l'escalade de privilèges et l'évasion.
*   **Tentatives d'Exfiltration :** Des tentatives d'exfiltration de données depuis Snowflake, Amazon Web Services (AWS) et d'autres dépôts ont été détectées.
*   **Lien avec d'Autres Groupes :** Scattered Spider est lié à d'autres groupes comme ShinyHunters et LAPSUS$, formant parfois une entité plus large nommée "scattered LAPSUS$ hunters".
*   **Doute sur la "Retraite" :** Les affirmations de cessation d'activités du groupe sont considérées avec scepticisme, potentiellement une manœuvre stratégique pour échapper à la pression des forces de l'ordre, se regrouper ou changer d'identité.

**Vulnérabilités et Vecteurs d'Attaque :**

*   **Ingénierie Sociale :** L'exploitation de la confiance et de l'accès des exécutifs pour obtenir un accès initial.
*   **Gestion des Identités et des Accès :** Exploitation de la fonctionnalité "Self-Service Password Management" d'Azure Active Directory et de comptes de service (Veeam) pour une élévation de privilèges.
*   **Configuration d'Infrastructure Cloud et Virtuelle :** Compromission d'environnements Citrix, VPN, VMware ESXi, Snowflake et AWS.
*   **Faiblesses de la Configuration des Services Cloud :** Potentielle mauvaise configuration des environnements AWS et Snowflake facilitant l'exfiltration.

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article.

**Recommandations :**

*   **Maintenir la Vigilance :** Les organisations, en particulier dans le secteur financier, doivent rester vigilantes face aux menaces persistantes et ne pas se fier aux affirmations de "retraite" des groupes de cybercriminels.
*   **Renforcer la Sécurité des Identités et des Accès :** Examiner et sécuriser rigoureusement les processus de gestion des mots de passe, y compris les fonctionnalités de réinitialisation automatique, et les permissions des comptes de service.
*   **Sécuriser l'Environnement Cloud et Virtuel :** Mettre en place des contrôles de sécurité robustes pour les infrastructures virtualisées (VMware ESXi) et les plateformes cloud (AWS, Snowflake), en accordant une attention particulière aux permissions d'accès et aux stratégies d'évasion.
*   **Surveillance des Domaines :** Surveiller activement les domaines ressemblant à des domaines légitimes utilisés par des entreprises du secteur financier pour détecter les tentatives d'hameçonnage et de phishing.
*   **Contrôles d'Accès Strict :** Appliquer le principe du moindre privilège pour tous les comptes utilisateurs et de service.
*   **Contre-mesures contre l'Ingénierie Sociale :** Mettre en place des formations de sensibilisation continues pour les employés sur les tactiques d'ingénierie sociale.

---
[Source](https://thehackernews.com/2025/09/scattered-spider-resurfaces-with.html){:target="_blank"}
