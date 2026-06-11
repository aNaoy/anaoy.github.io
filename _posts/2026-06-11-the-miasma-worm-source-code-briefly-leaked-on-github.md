---
title: 'The ‘Miasma’ worm source code briefly leaked on GitHub'
date: 2026-06-11
permalink: /posts/2026/06/11/the-miasma-worm-source-code-briefly-leaked-on-github/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite du code source du ver Miasma : une menace pour la supply chain

Le framework « Miasma », un ver spécialisé dans le vol d'identifiants et les attaques par chaîne d'approvisionnement, a vu son code source délibérément rendu public sur GitHub. Dérivé du ver Shai-Hulud, cet outil permet une propagation autonome en infectant les machines des développeurs pour corrompre des dépôts de logiciels légitimes.

**Points clés :**
* **Fonctionnement autonome :** Miasma n'utilise pas de serveur C2 traditionnel, il exploite directement l'infrastructure GitHub pour ses opérations.
* **Polyvalence destructive :** Il vole des identifiants (cloud, CI/CD, K8s, gestionnaires de mots de passe), empoisonne des outils de codage par IA et se déplace latéralement via SSH ou AWS SSM.
* **Mécanisme de survie :** Un « dead-man switch » surveille la validité des tokens volés. Si le jeton est révoqué, le malware exécute une commande de suppression massive (`rm -rf`) sur les dossiers personnels de la victime.
* **Évasion :** Le malware intègre un pipeline de build en cinq étapes utilisant le chiffrement AES-256-GCM et une obfuscation complexe pour rendre chaque payload unique et difficile à détecter par signature.

**Vulnérabilités :**
* Aucune CVE spécifique n'est associée, le malware exploitant les vecteurs de confiance des écosystèmes open-source (npm, PyPI, RubyGems) et les mauvaises configurations des environnements de développement et CI/CD.

**Recommandations :**
* **Verrouillage des dépendances :** Utiliser des fichiers de verrouillage (lockfiles) pour figer les versions des dépendances.
* **Gestion du cycle de vie des mises à jour :** Imposer un délai de plusieurs jours avant d'adopter les nouvelles versions de paquets afin de détecter d'éventuelles compromissions.
* **Isolement :** Valider rigoureusement toutes les nouvelles versions et les builds dans des environnements de test isolés (sandbox).
* **Monitoring :** Surveiller les accès aux secrets et aux jetons d'API dans les pipelines CI/CD.

---
[Source](https://www.bleepingcomputer.com/news/security/the-miasma-worm-source-code-briefly-leaked-on-github/){:target="_blank"}
