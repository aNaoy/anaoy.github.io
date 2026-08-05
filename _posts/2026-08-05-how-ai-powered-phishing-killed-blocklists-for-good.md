---
title: 'How AI-powered phishing killed blocklists for good'
date: 2026-08-05
permalink: /posts/2026/08/05/how-ai-powered-phishing-killed-blocklists-for-good/
tags:
- veille-cyber
- bleepingcomp
---
### L'obsolescence des listes de blocage face au phishing dopé à l'IA

Les méthodes de défense traditionnelles basées sur les listes de blocage (blocklists) et les indicateurs de compromission (IOC) sont devenues inefficaces. L'intelligence artificielle permet désormais aux attaquants de créer, déployer et détruire des infrastructures de phishing en quelques minutes, rendant les listes de détection obsolètes avant même d'être mises à jour.

**Points clés :**
*   **Infrastructure éphémère :** 89 % des domaines de phishing sont actifs moins de deux jours. Les attaquants utilisent des services légitimes (Cloudflare, Microsoft, Google, etc.) et des techniques de contournement (bot protection, empreintes numériques) pour masquer leur activité.
*   **Industrialisation des kits (PhaaS) :** Le développement de kits de phishing (ex: *EvilTokens*, *Kali365*, *Tycoon 2FA*) est accéléré par l'IA. Ces kits sont devenus dynamiques et capables de basculer entre plusieurs vecteurs d'attaque.
*   **Mutation des attaques :** Les nouvelles menaces exploitent des comportements légitimes détournés plutôt que des vulnérabilités logicielles classiques.

**Techniques et vecteurs d'attaque mentionnés :**
*   **AiTM (Adversary-in-the-Middle) :** Interception de sessions et de jetons MFA en temps réel.
*   **ClickFix :** Manipulation du presse-papiers utilisateur pour exécuter des commandes malveillantes.
*   **Device Code Phishing :** Exploitation du processus d'authentification par code d'appareil (OAuth).
*   **Abus de services légitimes :** Utilisation des fonctions de partage des chatbots IA, des redirections OAuth, ou de l'hébergement sur des plateformes de confiance pour hériter de leur réputation.

**Recommandations pour la défense :**
*   **Détection comportementale (TTPs) :** Se concentrer sur la détection des *mécanismes* d'attaque (ex : redirection OAuth suspecte, manipulation du presse-papiers) plutôt que sur les domaines ou signatures de fichiers, qui changent constamment.
*   **Visibilité au niveau du navigateur :** La détection doit se faire au sein de la session utilisateur, là où le trafic est déchiffré, car les outils EDR et proxys réseau classiques sont aveugles face à ces techniques.
*   **Vitesse de recherche :** Réduire le temps entre la découverte d'une nouvelle technique par les chercheurs et le déploiement de règles de détection basées sur le comportement pour contrer l'industrialisation rapide par les cybercriminels.

---
[Source](https://www.bleepingcomputer.com/news/security/how-ai-powered-phishing-killed-blocklists-for-good/){:target="_blank"}
