---
title: 'CJIS v6.1 Compliance: 5 Practical Priorities for Agencies'
date: 2026-10-20
permalink: /posts/2026/10/20/cjis-v61-compliance-5-practical-priorities-for-agencies/
tags:
- veille-cyber
- bleepingcomp
---
### Priorités pour la conformité à la norme CJIS v6.1

La mise en conformité avec la norme **CJIS v6.1** exige une gestion continue des contrôles de sécurité afin de protéger les informations de justice pénale (CJI). L'article souligne que la conformité ne doit pas être un exercice ponctuel, mais une pratique intégrée aux opérations informatiques quotidiennes.

**Points clés :**

*   **Authentification multifacteur (MFA) :** Obligatoire pour tous les comptes (privilégiés ou non) accédant aux systèmes locaux, réseau ou distants. L'usage de méthodes résistantes au phishing (clés FIDO2) est fortement recommandé.
*   **Gestion des accès :** Application du principe du moindre privilège. Nécessite un inventaire à jour des comptes et la désactivation des comptes inactifs sous 90 jours (ou suppression sous 72h pour les comptes temporaires).
*   **Gestion des mots de passe (IA-5) :** Exigence minimale de 8 caractères. Il est conseillé de privilégier les phrases de passe, de bloquer les mots de passe compromis et de limiter les tentatives de connexion à cinq.
*   **Journalisation (Logging) :** Collecte systématique des événements critiques, centralisation dans un SIEM et protection des journaux contre toute altération.
*   **Préparation aux audits :** Maintien d'un inventaire des contrôles, documentation des preuves de conformité et réalisation d'auto-évaluations régulières.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifiques, mais identifie les vecteurs de risque suivants :
*   Utilisation de mots de passe compromis ou réutilisés.
*   Comptes obsolètes (orphelins ou inactifs) non supprimés.
*   Absence de MFA sur les systèmes hérités ou les comptes administratifs.

**Recommandations :**

1.  **Automatisation :** Automatiser le provisionnement et la suppression des comptes pour réduire l'erreur humaine.
2.  **Audit permanent :** Effectuer des revues de privilèges au moins annuellement et mettre à jour les plans de remédiation tous les six mois.
3.  **Surveillance proactive :** Utiliser des outils d'analyse pour détecter les mots de passe compromis en temps réel et les bloquer lors de leur création ou modification.
4.  **Centralisation :** Centraliser la gestion des politiques et la collecte des journaux d'audit pour faciliter la démonstration de la conformité lors des contrôles triennaux.

---
[Source](https://www.bleepingcomputer.com/news/security/cjis-v61-compliance-5-practical-priorities-for-agencies/){:target="_blank"}
