---
title: 'Writer AI Flaw Could Let Agent Previews Leak Session Tokens Across Tenants'
date: 2026-07-08
permalink: /posts/2026/07/08/writer-ai-flaw-could-let-agent-previews-leak-session-tokens-across-tenants/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "WriteOut" dans la plateforme Writer AI

Une faille de sécurité critique, baptisée **WriteOut**, a été découverte dans la plateforme d'IA générative d'entreprise **Writer**. Cette vulnérabilité permettait à un attaquant externe de compromettre le compte d'un utilisateur, indépendamment de son organisation, par le simple clic sur un lien de prévisualisation d'agent IA.

**Points clés :**
* **Isolation inter-locataires rompue :** La faille brisait l'isolement des "tenants" (locataires), permettant à un attaquant de prendre le contrôle complet du compte d'une victime.
* **Accès aux données sensibles :** Une fois le compte compromis, l'attaquant pouvait accéder aux chats privés, documents, modèles personnalisés et identifiants LLM.
* **Mécanisme d'attaque :** En exploitant la fonction de "prévisualisation en direct" (live preview), le navigateur de la victime transmettait ses cookies de session vers le bac à sable (sandbox) contrôlé par l'attaquant. Celui-ci récupérait alors le jeton de session pour usurper l'identité de la victime.
* **Contournement des protections :** L'attaquant pouvait contourner les filtres de sécurité de Writer en téléchargeant un script distant plutôt qu'en injectant du code malveillant directement dans le prompt, rendant l'activité malveillante invisible pour les contrôles basés sur le texte.

**Vulnérabilités :**
* Il n'y a pas de CVE assignée publiquement dans l'article, mais la faille concerne une rupture d'isolation de session (Session Hijacking via Cross-Tenant Preview).

**Recommandations :**
* **Correctif appliqué :** Writer a corrigé la vulnérabilité en isolant totalement les prévisualisations dans une origine distincte et en empêchant la transmission des cookies de session vers ces environnements de test.
* **Bonnes pratiques :** Les utilisateurs d'IA d'entreprise doivent rester vigilants face aux liens externes de prévisualisation et les administrateurs doivent s'assurer que les outils SaaS utilisés isolent correctement les environnements de test des données de session réelles des utilisateurs.

---
[Source](https://thehackernews.com/2026/07/writer-ai-flaw-could-let-agent-previews.html){:target="_blank"}
