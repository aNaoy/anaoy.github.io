---
title: 'ShadyPanda browser extensions amass 4.3M installs in malicious campaign'
date: 2025-12-01
permalink: /posts/2025/12/01/shadypanda-browser-extensions-amass-43m-installs-in-malicious-campaign/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne de Malwares via Extensions de Navigateur : ShadyPanda

Une opération de malware de longue durée, baptisée "ShadyPanda", a réussi à faire installer plus de 4,3 millions d'extensions de navigateur pour Chrome et Edge, initialement présentées comme légitimes, mais qui ont évolué pour devenir des logiciels malveillants. Découverte par Koi Security, cette campagne s'est déroulée en plusieurs phases, introduisant progressivement des fonctionnalités malveillantes.

Au total, 145 extensions (20 pour Chrome et 125 pour Edge) ont été identifiées. Bien que Google ait retiré les extensions de son Web Store, la campagne reste active sur la plateforme Microsoft Edge Add-ons, où une extension compte 3 millions d'installations. Il est incertain si ces installations ont été gonflées artificiellement pour accroître leur crédibilité.

**Phases de la Campagne :**

*   **2018 - Début 2023 :** Les premières soumissions d'extensions ont eu lieu en 2018. Les signes d'activités malveillantes sont apparus en 2023 avec des extensions se présentant comme des outils de productivité ou des fonds d'écran. Elles pratiquaient la fraude affiliée en injectant des codes de suivi (eBay, Booking.com, Amazon) dans des liens légitimes pour générer des revenus sur les achats des utilisateurs.
*   **Début 2024 :** Une extension nommée Infinity V+ a commencé à détourner les recherches, redirigeant les requêtes vers trovi[.]com et exfiltrant les cookies vers dergoodting[.]com, ainsi que les requêtes de recherche vers des sous-domaines de gotocdn.
*   **2024 :** Cinq extensions, dont certaines soumises en 2018 et 2019, ont été modifiées via une mise à jour pour inclure une "backdoor" permettant l'exécution de code à distance (RCE). Chaque navigateur infecté exécute un framework RCE qui vérifie toutes les heures la présence de nouvelles instructions sur api.extensionplay[.]com, télécharge et exécute du JavaScript arbitraire avec un accès complet aux API du navigateur. Cette backdoor exfiltre également les URL visitées, les informations d'identification et les identifiants persistants vers api[.]cleanmasters[.]store, en utilisant le chiffrement AES. L'extension "Clean Master" sur le Chrome Web Store, avec 200 000 installations, faisait partie de cet ensemble.
*   **Phase actuelle :** Cinq extensions pour Microsoft Edge, publiées en 2023 par "Starlab Technology", sont toujours actives et ont cumulé 4 millions d'installations. Ces extensions contiennent un composant spyware qui collecte l'historique de navigation, les requêtes de recherche et les frappes au clavier, les clics de souris avec coordonnées, les données d'identification du navigateur (fingerprinting), ainsi que le stockage local/de session et les cookies, les envoyant vers 17 domaines en Chine. Bien que ces extensions aient les permissions nécessaires pour délivrer une backdoor similaire à celle du groupe "Clean Master", aucune activité de ce type n'a été observée pour le moment.

**Points Clés :**

*   **Acteurs :** Groupe malveillant "ShadyPanda".
*   **Outils :** Extensions de navigateur pour Chrome et Edge.
*   **Volume :** Plus de 4,3 millions d'installations cumulées.
*   **Évolution des menaces :** Passage de la fraude affiliée à la redirection de recherche, puis à l'exécution de code à distance et au spyware.
*   **Pérsistance :** La campagne reste active sur la plateforme Microsoft Edge Add-ons.

**Vulnérabilités :**

Il n'y a pas de CVE spécifique mentionné dans l'article, car la menace réside dans la conception et la distribution d'extensions malveillantes plutôt que dans l'exploitation d'une faille logicielle spécifique sur le système de l'utilisateur. Les vulnérabilités exploitées sont plutôt liées à la confiance accordée aux extensions des navigateurs et aux processus de validation des stores d'extensions.

**Recommandations :**

*   **Supprimer immédiatement** toutes les extensions suspectes ou inconnues.
*   **Réinitialiser les mots de passe** de tous les comptes en ligne après la suppression des extensions compromises.
*   **Vérifier attentivement les permissions** demandées par les extensions avant de les installer.
*   **Privilégier les extensions provenant de développeurs réputés** et avec un historique de sécurité vérifié.
*   **Être vigilant face aux extensions** qui semblent trop belles pour être vraies ou qui demandent des privilèges excessifs.

---
[Source](https://www.bleepingcomputer.com/news/security/shadypanda-browser-extensions-amass-43m-installs-in-malicious-campaign/){:target="_blank"}
