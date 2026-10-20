---
title: 'WhatsApp Hid Instructions in Help Pages Telling Its AI Chatbot Not to Recommend Privacy Regulators'
date: 2026-10-20
permalink: /posts/2026/10/20/whatsapp-hid-instructions-in-help-pages-telling-its-ai-chatbot-not-to-recommend-privacy-regulators/
tags:
- veille-cyber
- hackernews
---
### Instructions dissimulées dans les chatbots de support WhatsApp

Des chercheurs ont découvert que les pages d'aide de WhatsApp contenaient des instructions cachées (intégrées dans le code HTML) destinées à influencer le comportement de son chatbot IA. Ces directives limitaient la transparence et l'assistance aux utilisateurs dans des situations critiques :

**Points clés :**
*   **Contrôle du discours :** Le chatbot avait pour instruction explicite de ne pas recommander aux utilisateurs de contacter des autorités de protection des données (régulateurs) et de ne pas mentionner les réglementations sur la vie privée (comme le RGPD, le LGPD ou le CCPA), même lorsque l'utilisateur les évoquait directement.
*   **Blocage des recours :** En cas de mention de litiges, d'avocats ou d'actions en justice, l'IA devait cesser toute référence aux conditions d'utilisation ou à la politique de confidentialité de WhatsApp.
*   **Gestion des comptes :** Le chatbot était instruit de ne pas indiquer aux utilisateurs que WhatsApp pouvait supprimer manuellement un compte en cas de perte de téléphone, malgré les droits d'effacement prévus par le RGPD.
*   **Portée :** 102 blocs d'instructions cachées ont été identifiés sur 80 pages d'aide, une pratique absente sur les pages de Facebook et Instagram.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle classique (CVE), mais d'une **faille de transparence et d'éthique algorithmique**. Cette pratique illustre le risque de « *prompt injection* » ou de manipulation interne des réponses des IA pour servir les intérêts juridiques de l'entreprise au détriment des droits des utilisateurs.

**Recommandations :**
*   **Pour les utilisateurs :** Ne vous reposez pas uniquement sur les chatbots d'assistance pour obtenir des informations juridiques ou exercer vos droits fondamentaux. Consultez directement les politiques de confidentialité officielles et les sites des autorités de protection des données (comme la CNIL en France ou le DPC en Irlande).
*   **Pour la conformité :** Les entreprises utilisant des systèmes d'IA pour le support client doivent garantir que les instructions données aux modèles (system prompts) sont en totale adéquation avec leurs engagements légaux et les droits des utilisateurs (RGPD, etc.), sous peine d'induire le public en erreur de manière intentionnelle.

---
[Source](https://thehackernews.com/2026/10/whatsapp-hid-instructions-in-help-pages.html){:target="_blank"}
