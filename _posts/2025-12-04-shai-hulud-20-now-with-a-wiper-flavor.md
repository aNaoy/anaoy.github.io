---
title: 'Shai Hulud 2.0, now with a wiper flavor'
date: 2025-12-04
permalink: /posts/2025/12/04/shai-hulud-20-now-with-a-wiper-flavor/
tags:
- veille-cyber
- securelist
---
### **Shai Hulud 2.0 : Nouvelle menace dans l'écosystème npm**

Une nouvelle version du malware "Shai Hulud", découvert en septembre, sévit dans l'écosystème npm. Cette variante, baptisée "Shai Hulud 2.0", est un ver malveillant en deux étapes qui se propage en compromettant des jetons npm pour republier des packages de confiance avec une charge utile malveillante. Plus de 800 packages npm ont été infectés par cette nouvelle itération. Les attaques ont touché des individus et des organisations dans le monde entier, avec une concentration notable en Russie, Inde, Vietnam, Brésil, Chine, Türkiye et France.

Le mécanisme d'infection débute lors de l'installation d'un package npm compromis. Un script initial, `setup_bun.js`, est exécuté lors de la phase de pré-installation. Ce script, délibérément peu obfusqué, simule une installation légitime du runtime JavaScript Bun tout en préparant l'environnement d'exécution pour le deuxième stage du malware. Le runtime Bun installé exécute ensuite le script malveillant principal, `bun_environment.js`, qui est fortement obfusqué.

**Points clés :**

*   **Type de menace :** Ver malveillant en deux étapes.
*   **Vecteur d'infection :** Compromission de packages npm.
*   **Mécanisme de propagation :** Utilisation de jetons npm volés pour rééditer des packages légitimes avec un payload malveillant.
*   **Activité principale :** Vol de secrets et exfiltration de données.
*   **Payload destructeur :** Effacement de fichiers en cas d'échec de l'exfiltration.

**Vulnérabilités et techniques exploitées :**

*   **Compromission de jetons npm :** Le malware recherche et exploite des jetons d'autorisation npm pour publier des versions modifiées de packages.
*   **Vol de secrets :**
    *   **Secrets GitHub :** Recherche dans les variables d'environnement et la configuration du GitHub CLI, création de workflows malveillants pour obtenir des secrets GitHub Actions.
    *   **Identifiants cloud :** Recherche dans les environnements AWS, Azure, et Google Cloud via les services de métadonnées d'instance cloud et l'utilisation de SDKs officiels.
    *   **Fichiers locaux :** Utilisation de l'outil TruffleHog pour un scan exhaustif du système de fichiers à la recherche d'identifiants.
*   **Exfiltration de données :** Utilisation d'un dépôt GitHub public comme canal de communication et de stockage pour les données volées, souvent via un jeton GitHub compromis.
*   **Auto-propagation :** Scan des fichiers de configuration `.npmrc` pour trouver des jetons npm et publication de nouvelles versions malveillantes de packages.

**Recommandations :**

*   **Surveillance des packages npm :** Examiner attentivement les dépendances installées et les versions mises à jour.
*   **Gestion des secrets :** Sécuriser et révoquer les jetons npm et GitHub potentiellement compromis. Utiliser des approches de gestion des secrets robustes pour les environnements cloud.
*   **Outils de sécurité :** Les solutions de sécurité telles que celles de Kaspersky détectent cette famille de malwares sous la dénomination HEUR:Worm.Script.Shulud.gen.
*   **Veille :** Consulter des flux d'informations sur les menaces des logiciels open source, comme le Kaspersky Open Source Software Threats Data Feed, pour identifier les packages affectés et les comportements malveillants.

---
[Source](https://securelist.com/shai-hulud-2-0/118214/){:target="_blank"}
