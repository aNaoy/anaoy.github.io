---
title: 'Multiple Vulnerabilities in Frappe LMS Leading to Remote Code Execution'
date: 2026-09-15
permalink: /posts/2026/09/15/multiple-vulnerabilities-in-frappe-lms-leading-to-remote-code-execution/
tags:
- veille-cyber
- zerodaysfans
---
### Vulnérabilités critiques dans Frappe LMS : de la XSS à l'exécution de code à distance

Des chercheurs ont identifié une chaîne d'attaques dans Frappe LMS permettant à un utilisateur non privilégié de prendre le contrôle total du serveur. Cette compromission repose sur l'exploitation combinée de deux failles majeures.

#### Points clés
*   **Vecteur d'attaque :** Enchaînement d'une injection de script (XSS) pour piéger un administrateur et d'un contournement de sécurité lors de l'importation de fichiers pour exécuter du code arbitraire.
*   **Impact :** Exécution de code à distance (RCE) avec les privilèges du serveur.

#### Vulnérabilités identifiées
*   **CVE-2026-39405 (Path Traversal / RCE) :** Une absence de validation sur le nom des chapitres lors de l'importation de packages SCORM permet d'écrire des fichiers n'importe où sur le système. Un attaquant peut ainsi écraser des fichiers système (ex: `api.py`) pour y injecter un backdoor et exécuter des commandes.
*   **CVE-2026-34606 (Stored XSS) :** Le contournement du filtre HTML via l'usage détourné de la méthode `get_text()` de BeautifulSoup. En soumettant des fragments de balises inoffensifs, l'application les concatène lors de la prévisualisation pour générer un script malveillant exécutable dans le navigateur des victimes.
*   **CVE-2026-46546 (Open Redirect) :** Une injection de balises méta permettant de rediriger les utilisateurs vers des sites externes malveillants.

#### Recommandations
*   **Mise à jour :** Appliquer immédiatement les correctifs fournis par Frappe LMS (les vulnérabilités ont été corrigées courant mars 2026).
*   **Sécurisation des entrées :** Ne jamais utiliser de fonctions d'extraction ou de traitement de données (comme `get_text()`) pour générer du contenu destiné à être rendu au navigateur sans une phase stricte d'assainissement (sanitization) ou d'encodage de sortie (output encoding).
*   **Validation des chemins :** Lors de l'importation de fichiers, implémenter une validation stricte des chemins d'accès (path sanitization) pour empêcher toute sortie du répertoire de destination prévu (interdire les caractères `../`).

---
[Source](https://rhinosecuritylabs.com/research/multiple-vulnerabilities-in-frappe-lms-leading-to-remote-code-execution/){:target="_blank"}
