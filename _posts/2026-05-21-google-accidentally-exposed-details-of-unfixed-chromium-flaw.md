---
title: 'Google accidentally exposed details of unfixed Chromium flaw'
date: 2026-05-21
permalink: /posts/2026/05/21/google-accidentally-exposed-details-of-unfixed-chromium-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Fuite d'une vulnérabilité critique de persistance dans Chromium

Google a accidentellement rendu publics les détails techniques d'une faille de sécurité majeure au sein du moteur Chromium, permettant l'exécution de code JavaScript à distance (RCE). Bien que marquée comme corrigée dans le système de suivi des bugs de Google, la vulnérabilité reste active, exposant les utilisateurs à un risque de persistance silencieuse même après la fermeture du navigateur.

**Points clés :**
* **Mécanisme :** L'exploitation repose sur l'utilisation d'un *Service Worker* malveillant qui ne se termine jamais, transformant le navigateur de la victime en un nœud de botnet permanent.
* **Impact :** La faille touche tous les navigateurs basés sur Chromium (Chrome, Edge, Brave, Opera, Vivaldi, Arc).
* **Gravité :** L'exécution du code est invisible pour l'utilisateur, d'autant plus que les versions récentes de Microsoft Edge ont supprimé les alertes de téléchargement qui permettaient auparavant de détecter l'activité en arrière-plan.
* **Risques :** Les attaquants peuvent détourner le navigateur pour mener des attaques DDoS, relayer du trafic malveillant ou rediriger des requêtes web.
* **Portée limitée :** La faille ne permet pas de contourner les protections du bac à sable (*sandbox*) du navigateur ; elle ne donne pas accès aux fichiers locaux, aux emails ou au système d'exploitation hôte.

**Vulnérabilités :**
* La faille, identifiée par la chercheuse Lyra Rebane, concerne un défaut de terminaison des *Service Workers*. 
* Aucune référence CVE officielle n'est mentionnée dans l'article à ce stade, bien que le problème soit suivi dans le gestionnaire de bugs de Chromium.

**Recommandations :**
* **Utilisateurs :** Étant donné qu'aucun correctif efficace n'a été déployé malgré les annonces, la prudence est de mise lors de la navigation sur des sites web inconnus ou non fiables.
* **Attente de mise à jour :** Google devrait publier des correctifs d'urgence sous peu. Il est impératif de maintenir le navigateur à jour dès qu'une nouvelle version devient disponible.
* **Développeurs et administrateurs :** Surveiller les annonces de sécurité de Google Chrome et appliquer les correctifs immédiatement après leur publication.

---
[Source](https://www.bleepingcomputer.com/news/security/google-accidentally-exposed-details-of-unfixed-chromium-flaw/){:target="_blank"}
