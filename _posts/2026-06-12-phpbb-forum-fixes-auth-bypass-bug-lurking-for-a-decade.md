---
title: 'phpBB forum fixes auth bypass bug lurking for a decade'
date: 2026-06-12
permalink: /posts/2026/06/12/phpbb-forum-fixes-auth-bypass-bug-lurking-for-a-decade/
tags:
- veille-cyber
- bleepingcomp
---
### Correction d'une faille critique d'authentification sur phpBB

Une vulnérabilité critique, présente depuis dix ans dans le code de la plateforme de forums phpBB, a été découverte par les chercheurs de l'entreprise Aikido. Cette faille permet à un attaquant de contourner le mécanisme d'authentification et de prendre le contrôle de n'importe quel compte, y compris ceux des administrateurs, via une simple requête HTTP.

**Points clés :**
* **Impact :** La vulnérabilité touche toutes les versions 3.x jusqu'à 3.3.16 et la version 4.0.0-a2.
* **Gravité :** Exploitable par défaut sans configuration particulière ; elle permet d'accéder aux messages privés, de modifier le contenu du forum ou d'usurper l'identité d'utilisateurs.
* **Exécution de code :** Aucune exécution de code à distance (RCE) n'est possible grâce à une protection supplémentaire sur le panneau d'administration.
* **Statut :** Aucun identifiant CVE n'a été attribué à ce jour.

**Vulnérabilités :**
* Contournement d'authentification (Authentication Bypass).

**Recommandations :**
* **Mise à jour immédiate :** Passer à la version **3.3.17**, qui corrige la faille pour la branche 3.x.
* **Utilisateurs de la version 4.x :** Aucune version corrective n'est disponible pour le moment ; il est conseillé de surveiller les annonces pour passer à la branche "master" dès qu'une solution sera déployée.
* **Attention aux configurations OAuth :** La mise à jour vers la version 3.3.17 modifie l'emplacement du gestionnaire de redirection OAuth, ce qui peut nécessiter un ajustement manuel pour maintenir cette fonctionnalité active.

---
[Source](https://www.bleepingcomputer.com/news/security/phpbb-forum-fixes-auth-bypass-bug-lurking-for-a-decade/){:target="_blank"}
