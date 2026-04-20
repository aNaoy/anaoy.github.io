---
title: 'Vercel Breach Tied to Context AI Hack Exposes Limited Customer Credentials'
date: 2026-04-20
permalink: /posts/2026/04/20/vercel-breach-tied-to-context-ai-hack-exposes-limited-customer-credentials/
tags:
- veille-cyber
- hackernews
---
### Intrusion chez Vercel : une attaque par rebond via Context.ai

Vercel a subi une intrusion dans ses systèmes internes suite à la compromission d'un compte employé via l'outil tiers Context.ai. L'attaquant a exploité des jetons OAuth pour accéder à l'environnement Google Workspace de l'entreprise, permettant ainsi de consulter certaines variables d'environnement non marquées comme « sensibles ». Le groupe ShinyHunters a revendiqué l'attaque et tente de vendre les données dérobées.

**Points clés :**
* **Vecteur initial :** Un employé de Context.ai a été infecté par le logiciel malveillant **Lumma Stealer** (suite au téléchargement de scripts de triche pour jeux vidéo), permettant le vol de ses identifiants et jetons OAuth.
* **Escalade :** L'attaquant a utilisé ces jetons pour s'introduire dans le Google Workspace de Vercel, bénéficiant de permissions excessives accordées par l'utilisateur lors de l'intégration de l'outil tiers.
* **Impact :** Accès potentiel à des variables d'environnement non protégées et compromission des identifiants d'un sous-ensemble limité de clients.

**Vulnérabilités :**
* **Supply Chain Attack (Escalade) :** Utilisation d'un accès tiers compromis (Context.ai) pour pivoter vers l'infrastructure de Vercel.
* **Shadow IT / Permissions OAuth :** Octroi de permissions « Autoriser tout » (Allow All) à des outils tiers, facilitant l'accès non autorisé aux ressources d'entreprise.
* **Malware :** Infection par *Lumma Stealer* (non listé sous une CVE unique, mais associé à des vecteurs de vol d'informations identifiés).

**Recommandations :**
* **Vérification OAuth :** Examiner et révoquer l'application OAuth suspecte (`110671459871-30f1spbu0hptbs60cb4vsmv79i7bbvqj.apps.googleusercontent.com`).
* **Gestion des secrets :** Auditer et faire pivoter les variables d'environnement ; utiliser exclusivement la fonctionnalité « variables d'environnement sensibles » pour les secrets.
* **Surveillance :** Analyser les logs d'activité à la recherche d'actions suspectes et inspecter les déploiements récents pour détecter toute anomalie.
* **Sécurisation :** Appliquer une protection minimale de type « Standard » sur tous les déploiements et révoquer les jetons de protection de déploiement (Deployment Protection tokens) si nécessaire.

---
[Source](https://thehackernews.com/2026/04/vercel-breach-tied-to-context-ai-hack.html){:target="_blank"}
