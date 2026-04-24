---
title: 'Bitwarden CLI npm package compromised to steal developer credentials'
date: 2026-04-24
permalink: /posts/2026/04/24/bitwarden-cli-npm-package-compromised-to-steal-developer-credentials/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement : Le paquet npm Bitwarden CLI

Le paquet `@bitwarden/cli` (version 2026.4.0) a été compromis le 22 avril 2026 pendant environ 90 minutes. Cette attaque par chaîne d'approvisionnement, liée à une faille chez Checkmarx, a permis d'injecter un logiciel malveillant visant les environnements de développement.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation d'une action GitHub compromise dans le pipeline CI/CD de Bitwarden pour injecter du code malveillant dans le paquet npm.
*   **Mécanisme :** Le malware télécharge le runtime Bun pour exécuter un script obfuscé (`bw1.js`) capable de voler des secrets.
*   **Exfiltration :** Les données volées (clés SSH, tokens npm/GitHub, identifiants cloud AWS/Azure/GCP) sont chiffrées et exfiltrées via la création de dépôts GitHub publics, identifiés par la chaîne « Shai-Hulud: The Third Coming ».
*   **Propagation :** Le malware utilise les identifiants dérobés pour infecter d'autres paquets maintenus par la victime.
*   **Impact limité :** Bitwarden confirme que les données des coffres-forts des utilisateurs finaux et les systèmes de production n'ont pas été compromis.

**Vulnérabilités :**
*   Aucune CVE spécifique n'a été attribuée, l'incident étant une attaque directe sur la chaîne d'approvisionnement (Supply Chain Attack) exploitant des outils de développement tiers (Checkmarx).

**Recommandations :**
*   **Rotation immédiate :** Les développeurs ayant installé la version 2026.4.0 doivent considérer leurs systèmes comme compromis.
*   **Réinitialisation des secrets :** Renouveler tous les identifiants et tokens potentiellement exposés, en particulier ceux liés aux pipelines CI/CD, aux accès cloud et aux environnements de développement (clés SSH, tokens npm/GitHub).
*   **Audit de sécurité :** Vérifier l'historique des dépôts GitHub associés pour détecter d'éventuels dépôts suspects créés à votre insu.

---
[Source](https://www.bleepingcomputer.com/news/security/bitwarden-cli-npm-package-compromised-to-steal-developer-credentials/){:target="_blank"}
