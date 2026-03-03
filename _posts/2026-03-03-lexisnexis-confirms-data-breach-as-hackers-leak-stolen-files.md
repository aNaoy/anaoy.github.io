---
title: 'LexisNexis confirms data breach as hackers leak stolen files'
date: 2026-03-03
permalink: /posts/2026/03/03/lexisnexis-confirms-data-breach-as-hackers-leak-stolen-files/
tags:
- veille-cyber
- bleepingcomp
---
**Fuite de données chez LexisNexis suite à une exploitation de vulnérabilité**

La société d'analyse de données LexisNexis Legal & Professional a confirmé avoir subi une intrusion dans ses systèmes par des pirates informatiques, qui ont ensuite divulgué environ 2 Go de données volées. Le groupe de pirates FulcrumSec a revendiqué l'attaque, déclarant avoir accédé à l'infrastructure cloud de LexisNexis le 24 février en exploitant une vulnérabilité dans une application React non corrigée.

Les données dérobées, principalement des informations "legacy" antérieures à 2020, incluent des noms de clients, des identifiants utilisateurs, des contacts professionnels, des informations sur les produits utilisés, des enquêtes clients avec adresses IP, et des tickets de support. L'entreprise assure qu'aucune information sensible comme les numéros de sécurité sociale, d'identité, les informations financières, les mots de passe actifs ou les données contractuelles clients n'a été compromise.

FulcrumSec affirme avoir accédé à des tables de bases de données, des secrets stockés en clair, des enregistrements clients, des réponses d'enquêtes d'avocats, des hachages de mots de passe employés, et des informations d'infrastructure cloud. Les pirates ont notamment ciblé des utilisateurs ayant des adresses e-mail .gov, incluant des employés du gouvernement américain, des juges fédéraux, des greffiers, des avocats du ministère de la Justice et du personnel de la SEC.

LexisNexis a déclaré avoir pris des mesures pour contenir l'intrusion, notifié les forces de l'ordre et engagé un expert externe en cybersécurité. L'entreprise a également informé ses clients actuels et passés de l'incident.

**Points Clés :**

*   **Vecteur d'attaque :** Exploitation de la vulnérabilité React2Shell dans une application front-end React non patchée.
*   **Infrastructure compromise :** Infrastructure AWS de LexisNexis.
*   **Nature des données volées :** Principalement des informations "legacy" (avant 2020), incluant des informations clients et professionnelles non critiques. Aucune donnée financière ou d'identité hautement sensible n'a été affectée selon l'entreprise.
*   **Données spécifiques revendiquées par les pirates :** Tables de bases de données, secrets en clair, enregistrements clients, hachages de mots de passe, informations sur l'infrastructure cloud, profils utilisateurs (noms, e-mails, numéros de téléphone, fonctions).
*   **Ciblage spécifique :** Utilisateurs avec des adresses .gov.
*   **Action de l'entreprise :** Confirmation de l'intrusion, notification des autorités, recours à un expert externe, notification aux clients.

**Vulnérabilités :**

*   **React2Shell :** Vulnérabilité dans les applications front-end React (pas de CVE spécifique mentionné dans l'article pour cette vulnérabilité elle-même, mais le terme "React2Shell" est utilisé comme nom de la faille exploitée).

**Recommandations implicites et actions :**

*   **Maintien des systèmes à jour :** Nécessité de patcher rapidement les vulnérabilités dans les applications web, notamment les composants front-end comme React.
*   **Gestion des secrets :** Sécurisation adéquate des secrets d'infrastructure cloud (AWS Secrets Manager) pour éviter qu'ils ne soient accessibles en clair.
*   **Segmentation du réseau et contrôle d'accès :** Mettre en place des mesures pour limiter la portée d'une éventuelle compromission, comme le mentionnent les pirates concernant l'accès général d'un rôle ECS.
*   **Surveillance et détection :** Déployer des systèmes de surveillance pour détecter les accès non autorisés et les exfiltrations de données.
*   **Réponse aux incidents :** Disposer d'un plan de réponse aux incidents bien établi, incluant la notification aux forces de l'ordre et l'assistance par des experts en cybersécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/lexisnexis-confirms-data-breach-as-hackers-leak-stolen-files/){:target="_blank"}
