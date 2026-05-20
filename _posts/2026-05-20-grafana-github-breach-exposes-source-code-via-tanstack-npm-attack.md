---
title: 'Grafana GitHub Breach Exposes Source Code via TanStack npm Attack'
date: 2026-05-20
permalink: /posts/2026/05/20/grafana-github-breach-exposes-source-code-via-tanstack-npm-attack/
tags:
- veille-cyber
- hackernews
---
### Compromission de Grafana via la chaîne d'approvisionnement TanStack

Grafana Labs a subi une violation de sécurité sur son environnement GitHub, conséquence directe de l'attaque par empoisonnement de la chaîne d'approvisionnement npm visant le paquet **TanStack**. Bien que les systèmes de production et les données des clients de la plateforme Grafana Cloud ne soient pas impactés, les attaquants ont exfiltré du code source public et privé, ainsi que des informations opérationnelles internes et des contacts professionnels.

**Points clés :**
*   **Origine :** L'incident découle de l'attaque de la chaîne d'approvisionnement "TanStack", orchestrée par le groupe TeamPCP.
*   **Vecteur :** Malgré une rotation rapide des jetons d'automatisation GitHub, un jeton oublié a permis aux attaquants de maintenir l'accès.
*   **Extorsion :** Les assaillants (identifiés comme le groupe *CoinbaseCartel*) ont tenté une extorsion, que Grafana a refusé de payer.
*   **Impact :** Accès aux dépôts GitHub, compromission de données internes et de listes de contacts professionnels.

**Vulnérabilités :**
*   **Attaque de chaîne d'approvisionnement (Supply Chain Attack) :** Injection de code malveillant via le paquet npm TanStack.
*   **Gestion des accès :** Mauvaise rotation des jetons (tokens) de flux de travail (workflow) GitHub. 
*   *Note : Aucune CVE spécifique n'est mentionnée dans l'article pour cette attaque logicielle précise.*

**Recommandations :**
*   **Rotation des secrets :** Assurer une rotation exhaustive et rigoureuse des jetons d'accès et des clés d'automatisation après une alerte de sécurité.
*   **Audit de sécurité :** Effectuer une vérification systématique de tous les commits pour détecter des activités malveillantes après une compromission.
*   **Surveillance renforcée :** Renforcer la posture de sécurité sur GitHub en implémentant des outils de monitoring plus stricts sur les accès aux dépôts.
*   **Politique de non-paiement :** Maintenir une politique stricte de refus de paiement des rançons pour décourager les futures campagnes d'extorsion.

---
[Source](https://thehackernews.com/2026/05/grafana-github-breach-exposes-source.html){:target="_blank"}
