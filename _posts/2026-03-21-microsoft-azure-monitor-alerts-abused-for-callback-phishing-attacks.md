---
title: 'Microsoft Azure Monitor alerts abused for callback phishing attacks'
date: 2026-03-21
permalink: /posts/2026/03/21/microsoft-azure-monitor-alerts-abused-for-callback-phishing-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement de Microsoft Azure Monitor pour des campagnes de phishing par rappel

Des cybercriminels exploitent la plateforme **Microsoft Azure Monitor** pour diffuser des courriels de phishing extrêmement crédibles. En manipulant le champ de description des règles d'alerte, les attaquants génèrent des notifications légitimes concernant de prétendues factures impayées ou des transactions suspectes, incitant les victimes à appeler un numéro de téléphone frauduleux.

**Points clés :**
*   **Légitimité détournée :** Les e-mails sont envoyés directement par les serveurs officiels de Microsoft (`azure-noreply@microsoft.com`).
*   **Contournement des protections :** Comme les messages proviennent de l'infrastructure Microsoft, ils valident les protocoles SPF, DKIM et DMARC, ce qui permet de passer outre les filtres anti-spam traditionnels.
*   **Méthodologie :** Les attaquants configurent des alertes basées sur des événements de facturation et insèrent un message d'alerte falsifié dans le champ de description, incluant un faux numéro de support technique.
*   **Objectifs :** Vol d'identifiants, fraude financière ou incitation à installer des logiciels d'accès à distance (RAT).

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle (CVE), mais d'un **abus de conception fonctionnelle** de la plateforme Azure Monitor, permettant d'utiliser des champs de texte libre pour usurper des notifications de sécurité officielles.

**Recommandations :**
*   **Méfiance systématique :** Ne jamais contacter un numéro de téléphone figurant dans une alerte de sécurité non sollicitée, même si l'e-mail semble provenir d'une source légitime.
*   **Vérification indépendante :** Pour toute question relative à une facture ou une activité suspecte, connectez-vous directement à votre portail de gestion de compte via une URL officielle saisie manuellement dans votre navigateur.
*   **Sensibilisation :** Éduquer les utilisateurs sur le fait que les notifications officielles de Microsoft ne demandent généralement pas de contacter un support téléphonique par urgence pour des questions de facturation.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-azure-monitor-alerts-abused-in-callback-phishing-campaigns/){:target="_blank"}
