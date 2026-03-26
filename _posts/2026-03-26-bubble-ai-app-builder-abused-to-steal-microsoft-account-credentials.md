---
title: 'Bubble AI app builder abused to steal Microsoft account credentials'
date: 2026-03-26
permalink: /posts/2026/03/26/bubble-ai-app-builder-abused-to-steal-microsoft-account-credentials/
tags:
- veille-cyber
- bleepingcomp
---
### Abus de la plateforme Bubble pour le hameçonnage de comptes Microsoft

Des cybercriminels exploitent la plateforme de développement « no-code » Bubble pour héberger des applications malveillantes. En utilisant l'infrastructure légitime de Bubble (domaine `*.bubble.io`), les attaquants contournent les filtres de sécurité des e-mails, car le domaine est considéré comme fiable.

**Points clés :**
*   **Méthodologie :** Les attaquants créent des applications via Bubble qui redirigent les victimes vers de faux portails de connexion Microsoft, souvent protégés par des vérifications Cloudflare pour éviter l'analyse automatisée.
*   **Technique d'évasion :** Le code généré par Bubble, riche en JavaScript complexe et en structures *Shadow DOM*, trompe les outils d'analyse statique qui interprètent le site comme une application fonctionnelle et légitime.
*   **Risques :** Vol d'identifiants et de données sensibles (e-mails, calendriers) liées aux comptes Microsoft 365.
*   **Évolution :** Cette technique risque d'être rapidement intégrée aux plateformes de « Phishing-as-a-Service » (PhaaS), facilitant son adoption par des attaquants moins expérimentés.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, car il s'agit d'un détournement d'usage d'une plateforme légitime (abus de confiance) plutôt que d'une faille logicielle classique.

**Recommandations :**
*   **Vigilance accrue :** Sensibiliser les utilisateurs à vérifier systématiquement l'URL réelle de connexion, même si l'e-mail semble provenir d'une source fiable ou si le lien pointe vers une plateforme connue.
*   **Sécurité des accès :** Déployer des solutions d'authentification multifacteur (MFA) robustes (idéalement basées sur FIDO2/WebAuthn) pour contrer les attaques de type *Adversary-in-the-Middle* (AiTM).
*   **Filtrage :** Mettre à jour les politiques de filtrage Web pour inspecter plus finement les redirections provenant de plateformes de développement, même celles réputées sûres.

---
[Source](https://www.bleepingcomputer.com/news/security/bubble-ai-app-builder-abused-to-steal-microsoft-account-credentials/){:target="_blank"}
