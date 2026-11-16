---
title: 'Six Unpatched Danfoss Refrigeration Controller Flaws Could Allow Remote Takeover Without Login'
date: 2026-11-16
permalink: /posts/2026/11/16/six-unpatched-danfoss-refrigeration-controller-flaws-could-allow-remote-takeover-without-login/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les contrôleurs de réfrigération Danfoss AK-SM800A

Six failles de sécurité non corrigées ont été découvertes dans les contrôleurs de réfrigération Danfoss AK-SM800A. Ces vulnérabilités permettent à un attaquant distant de prendre le contrôle total de l'appareil sans authentification, y compris sur les versions les plus récentes (5.4.0).

**Points clés :**
* **Impact :** Les attaquants peuvent modifier les paramètres de température, forcer des cycles de dégivrage (endommageant les stocks) et dissimuler leurs activités dans les journaux.
* **Persistance :** L'absence de « Secure Boot » permet aux attaquants d'installer des malwares persistants qui survivent aux réinitialisations d'usine et aux mises à jour de firmware.
* **État des correctifs :** Aucun correctif n'est disponible. Le fabricant n'a pas encore attribué de CVE aux vulnérabilités.
* **Complexité :** Les failles ont été identifiées rapidement par analyse manuelle, suggérant que le firmware pourrait contenir d'autres vulnérabilités similaires.

**Vulnérabilités :**
* Aucune référence CVE n'a été attribuée à ce jour.
* **Nature des failles :** Cinq vulnérabilités résident dans des gestionnaires de requêtes Web accessibles sans connexion, s'exécutant avec les privilèges « root ». La sixième affecte la passerelle chargée de l'application du « mode strict » (Strict mode), permettant de contourner cette protection.

**Recommandations immédiates :**
* **Suppression de l'exposition Internet :** Il est impératif de retirer immédiatement l'interface de gestion de l'exposition publique (incluant les accès via modems 4G/5G).
* **Accès sécurisé :** Privilégier un accès distant exclusivement via un VPN sécurisé ou un réseau interne protégé. Le filtrage IP par pare-feu n'est qu'une mesure temporaire.
* **Audit de sécurité :** Vérifier l'intégrité des paramètres de température, des plannings de dégivrage, des comptes utilisateurs et des journaux d'accès pour détecter toute activité suspecte.
* **Contrôles supplémentaires :** Bien que le passage au mode « Strict » et la mise à jour vers la version 5.4.0 soient recommandés, ces mesures sont jugées insuffisantes pour protéger les appareils contre ces failles spécifiques.

---
[Source](https://thehackernews.com/2026/11/six-unpatched-danfoss-refrigeration.html){:target="_blank"}
