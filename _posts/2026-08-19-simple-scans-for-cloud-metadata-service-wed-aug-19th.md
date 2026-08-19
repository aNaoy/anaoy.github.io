---
title: 'Simple Scans for Cloud Metadata Service, (Wed, Aug 19th)'
date: 2026-08-19
permalink: /posts/2026/08/19/simple-scans-for-cloud-metadata-service-wed-aug-19th/
tags:
- veille-cyber
- sans-isc
---
### Risques d'exploitation du service de métadonnées Cloud (IMDS)

Les fournisseurs de cloud utilisent l'adresse IP « link-local » `169.254.169.254` pour exposer des données de configuration aux instances virtuelles. Bien qu'inaccessible depuis l'extérieur, cette interface est devenue une cible privilégiée pour les attaques par falsification de requête côté serveur (SSRF). Une recrudescence de scans automatisés a été observée, cherchant à exploiter des vulnérabilités SSRF génériques pour exfiltrer des identifiants IAM ou des jetons de services sensibles.

**Points clés :**
*   **Accessibilité :** L'adresse `169.254.169.254` n'est pas routable, mais une vulnérabilité SSRF permet à un attaquant de forcer l'instance à interroger ce service en son nom.
*   **Menace actuelle :** Des campagnes de scans massifs et non ciblés tentent d'accéder aux chemins de métadonnées (ex: `/latest/meta-data/iam/security-credentials/`) via des vecteurs SSRF.
*   **Historique :** Ce mécanisme a été au cœur de violations de données majeures, notamment l'incident Capital One.

**Vulnérabilités :**
*   **SSRF (Server-Side Request Forgery) :** L'article ne mentionne pas de CVE spécifique, mais souligne que l'exploitation repose sur l'existence de failles SSRF dans les applications hébergées.

**Recommandations :**
*   **Adoption d'IMDSv2 :** Passer impérativement à la version 2 du service de métadonnées (IMDSv2). Contrairement à la version 1, celle-ci impose une authentification par session, rendant les requêtes SSRF simples inefficaces pour extraire des secrets.
*   **Sécurisation applicative :** Auditer les applications pour détecter et corriger toute faille SSRF permettant d'effectuer des requêtes sortantes vers des ressources internes.

---
[Source](https://isc.sans.edu/diary/rss/33260){:target="_blank"}
