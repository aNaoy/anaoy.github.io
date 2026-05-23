---
title: 'Laravel-Lang PHP Packages Compromised to Deliver Cross-Platform Credential Stealer'
date: 2026-05-23
permalink: /posts/2026/05/23/laravel-lang-php-packages-compromised-to-deliver-cross-platform-credential-stealer/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement Laravel-Lang

Une campagne d'attaque par empoisonnement de la chaîne d'approvisionnement a compromis plusieurs paquets PHP de l'organisation **Laravel-Lang** (notamment `lang`, `http-statuses`, `attributes` et `actions`). Les attaquants ont publié plus de 700 versions malveillantes en un laps de temps très court, suggérant une compromission des identifiants ou de l'infrastructure de publication de l'organisation.

**Points clés :**
*   **Vecteur d'infection :** L'ajout d'un fichier `src/helpers.php` dans le `composer.json` (via `autoload.files`). Cela permet une exécution automatique et immédiate du code malveillant dès le chargement de l'application PHP, sans interaction utilisateur.
*   **Mécanisme :** Le script contacte un serveur distant (`flipboxstudio[.]info`) pour télécharger et exécuter un "stealer" multiplateforme (Windows, Linux, macOS).
*   **Exfiltration massive :** Le malware extrait une quantité considérable de données sensibles : jetons cloud (AWS, Azure, GCP), configurations Kubernetes, identifiants de dépôts (GitHub, GitLab), portefeuilles de cryptomonnaies, données de navigateurs, mots de passe de gestionnaires de coffres-forts (1Password, Bitwarden), ainsi que des clés SSH et fichiers de configuration (`.env`, `wp-config.php`).
*   **Discrétion :** Le malware utilise un hash MD5 unique par machine pour s'exécuter une seule fois et s'auto-supprime après l'exfiltration des données chiffrées en AES-256 pour limiter les traces forensiques.

**Vulnérabilités :**
*   Aucun identifiant CVE spécifique n'a été attribué, car il s'agit d'une compromission directe des dépôts (supply chain attack) plutôt que d'une faille logique dans le code source original de Laravel-Lang.

**Recommandations :**
*   **Audit immédiat :** Vérifier les versions des paquets Laravel-Lang installées et passer aux versions légitimes et sécurisées publiées après l'incident.
*   **Rotation des secrets :** Considérer comme compromis tous les jetons, clés API, mots de passe et fichiers de configuration accessibles par les applications PHP utilisant ces paquets. Une rotation immédiate de ces secrets est impérative.
*   **Surveillance :** Inspecter les logs de sortie réseau pour détecter des communications vers `flipboxstudio[.]info`.
*   **Sécurisation :** Renforcer la sécurité des accès aux pipelines CI/CD et aux comptes de publication sur les gestionnaires de paquets (Packagist).

---
[Source](https://thehackernews.com/2026/05/laravel-lang-php-packages-compromised.html){:target="_blank"}
