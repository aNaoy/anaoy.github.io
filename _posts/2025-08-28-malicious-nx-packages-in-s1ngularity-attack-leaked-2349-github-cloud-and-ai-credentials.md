---
title: 'Malicious Nx Packages in ‘s1ngularity’ Attack Leaked 2,349 GitHub, Cloud, and AI Credentials'
date: 2025-08-28
permalink: /posts/2025/08/28/malicious-nx-packages-in-s1ngularity-attack-leaked-2349-github-cloud-and-ai-credentials/
tags:
- veille-cyber
- hackernews
---
**Vol de Données par le biais de Paquets Nx Compromis**

Une attaque par chaîne d'approvisionnement a permis la publication de versions malveillantes de paquets npm populaires, notamment "nx" et certains de ses plugins. Ces versions contenaient du code conçu pour explorer le système de fichiers, collecter des identifiants et les envoyer à des dépôts GitHub contrôlés par les attaquants. Plus de 3,5 millions de téléchargements hebdomadaires du paquet nx sont concernés.

**Points Clés :**

*   **Exploitation d'une Vulnérabilité de Workflow GitHub :** L'attaque a exploité une vulnérabilité dans un workflow GitHub utilisant le déclencheur `pull_request_target`. Ce déclencheur exécute les workflows avec des permissions élevées, y compris un `GITHUB_TOKEN` avec des droits de lecture/écriture sur le dépôt.
*   **Vol d'Identifiants :** Le code malveillant, activé après l'installation des paquets compromis, scanne les fichiers texte du système pour y trouver des identifiants. Ces informations sont ensuite encodées en Base64 et envoyées à un dépôt GitHub contrôlé par l'attaquant.
*   **Modification de Fichiers de Configuration :** Les scripts malveillants ont également altéré les fichiers `.zshrc` et `.bashrc`. Ils y ont ajouté une commande `sudo shutdown -h 0` qui, si exécutée avec succès après une demande de mot de passe utilisateur, provoque l'arrêt immédiat de la machine.
*   **Utilisation Innovante des IA :** L'attaque a démontré une nouvelle méthode d'exploitation où les outils d'IA pour développeurs (comme Claude, Google Gemini, Amazon Q) ont été utilisés pour l'énumération de secrets et l'exfiltration de données sur les machines des victimes, en exploitant des drapeaux de sécurité dangereux.
*   **Impact Majeur sur les Identifiants :** Environ 90% des plus de 1 000 jetons GitHub compromis étaient toujours valides au moment de la découverte, ainsi que des dizaines d'identifiants cloud et de jetons npm. L'attaque a permis la fuite de 2 349 secrets uniques, incluant des clés OAuth GitHub, des jetons d'accès personnels (PATs), des clés API pour Google AI, OpenAI, AWS, et d'autres services.

**Versions Affectées :**

*   nx : 21.5.0, 20.9.0, 20.10.0, 21.6.0, 20.11.0, 21.7.0, 21.8.0, 20.12.0
*   @nx/devkit : 21.5.0, 20.9.0
*   @nx/enterprise-cloud : 3.2.0
*   @nx/eslint : 21.5.0
*   @nx/js : 21.5.0, 20.9.0
*   @nx/key : 3.2.0
*   @nx/node : 21.5.0, 20.9.0
*   @nx/workspace : 21.5.0, 20.9.0

Ces versions ont été retirées du registre npm.

**Vulnérabilités :**

*   Aucun identifiant CVE spécifique n'est mentionné dans l'article pour cette attaque particulière. La vulnérabilité principale découle d'une mauvaise configuration du workflow GitHub (`pull_request_target`) permettant l'exécution de code arbitraire avec des permissions élevées.

**Recommandations :**

*   **Rotation des Identifiants :** Les utilisateurs ayant installé les versions compromises doivent immédiatement faire pivoter leurs identifiants et jetons GitHub et npm.
*   **Arrêt de l'Utilisation :** Cesser d'utiliser les paquets nx compromis.
*   **Vérification des Fichiers de Configuration :** Examiner les fichiers `.zshrc` et `.bashrc` pour y détecter et supprimer toute instruction inconnue ou suspecte.
*   **Audit des Activités :** Réaliser un audit des activités GitHub et npm pour identifier toute activité suspecte.
*   **Sécurisation des Accès :** Mettre en place l'authentification à deux facteurs (2FA) pour les accès de publication, ou utiliser des mécanismes d'automatisation sécurisés.
*   **Attention aux Extensions :** Être vigilant quant aux extensions d'éditeurs de code comme l'extension Nx pour Visual Studio Code, qui peuvent être des vecteurs d'infection.

---
[Source](https://thehackernews.com/2025/08/malicious-nx-packages-in-s1ngularity.html){:target="_blank"}
