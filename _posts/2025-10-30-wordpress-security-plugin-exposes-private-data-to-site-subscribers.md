---
title: 'WordPress security plugin exposes private data to site subscribers'
date: 2025-10-30
permalink: /posts/2025/10/30/wordpress-security-plugin-exposes-private-data-to-site-subscribers/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnerability in WordPress Security Plugin Exposes Sensitive Data**

Un plugin populaire de sécurité pour WordPress, installé sur plus de 100 000 sites, présente une faille qui permet à des utilisateurs avec des privilèges limités, tels que les abonnés, de lire n'importe quel fichier sur le serveur. Cette vulnérabilité, identifiée sous la référence CVE-2025-11705, concerne les versions 4.23.81 et antérieures du plugin "Anti-Malware Security and Brute-Force Firewall".

La faille provient de l'absence de vérifications adéquates des autorisations dans la fonction `GOTMLS_ajax_scan()`, permettant à un attaquant d'obtenir un nonce et d'exécuter cette fonction. Cela autorise la lecture de fichiers sensibles, notamment le fichier de configuration `wp-config.php`, qui contient les identifiants de connexion à la base de données. L'accès à la base de données peut ensuite révéler des informations privées comme les mots de passe hachés, les adresses e-mail des utilisateurs, les publications et d'autres données critiques.

Bien que la criticité de la vulnérabilité soit jugée modérée car une authentification est nécessaire pour l'exploiter, de nombreux sites WordPress permettent la création de comptes abonnés, ce qui rend cette condition remplie.

**Points Clés :**

*   **Plugin affecté :** Anti-Malware Security and Brute-Force Firewall (pour WordPress)
*   **Nombre de sites affectés :** Plus de 100 000
*   **Versions affectées :** 4.23.81 et antérieures

**Vulnérabilité :**

*   **CVE :** CVE-2025-11705
*   **Type :** Lecture arbitraire de fichiers (Arbitrary File Read)
*   **Cause :** Absence de vérifications de capacités utilisateur dans la fonction `GOTMLS_ajax_scan()`.
*   **Impact :** Permet à des utilisateurs à faibles privilèges de lire des fichiers sensibles sur le serveur, y compris les identifiants de base de données.

**Recommandations :**

*   **Mise à jour immédiate :** Les administrateurs de sites WordPress utilisant le plugin "Anti-Malware Security and Brute-Force Firewall" doivent impérativement mettre à jour vers la version 4.23.83 ou une version ultérieure. Le développeur a publié cette mise à jour le 15 octobre, corrigeant la faille par l'ajout d'une fonction de vérification des autorisations (`GOTMLS_kill_invalid_user()`).
*   **Prudence :** Même si aucune exploitation en dehors des laboratoires de recherche n'a été détectée pour le moment, la divulgation publique de cette faille rend la mise à jour d'autant plus urgente pour éviter d'attirer l'attention des cybercriminels.

---
[Source](https://www.bleepingcomputer.com/news/security/wordpress-security-plugin-exposes-private-data-to-site-subscribers/){:target="_blank"}
