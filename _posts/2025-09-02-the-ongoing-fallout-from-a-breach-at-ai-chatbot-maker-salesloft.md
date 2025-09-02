---
title: 'The Ongoing Fallout from a Breach at AI Chatbot Maker Salesloft'
date: 2025-09-02
permalink: /posts/2025/09/02/the-ongoing-fallout-from-a-breach-at-ai-chatbot-maker-salesloft/
tags:
- veille-cyber
- krebs
---
**Impact Étendu de la Compromission chez Salesloft : Des Fuites de Données Généralisées**

Une importante violation de sécurité chez Salesloft, fournisseur d'un chatbot IA utilisé par de nombreuses entreprises, a entraîné le vol de jetons d'authentification. Ces jetons volés ne se limitaient pas à l'accès aux données Salesforce, mais incluaient également des centaines d'autres services en ligne intégrés à Salesloft, tels que Slack, Google Workspace, Amazon S3, Microsoft Azure et OpenAI. Des groupes de menaces comme UNC6395 sont suspectés d'avoir exploité ces jetons pour exfiltrer de grandes quantités de données à partir de multiples instances Salesforce, cherchant notamment des identifiants AWS, VPN et Snowflake pour étendre leur compromission à d'autres environnements.

Cet incident s'inscrit dans un contexte de campagnes de social engineering, incluant le vishing, ciblant des plateformes comme Salesforce. Des groupes tels que ShinyHunters, connus pour leur utilisation de l'ingénierie sociale et leur large historique de fuites de données, sont potentiellement liés à ces attaques, avec des recoupements observés dans leurs méthodes avec ceux de groupes comme Scattered Spider. Un canal Telegram, "Scattered LAPSUS$ Hunters 4.0", a également revendiqué la responsabilité de la faille Salesloft, bien que sans preuves concrètes, tout en menaçant des chercheurs et promouvant un nouveau forum de cybercriminalité.

Le phénomène de "l'étalement des autorisations" ("authorization sprawl"), où les attaquants exploitent des jetons d'accès légitimes pour se déplacer discrètement entre les systèmes, est mis en évidence comme une raison clé du succès de ces attaques. L'accès via des plateformes d'identité centralisées avec authentification unique (SSO) permet aux attaquants de rester dans les limites des ressources déjà attribuées aux utilisateurs, rendant leurs actions difficiles à détecter. Salesloft a engagé Mandiant pour enquêter sur la cause profonde de l'incident.

**Points Clés :**

*   Vol massif de jetons d'authentification chez Salesloft, affectant de nombreux services tiers.
*   Exfiltration de données à grande échelle à partir d'instances Salesforce et d'autres plateformes.
*   Recherche d'identifiants sensibles (AWS, VPN, Snowflake) par les attaquants pour un accès étendu.
*   Association potentielle avec des groupes comme ShinyHunters et Scattered Spider en raison de similitudes dans les techniques.
*   Mise en avant du concept d'"authorization sprawl" comme vecteur d'attaque efficace.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique dans le code de Salesloft ou de Salesforce n'est mentionnée comme cause directe, mais plutôt l'exploitation de jetons d'authentification volés.

**Recommandations :**

*   Invalider immédiatement tous les jetons d'authentification stockés ou connectés aux intégrations Salesloft, quel que soit le service tiers concerné.
*   Considérer les données comme potentiellement compromises et prendre des mesures de remédiation urgentes.
*   Réauthentifier la connexion entre les applications Drift et Salesforce pour invalider les jetons existants.

---
[Source](https://krebsonsecurity.com/2025/09/the-ongoing-fallout-from-a-breach-at-ai-chatbot-maker-salesloft/){:target="_blank"}
