---
title: 'Cursor AI editor lets repos “autorun” malicious code on devices'
date: 2025-09-10
permalink: /posts/2025/09/10/cursor-ai-editor-lets-repos-autorun-malicious-code-on-devices/
tags:
- veille-cyber
- bleepingcomp
---
**Code Editor Cursor: Exécution Automatique de Code Malveillant**

Une faille de sécurité dans l'éditeur de code Cursor, un environnement de développement intégré (IDE) basé sur Visual Studio Code (VS Code) et intégrant des assistants IA, permet l'exécution automatique de tâches malveillantes dès l'ouverture d'un dépôt. Les acteurs malveillants peuvent ainsi déployer des logiciels malveillants, détourner des environnements de développement, ou voler des identifiants et des jetons API sans intervention de l'utilisateur.

**Points Clés :**

*   Cursor désactive par défaut la fonctionnalité "Workspace Trust" de VS Code, qui empêche l'exécution automatique de tâches sans consentement explicite.
*   La création d'un fichier `.vscode/tasks.json` malveillant dans un dépôt public suffit à déclencher le code nuisible lors de l'ouverture du projet dans Cursor.
*   VS Code, en configuration par défaut, n'est pas affecté par cette vulnérabilité car il n'exécute pas les fichiers de tâche automatiquement.

**Vulnérabilités :**

Aucun identifiant CVE spécifique n'est mentionné dans l'article pour cette vulnérabilité.

**Recommandations :**

*   **Pour les utilisateurs de Cursor :**
    *   Activer manuellement la fonctionnalité "Workspace Trust" dans Cursor.
    *   Utiliser un éditeur de texte basique pour ouvrir des dépôts potentiellement malveillants.
    *   Vérifier la source et le contenu des dépôts avant de les ouvrir.
    *   Éviter d'exporter des identifiants sensibles globalement dans les profils de shell.
*   **Pour les développeurs de Cursor :** Bien que l'équipe Cursor ait indiqué ne pas vouloir réactiver la fonction "Workspace Trust" par défaut, ils prévoient de mettre à jour leurs recommandations de sécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/cursor-ai-editor-lets-repos-autorun-malicious-code-on-devices/){:target="_blank"}
