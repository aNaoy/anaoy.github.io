---
title: 'Gainsight Expands Impacted Customer List Following Salesforce Security Alert'
date: 2025-11-27
permalink: /posts/2025/11/27/gainsight-expands-impacted-customer-list-following-salesforce-security-alert/
tags:
- veille-cyber
- hackernews
---
**Impact Accru sur les Clients Gainsight suite à une Alerte de Sécurité Salesforce**

Une activité suspecte détectée par Salesforce, visant des applications publiées par Gainsight, a affecté un nombre plus important de clients que prévu initialement. Bien que le nombre exact de clients impactés n'ait pas été précisé, des données suggèrent que seule une "poignée" d'entre eux a vu leurs données compromises. Ce piratage a été revendiqué par le groupe cybercriminel ShinyHunters.

En réponse, plusieurs mesures ont été prises : Salesforce a révoqué tous les accès et jetons d'actualisation associés aux applications Gainsight concernées. Des partenaires tels que Zendesk, Gong.io et HubSpot ont suspendu temporairement leurs intégrations avec Gainsight, et Google a désactivé certains clients OAuth. HubSpot a toutefois indiqué n'avoir trouvé aucune preuve de compromission de sa propre infrastructure ou de celle de ses clients.

Les produits Gainsight potentiellement concernés par cette perte d'accès temporaire à Salesforce incluent : Customer Success (CS), Community (CC) et Northpass - Customer Education (CE). L'intégration Staircase (ST) n'est pas affectée, mais a été déconnectée par mesure de précaution.

Des indicateurs de compromission (IoCs) ont été publiés par Salesforce et Gainsight, notamment une chaîne d'agent utilisateur ("Salesforce-Multi-Org-Fetcher/1.0") précédemment utilisée dans des activités similaires. Les premières tentatives de reconnaissance ont été enregistrées dès le 23 octobre 2025, suivies d'autres vagues d'accès non autorisés à partir du 8 novembre.

**Points Clés:**
*   **Expansion des clients affectés :** Plus de clients Gainsight que prévu initialement ont été impactés par l'activité suspecte liée à Salesforce.
*   **Revendication par ShinyHunters :** Le groupe cybercriminel ShinyHunters est suspecté d'être à l'origine de l'incident.
*   **Produits concernés :** Les applications Gainsight Customer Success, Community et Northpass - Customer Education ont connu des perturbations d'accès à Salesforce.
*   **Mesures de sécurité :** Revocation de jetons, suspension d'intégrations, désactivation de clients OAuth.
*   **Indicateurs de compromission (IoCs) :** Partage d'informations techniques pour aider à la détection.

**Vulnérabilités (avec CVE si possible):**
L'article ne mentionne pas de CVE spécifiques pour cet incident. Il décrit une activité suspecte et des accès non autorisés plutôt qu'une vulnérabilité technique précise permettant l'exploitation. L'accès non autorisé semble avoir été facilité par la compromission de jetons d'accès liés aux applications Gainsight.

**Recommandations:**
*   Rotation des clés d'accès aux buckets S3 et autres connecteurs (BigQuery, Zuora, Snowflake, etc.) utilisés avec Gainsight.
*   Connexion directe à Gainsight NXT plutôt que via Salesforce, jusqu'à la restauration complète de l'intégration.
*   Réinitialisation des mots de passe des utilisateurs NXT qui n'utilisent pas l'authentification unique (SSO).
*   Réautorisation de toutes les applications ou intégrations connectées qui dépendent d'identifiants ou de jetons d'utilisateur.

---
[Source](https://thehackernews.com/2025/11/gainsight-expands-impacted-customer.html){:target="_blank"}
