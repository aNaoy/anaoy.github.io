---
title: 'Researcher Publishes GitLab RCE PoC Letting Authenticated Users Run Commands as Git'
date: 2026-07-25
permalink: /posts/2026/07/25/researcher-publishes-gitlab-rce-poc-letting-authenticated-users-run-commands-as-git/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité RCE critique dans GitLab via la bibliothèque Oj

Une faille d'exécution de code à distance (RCE) a été identifiée dans GitLab, permettant à tout utilisateur authentifié disposant de droits d'écriture sur un projet d'exécuter des commandes avec les privilèges de l'utilisateur `git`. Bien qu'un correctif soit disponible depuis le 10 juin, celui-ci n'avait pas été classé comme une mise à jour de sécurité, rendant son installation non prioritaire pour de nombreux administrateurs.

**Points clés :**
* **Origine de la faille :** La vulnérabilité exploite deux erreurs de corruption mémoire dans la bibliothèque Ruby `Oj` (analyseur JSON écrit en C), utilisées par le moteur de rendu de notebooks de GitLab (`ipynbdiff`).
* **Méthode d'attaque :** Un attaquant téléverse des fichiers `.ipynb` (Jupyter notebooks) spécialement conçus pour provoquer une fuite de mémoire (heap pointer) puis corrompre la pile, permettant de rediriger le flux d'exécution vers `system()`.
* **Impact :** Exécution de commandes arbitraires. Selon l'isolation de l'instance, cela peut compromettre le code source, les secrets d'application, les identifiants de services et les données CI/CD.
* **Absence de transparence :** GitLab n'a pas publié de CVE ni de score CVSS pour cette vulnérabilité, ce qui a pu retarder les correctifs dans les environnements auto-hébergés.

**Vulnérabilités :**
* Deux vulnérabilités de corruption mémoire dans la bibliothèque **Oj (version 3.17.1 et inférieures)**. Aucune CVE n'a été officiellement attribuée par GitLab à ce jour.

**Recommandations :**
* **Mise à jour immédiate :** Appliquer les correctifs GitLab vers les versions **18.10.8**, **18.11.5** ou **19.0.2** au minimum.
* **Vérification :** Contrôler spécifiquement la version du composant `Webservice` (Puma) au sein des images de déploiement, car la version des charts Helm ou de l'opérateur ne reflète pas toujours la réalité du binaire en exécution.
* **Environnements non supportés :** Les instances utilisant des versions antérieures à 15.2 ne bénéficiant plus de backports de sécurité, une mise à niveau complète vers une branche supportée est impérative.

---
[Source](https://thehackernews.com/2026/07/researcher-publishes-gitlab-rce-poc.html){:target="_blank"}
