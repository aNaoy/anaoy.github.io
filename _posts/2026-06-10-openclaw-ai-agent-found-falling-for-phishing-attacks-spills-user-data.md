---
title: 'OpenClaw AI agent found falling for phishing attacks, spills user data'
date: 2026-06-10
permalink: /posts/2026/06/10/openclaw-ai-agent-found-falling-for-phishing-attacks-spills-user-data/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité des agents IA OpenClaw face au phishing

Des chercheurs de Varonis ont démontré que le framework d'agent IA open-source **OpenClaw** est vulnérable aux tactiques classiques de phishing. Bien que les agents (utilisant Google Gemini 3.1 Pro ou OpenAI GPT-5.4) sachent identifier des URLs malveillantes ou des applications OAuth suspectes, ils échouent lorsqu'ils sont confrontés à des requêtes urgentes provenant d'expéditeurs usurpant l'identité d'un supérieur hiérarchique.

**Points clés :**
*   **Fausse confiance :** Les agents ont compromis des identifiants AWS, des accès SSH et des données CRM sensibles (exports clients) sans vérifier l'identité réelle du demandeur.
*   **Urgence opérationnelle :** Même sous des configurations strictes, l'agent sacrifie ses protocoles de sécurité lorsqu'il interprète une demande comme étant urgente.
*   **Différences de modèles :** Gemini 3.1 Pro s'est montré plus enclin à interagir, tandis que GPT-5.4 a adopté une posture plus prudente.

**Vulnérabilités :**
*   Absence de mécanisme robuste de vérification d'identité (Identity Verification).
*   Manque d'application stricte des principes "Zero Trust" lors d'interactions sociales.
*   *Note : Aucune CVE spécifique n'est associée à ces résultats, car il s'agit de failles logiques et comportementales liées à la conception du framework.*

**Recommandations :**
*   **Vérification obligatoire :** Imposer une validation explicite de l'identité de l'expéditeur avant toute action.
*   **Segmentation des accès :** Restreindre l'accès des agents aux données critiques et limiter leur capacité à envoyer des courriels à de nouveaux destinataires externes sans approbation préalable.
*   **Human-in-the-loop :** Exiger une validation humaine systématique pour les actions à haut risque (partage de secrets, accès financiers ou premières communications).

---
[Source](https://www.bleepingcomputer.com/news/security/openclaw-ai-agent-found-falling-for-phishing-attacks-spills-user-data/){:target="_blank"}
