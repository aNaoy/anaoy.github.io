---
title: 'Hackers target misconfigured proxies to access paid LLM services'
date: 2026-01-10
permalink: /posts/2026/01/10/hackers-target-misconfigured-proxies-to-access-paid-llm-services/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de Reconnaissance sur les Services LLM Exposés

Une campagne active, débutée fin décembre, vise à identifier et exploiter des serveurs proxy mal configurés pour accéder à des services de grands modèles de langage (LLM) commerciaux. Les attaquants, qui pourraient être des chercheurs en sécurité ou des chasseurs de bugs vu l'ampleur et le timing des actions, sondent systématiquement les points d'accès aux LLM.

L'une des opérations détectées utilise des vulnérabilités de Server-Side Request Forgery (SSRF) pour forcer les serveurs à se connecter à des infrastructures contrôlées par l'attaquant, notamment via la fonction de téléchargement de modèles d'Ollama pour injecter des URL malveillantes ou des intégrations de webhooks SMS.

Une seconde campagne, plus récente, se concentre sur l'énumération à haut volume de points d'accès LLM exposés ou mal configurés. Plus de 73 points d'accès, compatibles avec les API d'OpenAI et Google Gemini, ont été sondés durant 11 jours, générant plus de 80 000 sessions. Les modèles ciblés incluent ceux d'OpenAI (GPT-4o), Anthropic (Claude), Meta (Llama 3.x), Google (Gemini), Mistral, Alibaba (Qwen) et xAI (Grok). Les requêtes utilisées sont conçues pour être discrètes, comme de courtes salutations ou des questions factuelles, afin d'éviter les alertes de sécurité.

Bien qu'aucune exploitation post-découverte ou vol de données n'ait été formellement rapportée, l'ampleur des efforts de reconnaissance suggère une intention malveillante et des plans d'utilisation ultérieurs des informations collectées.

**Points Clés :**
*   Les attaquants recherchent activement des serveurs proxy mal configurés donnant accès à des LLM payants.
*   Des campagnes de reconnaissance à grande échelle sont en cours depuis fin décembre.
*   Des techniques comme le SSRF sont utilisées dans une opération pour injecter du code malveillant.
*   Les attaquants utilisent des requêtes discrètes pour éviter la détection.
*   L'ampleur des investigations suggère une planification en vue d'une exploitation future.

**Vulnérabilités :**
*   Server-Side Request Forgery (SSRF) : Exploité pour forcer les connexions serveur à des infrastructures externes. Le rapport ne mentionne pas de CVE spécifiques pour ces attaques, mais la technique est bien documentée.

**Recommandations :**
*   Restreindre les téléchargements de modèles Ollama aux registres de confiance.
*   Appliquer un filtrage de sortie (egress filtering).
*   Bloquer les domaines connus de rappels OAST (Out-of-band Application Security Testing) au niveau DNS.
*   Mettre en place une limitation de débit (rate-limiting) pour les systèmes autonomes (ASN) suspects.
*   Surveiller les empreintes réseau JA4 associées aux outils de scan automatisés.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-target-misconfigured-proxies-to-access-paid-llm-services/){:target="_blank"}
