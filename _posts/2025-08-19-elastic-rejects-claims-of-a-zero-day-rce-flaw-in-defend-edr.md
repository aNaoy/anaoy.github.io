---
title: 'Elastic rejects claims of a zero-day RCE flaw in Defend EDR'
date: 2025-08-19
permalink: /posts/2025/08/19/elastic-rejects-claims-of-a-zero-day-rce-flaw-in-defend-edr/
tags:
- veille-cyber
- bleepingcomp
---
**Elastic Défend : Pas de faille zero-day confirmée**

La société Elastic, spécialisée dans la recherche d'entreprise et la sécurité, réfute les allégations concernant une vulnérabilité zero-day de type exécution de code à distance (RCE) dans son produit Defend EDR. Suite à un rapport de la société AshES Cybersecurity affirmant qu'une faille dans le pilote du noyau 'elastic-endpoint-driver.sys' permettrait de contourner les protections EDR, Elastic a mené une investigation approfondie.

**Points clés :**

*   AshES Cybersecurity a affirmé avoir découvert une vulnérabilité de déréférencement de pointeur NULL dans le pilote du noyau d'Elastic Defend.
*   Selon AshES, cette faille permettrait de contourner les protections EDR, d'exécuter du code à distance avec une visibilité réduite et d'établir une persistance sur le système.
*   Des vidéos ont été publiées pour démontrer le crash du pilote et l'exécution de `calc.exe` sans intervention de l'EDR.

**Réponse d'Elastic :**

*   Elastic n'a pas été en mesure de reproduire la vulnérabilité ni ses effets lors de ses tests.
*   La société indique que les rapports reçus d'AshES manquaient de preuves exploitables.
*   Elastic a tenté de reproduire les rapports et a invité les chercheurs à partager des preuves de concept reproductibles, ce qu'ils ont refusé.
*   Elastic déplore que AshES ait choisi de rendre ses allégations publiques au lieu de suivre les principes de divulgation coordonnée, n'ayant pas partagé les détails complets de la faille.

**Vulnérabilités :**

*   AshES Cybersecurity a identifié un problème de déréférencement de pointeur NULL dans le pilote du noyau `elastic-endpoint-driver.sys`.
*   Aucun identifiant CVE n'a été mentionné dans l'article pour cette vulnérabilité présumée.

**Recommandations :**

*   Il n'y a pas de recommandations directes dans cet article, car Elastic réfute l'existence de la faille telle que décrite par AshES Cybersecurity. Les utilisateurs sont encouragés à rester attentifs aux communications officielles d'Elastic concernant la sécurité de leurs produits.

---
[Source](https://www.bleepingcomputer.com/news/security/elastic-rejects-claims-of-a-zero-day-rce-flaw-in-defend-edr/){:target="_blank"}
