---
title: 'LG Smart TVs Vulnerable to Pre-Auth Root Takeover From Local Network'
date: 2026-10-13
permalink: /posts/2026/10/13/lg-smart-tvs-vulnerable-to-pre-auth-root-takeover-from-local-network/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans webOS : Risque de prise de contrôle totale des TV LG

Des chercheurs ont identifié une chaîne de trois vulnérabilités au sein du système d'exploitation webOS de LG, permettant à un attaquant situé sur le même réseau local d'obtenir un accès administrateur (root) sur certains modèles de téléviseurs connectés, sans interaction de l'utilisateur ni code PIN.

**Points clés :**
* **Vecteur d'attaque :** L'attaque exploite le service de couplage de l'application LG ThinQ (port 3001).
* **Mécanisme :** En utilisant un certificat de test préinstallé et approuvé par le firmware, l'attaquant contourne l'authentification. Il utilise ensuite l'application interne `cmp-client` pour rediriger le trafic vers une page malveillante, accédant ainsi à l'interface `PalmServiceBridge`.
* **Escalade de privilèges :** L'injection de commandes via le service de journalisation système (`pmlogd`), qui s'exécute avec les privilèges root, permet une prise de contrôle complète.
* **Statut :** Aucun identifiant CVE n'a été attribué pour ces vulnérabilités. Bien qu'aucune exploitation malveillante n'ait été signalée à ce jour, le risque de compromission est réel pour les appareils non mis à jour.

**Vulnérabilités :**
* Pas de CVE assigné.

**Recommandations :**
* **Mise à jour immédiate :** Les propriétaires des modèles concernés (notamment les séries 32LQ636BPSA et 27TQ600SW) doivent vérifier et installer la dernière version du firmware disponible via les paramètres du téléviseur.
* **Atténuation :** Aucune solution de contournement (workaround) n'est disponible ; la mise à jour logicielle constitue l'unique mesure de protection.

---
[Source](https://thehackernews.com/2026/10/lg-smart-tvs-vulnerable-to-pre-auth.html){:target="_blank"}
