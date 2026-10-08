---
title: '16 Malicious Firefox Extensions Pose as Rabby and OKX Wallets to Steal Recovery Phrases'
date: 2026-10-08
permalink: /posts/2026/10/08/16-malicious-firefox-extensions-pose-as-rabby-and-okx-wallets-to-steal-recovery-phrases/
tags:
- veille-cyber
- hackernews
---
### Vague de 16 extensions Firefox malveillantes ciblant les portefeuilles crypto

Des chercheurs en cybersécurité ont identifié 16 extensions malveillantes sur Firefox se faisant passer pour des portefeuilles légitimes (Rabby et OKX) ou des outils utilitaires. Ces modules sont conçus pour intercepter et exfiltrer les phrases de récupération (seed phrases) et les clés privées des utilisateurs vers des serveurs contrôlés par des attaquants via Cloudflare Workers.

**Points clés :**
* **Mode opératoire :** Les extensions utilisent des interfaces clonées pour tromper les utilisateurs lors de l'importation de leur portefeuille.
* **Persistance de la menace :** Cette campagne est une réitération d'attaques précédentes, démontrant une rotation constante des noms, versions et identifiants pour échapper à la détection tout en réutilisant la même infrastructure.
* **Impact :** Bien que ces extensions aient été supprimées de la boutique officielle le 5 octobre 2026, tout utilisateur ayant saisi ses secrets dans ces interfaces doit considérer ses comptes comme compromis.
* **Contexte élargi :** Le problème des extensions malveillantes est généralisé, touchant également Chrome et Edge, avec des vecteurs variés : espionnage de conversations IA, vol de cookies de session (compte Google) ou redirection vers des pages de phishing.

**Vulnérabilités :**
Aucune CVE spécifique n'est associée à ces extensions malveillantes, car il s'agit de logiciels conçus intentionnellement à des fins malveillantes (logiciels espions/voleurs) plutôt que d'exploits techniques sur des vulnérabilités de navigateur.

**Recommandations :**
* **Réaction immédiate :** Si une extension suspecte a été utilisée, créez immédiatement un nouveau portefeuille sur un système propre et transférez-y vos actifs.
* **Audit des extensions :** Passez en revue vos extensions installées et supprimez celles qui ne sont plus nécessaires ou dont l'utilité semble douteuse.
* **Gestion en entreprise :** Les organisations doivent auditer les extensions dans leurs environnements gérés et déployer des outils de surveillance comportementale pour détecter les activités suspectes au niveau du navigateur.

---
[Source](https://thehackernews.com/2026/10/16-malicious-firefox-extensions-pose-as.html){:target="_blank"}
