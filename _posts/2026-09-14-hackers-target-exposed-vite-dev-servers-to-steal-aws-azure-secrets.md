---
title: 'Hackers target exposed Vite dev servers to steal AWS, Azure secrets'
date: 2026-09-14
permalink: /posts/2026/09/14/hackers-target-exposed-vite-dev-servers-to-steal-aws-azure-secrets/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne d'exploitation active ciblant les serveurs Vite

Une campagne de cyberattaques massive exploite des serveurs de développement Vite exposés sur Internet pour dérober des identifiants AWS, Azure, des fichiers de configuration Terraform et des variables d'environnement critiques. Les attaquants utilisent des techniques de balayage automatisé pour extraire des fichiers sensibles en texte clair.

**Points clés :**
* **Vecteur d'attaque :** Manipulation des paramètres de requête HTTP (`?raw`, `?import&raw`, etc.) pour contourner les contrôles d'accès.
* **Cibles :** Fichiers `.env`, configurations cloud (AWS/Azure), fichiers système (`/etc/passwd`) et état Terraform.
* **Origine :** Utilisation d'adresses IP Google Cloud pour masquer les activités, principalement depuis les États-Unis, la Belgique et les Pays-Bas.
* **Techniques avancées :** Utilisation de variantes de traversée de répertoires et d'encodage double pour déjouer les pare-feux applicatifs (WAF) et les proxys inversés.

**Vulnérabilités exploitées :**
* **CVE-2026-39364 :** Vulnérabilité majeure permettant le contournement du contrôle d'accès aux fichiers (Vite 7.1.0-7.3.2 et 8.x avant 8.0.5).
* **Autres failles identifiées :** CVE-2025-30208, CVE-2025-31125 et CVE-2024-45811.

**Recommandations :**
* **Mise à jour :** Appliquer immédiatement les derniers correctifs de sécurité pour Vite.
* **Configuration réseau :** Ne pas exposer les serveurs de développement (port 5173) sur Internet ; privilégier l'accès via localhost ou des accès restreints.
* **Sécurisation :** Bloquer les requêtes suspectes vers `/@fs/` et ignorer les requêtes provenant de robots indexeurs.
* **Remédiation :** En cas d'exposition avérée, procéder au renouvellement immédiat de tous les secrets, jetons d'accès et identifiants cloud accessibles par le système compromis.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-target-exposed-vite-dev-servers-to-steal-aws-azure-secrets/){:target="_blank"}
