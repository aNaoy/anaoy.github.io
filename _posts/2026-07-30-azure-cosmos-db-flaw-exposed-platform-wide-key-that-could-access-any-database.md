---
title: 'Azure Cosmos DB Flaw Exposed Platform-Wide Key That Could Access Any Database'
date: 2026-07-30
permalink: /posts/2026/07/30/azure-cosmos-db-flaw-exposed-platform-wide-key-that-could-access-any-database/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité CosmosEscape : compromission cross-tenant sur Azure Cosmos DB

Une faille critique, baptisée **CosmosEscape** et découverte par les chercheurs de Wiz, a exposé l'intégralité des bases de données Azure Cosmos DB à un risque d'accès non autorisé. Cette vulnérabilité permettait à un attaquant de s'extraire de l'environnement isolé (sandbox) du moteur de requêtes Gremlin pour exécuter du code arbitraire sur les passerelles multi-locataires de Microsoft.

**Points clés :**
* **Mécanisme d'attaque :** La faille exploitait une mauvaise gestion de la réflexion .NET au sein du moteur Gremlin, permettant de passer de l'exécution de requêtes à l'exécution de code sur le serveur.
* **Impact étendu :** Une fois le contrôle de la passerelle obtenu, les chercheurs ont pu accéder à un "Cosmos Master Key" et au répertoire de configuration global. Cela donnait un accès complet (lecture/écriture) aux bases de données de n'importe quel client Azure, indépendamment de la région, du locataire ou du type d'API (SQL, MongoDB, Cassandra, Gremlin).
* **Contournement des protections :** L'attaque permettait de s'affranchir des règles de segmentation réseau, car l'exécution du code se situait à l'intérieur même de l'infrastructure de service de Microsoft.
* **État de la correction :** Microsoft a neutralisé le point d'entrée vulnérable en 48 heures suite au signalement en novembre 2025, et a finalisé la suppression de la clé maîtresse globale en juillet 2026. Aucun signe d'exploitation malveillante en dehors des recherches de Wiz n'a été détecté.

**Vulnérabilités :**
* Aucune référence **CVE** n'a été publiée pour cette faille.

**Recommandations :**
* **Pour les utilisateurs :** Microsoft indique qu'aucune action corrective n'est requise de la part des clients, la vulnérabilité ayant été corrigée au niveau de la plateforme. 
* **Bonnes pratiques :** Bien que l'infrastructure ait été sécurisée, il demeure essentiel de suivre les principes de moindre privilège pour les accès aux bases de données et d'utiliser des outils de surveillance et de journalisation pour détecter toute activité inhabituelle sur les ressources cloud.

---
[Source](https://thehackernews.com/2026/07/azure-cosmos-db-flaw-exposed-platform.html){:target="_blank"}
