---
title: 'Cybersecurity firms targeted by fraudulent OpenAI organization invites'
date: 2026-06-26
permalink: /posts/2026/06/26/cybersecurity-firms-targeted-by-fraudulent-openai-organization-invites/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de « locataires empoisonnés » sur OpenAI

Des cybercriminels exploitent le système d'invitation légitime d'OpenAI pour créer de faux espaces de travail (« tenants ») au nom d'entreprises réelles, visant principalement les secteurs de la cybersécurité et de la technologie. L'objectif est d'inciter les employés à rejoindre ces espaces pour y partager des données sensibles (code source, documents internes, stratégie) via des requêtes ChatGPT.

**Points clés :**
*   **Tactique de légitimité :** Les invitations sont envoyées directement depuis les serveurs d'OpenAI, ce qui permet de contourner les filtres anti-spam et les authentifications d'e-mails (SPF, DKIM, DMARC).
*   **Ciblage précis :** Les attaquants effectuent une reconnaissance préalable pour cibler des employés spécifiques par leur adresse e-mail professionnelle.
*   **Dissimulation :** Les attaquants ajoutent une carte bancaire au compte de facturation du faux tenant pour renforcer l'apparence de légitimité.
*   **Abus de plateforme :** Cette méthode illustre une tendance croissante où des services SaaS légitimes sont utilisés comme vecteurs d'attaque, rendant la détection extrêmement difficile.

**Vulnérabilités :**
*   Aucune CVE n'est associée, car il s'agit d'un **abus de fonctionnalités légitimes** (design flaw) plutôt que d'une faille technique logicielle. Le système d'OpenAI permet à n'importe quel utilisateur de créer une organisation et d'inviter des tiers, sans restreindre le nom de l'organisation à un domaine validé.

**Recommandations :**
*   **Sensibilisation :** Former les employés à la méfiance vis-à-vis des invitations inattendues, même si elles proviennent d'expéditeurs officiels.
*   **Vigilance sur les domaines :** Apprendre aux utilisateurs à vérifier systématiquement si le domaine de l'inviteur correspond bien à celui de l'entreprise (bien qu'OpenAI affiche un avertissement, celui-ci est souvent peu visible).
*   **Audit et monitoring :** Surveiller les adhésions des employés aux organisations SaaS tierces et restreindre l'usage d'outils non approuvés par le service informatique au sein de l'organisation.

---
[Source](https://www.bleepingcomputer.com/news/security/cybersecurity-firms-targeted-by-fraudulent-openai-organization-invites/){:target="_blank"}
