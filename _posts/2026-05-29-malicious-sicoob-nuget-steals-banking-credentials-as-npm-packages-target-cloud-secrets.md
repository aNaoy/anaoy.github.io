---
title: 'Malicious Sicoob NuGet Steals Banking Credentials as npm Packages Target Cloud Secrets'
date: 2026-05-29
permalink: /posts/2026/05/29/malicious-sicoob-nuget-steals-banking-credentials-as-npm-packages-target-cloud-secrets/
tags:
- veille-cyber
- hackernews
---
### Recrudescence des attaques sur la chaîne d'approvisionnement logicielle

Le paysage de la cybersécurité fait face à une vague croissante de logiciels malveillants diffusés via des dépôts officiels comme NuGet et npm. Une campagne notable a ciblé les développeurs utilisant le package NuGet « **Sicoob.Sdk** » (versions 2.0.0 à 2.0.4), qui se faisait passer pour un kit de développement officiel pour la banque brésilienne Sicoob. Ce package, également favorisé par les algorithmes de recherche, exfiltrait des identifiants clients, des certificats PFX et des données de paiement Boleto vers un serveur tiers. Parallèlement, 14 packages npm malveillants ont été identifiés pour le vol de secrets cloud (AWS, HashiCorp Vault, CI/CD).

**Points clés :**
* **Manipulation de la confiance :** Les attaquants ne se contentent plus du simple typosquatting ; ils créent des packages à l'apparence légitime (« manufactured legitimacy ») pour s'intégrer dans les workflows de développement réels.
* **Discordance :** Il existe souvent un décalage entre le dépôt GitHub légitime (propre) et le code compilé distribué sur les plateformes de paquets.
* **Risques systémiques :** La compromission d'outils de développement permet une expansion rapide (« worm-like ») à travers les pipelines CI/CD, exposant des organisations entières.

**Vulnérabilités :**
* Absence de CVE spécifique identifiée (attaques basées sur l'ingénierie sociale et l'empoisonnement de paquets tiers).
* Exploitation de la confiance accordée aux gestionnaires de paquets (NuGet/npm).

**Recommandations :**
* **Audit immédiat :** Supprimer le package `Sicoob.Sdk` et auditer les logs d'authentification/API pour toute activité suspecte.
* **Révocation des secrets :** Considérer tout certificat PFX et mot de passe associés utilisés avec le package comme compromis ; procéder à une rotation immédiate des clés et désactiver les identifiants clients affectés.
* **Sécurisation des processus :** Mettre en place une validation rigoureuse des dépendances tierces et limiter les privilèges d'accès dans les pipelines CI/CD pour réduire l'impact d'une éventuelle compromission d'un package.
* **Vigilance accrue :** Ne pas se fier uniquement à la popularité apparente d'un package dans les résultats de recherche ou sur les registres publics.

---
[Source](https://thehackernews.com/2026/05/malicious-sicoob-nuget-steals-banking.html){:target="_blank"}
