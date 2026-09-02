---
title: 'AI Agents Are Now Emailing Me with Their Security Concerns'
date: 2026-09-02
permalink: /posts/2026/09/02/ai-agents-are-now-emailing-me-with-their-security-concerns/
tags:
- veille-cyber
- schneier
---
### L'émergence des agents autonomes : nouveaux enjeux de sécurité

Un agent autonome utilisant un modèle Claude a mené une expérimentation sur les mécanismes de défense web actuels. L'analyse révèle des failles structurelles dans la manière dont les services en ligne gèrent l'automatisation, tout en mettant en lumière des tactiques défensives émergentes contre les IA.

**Points clés :**
*   **Absence de canal pour les agents déclarés :** Les systèmes anti-bot traitent toute connexion automatisée comme malveillante par défaut, indépendamment du fait que l'agent déclare honnêtement sa nature. Cela incite les développeurs d'IA à privilégier la dissimulation.
*   **Passivité de la sécurité réseau :** La délivrabilité des emails par des machines autonomes repose largement sur la clémence des grands fournisseurs (Google, Proton) plutôt que sur des politiques de sécurité strictes, l'infrastructure Internet étant vulnérable à l'usurpation d'identité logicielle.
*   **"ASCII smuggling" défensif :** Certains sites utilisent des caractères Unicode invisibles ou des instructions cachées (reverse prompt injection) pour piéger les agents autonomes qui scannent les formulaires, une première forme de défense technique ciblée contre le traitement automatisé de texte.

**Vulnérabilités :**
*   **Absence de filtrage par réputation réelle :** Les contrôles se basent sur des heuristiques superficielles (IP de datacenters, âge du compte, captchas) plutôt que sur une authentification robuste.
*   **Exposition d'API non sécurisées :** Des instances de plateformes (ex: Lemmy) exposent des questions d'inscription via des API ouvertes, permettant aux agents de collecter et d'analyser ces défis défensifs.
*   **Dépendance à la configuration DNS :** Le manque de rigueur dans l'application des enregistrements PTR (Reverse DNS) permet aux bots de contourner les restrictions d'envoi d'emails.

**Recommandations :**
*   **Standardiser l'identification des agents :** Créer des protocoles permettant aux bots de se déclarer officiellement afin de mieux différencier le trafic légitime de l'automatisation malveillante.
*   **Renforcer l'analyse des formulaires :** Passer outre les simples tests de Turing (captchas) pour implémenter des vérifications contextuelles plus dynamiques, tout en restant vigilant face à l'injection de prompts.
*   **Durcir les politiques de messagerie :** Imposer des contrôles de sécurité stricts (SPF, DKIM, DMARC et PTR) pour valider l'origine des flux mails, empêchant ainsi les agents non autorisés de se faire passer pour des serveurs légitimes.

---
[Source](https://www.schneier.com/blog/archives/2026/09/ai-agents-are-now-emailing-me-with-their-security-concerns.html){:target="_blank"}
