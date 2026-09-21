---
title: 'WordPress Click2Shell flaw lets hackers execute PHP on the server'
date: 2026-09-21
permalink: /posts/2026/09/21/wordpress-click2shell-flaw-lets-hackers-execute-php-on-the-server/
tags:
- veille-cyber
- bleepingcomp
---
### Click2Shell : Une faille RCE critique dans WordPress

La vulnérabilité « Click2Shell » permet l'exécution de code PHP arbitraire sur le serveur via une attaque par contrefaçon de requête intersite (CSRF). Cette faille permet à un attaquant de forcer l'installation d'un thème WordPress vulnérable depuis le catalogue officiel, puis d'exécuter du code malveillant lors de la prévisualisation dans le « Customizer ».

**Points clés :**
*   **Vecteur d'attaque :** Un administrateur authentifié doit cliquer sur un lien piégé ou être redirigé via une faille XSS existante.
*   **Impact :** Exécution de code à distance (RCE), accès aux données utilisateurs, modification/suppression de fichiers, récupération des identifiants de base de données (fichier `wp-config.php`) et création de comptes administrateur malveillants.
*   **Conditions :** L'attaque ne nécessite aucun compte sur le site cible, mais requiert qu'un administrateur visite l'URL malveillante. Les rôles « Auteur » ou « Éditeur » ne possèdent pas les permissions nécessaires pour déclencher cette action.

**Vulnérabilités :**
*   **Composant :** WordPress Core (versions 7.1.0 et antérieures).
*   **CVE :** Aucun identifiant officiel attribué à ce jour.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer la version **WordPress 7.1.1** ou supérieure, qui corrige la gestion du slug de thème et restreint les sélecteurs JavaScript.
*   **Mesure d'atténuation temporaire :** Activer la constante `DISALLOW_FILE_MODS` dans le fichier `wp-config.php` pour empêcher l'installation forcée de thèmes ou de plugins si la mise à jour n'est pas réalisable immédiatement.

---
[Source](https://www.bleepingcomputer.com/news/security/wordpress-click2shell-flaw-lets-hackers-execute-php-on-the-server/){:target="_blank"}
