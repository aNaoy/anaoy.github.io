---
title: 'Carrot disclosure: Forgejo'
date: 2026-04-29
permalink: /posts/2026/04/29/carrot-disclosure-forgejo/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse de sécurité de Forgejo : Vulnérabilités systémiques

Un audit rapide de la plateforme Forgejo a révélé une multitude de failles critiques, témoignant de problèmes structurels profonds au sein de la base de code. Plutôt qu'une divulgation classique, l'auteur a opté pour une « divulgation par la carotte » (carrot disclosure) : la démonstration publique d'une chaîne d'exploitation fonctionnelle pour inciter les développeurs à réaliser un audit de sécurité complet.

**Points clés :**
*   **Insécurité systémique :** La découverte d'une vaste gamme de vulnérabilités en une seule soirée indique une architecture fragile héritée, en partie, de Gitea.
*   **Chaînage d'exploitation :** L'auteur a réussi à combiner plusieurs failles pour obtenir une exécution de code à distance (RCE), des fuites de secrets, des privilèges élevés via OAuth2 et un accès persistant aux comptes.
*   **Technique de pression :** La publication du code d'exploitation (PoC) sert d'ultimatum pour forcer une refonte de la sécurité logicielle plutôt qu'une correction superficielle (« wack-a-mole »).

**Vulnérabilités identifiées :**
*   **Exécution de code à distance (RCE) :** Permise par le chaînage de plusieurs failles.
*   **Failles SSRF :** Présentes en de nombreux points de l'application.
*   **Problèmes d'authentification :** Faiblesses dans la gestion des sessions, OAuth2, OTP et le processus de récupération de compte.
*   **Déni de service (DoS) :** Plusieurs vecteurs identifiés permettant de saturer les ressources (CPU, stockage, base de données).
*   **Fuites d'informations :** Diverses failles permettant d'exposer des données sensibles ou des jetons.
*   **Autres failles :** Absence de CSP/Trusted-Types, mauvaises pratiques cryptographiques, failles TOCTOU (Time-of-check to time-of-use).
*   *Note : Aucune CVE spécifique n'a été attribuée par l'auteur dans cet article.*

**Recommandations :**
*   **Pour les développeurs (Forgejo) :** Entreprendre un audit de sécurité holistique plutôt que des correctifs isolés, afin de traiter la dette technique et les faiblesses architecturales.
*   **Pour les administrateurs d'instances :**
    *   Limiter autant que possible l'exposition des instances.
    *   Désactiver les options de configuration non essentielles qui pourraient faciliter les chaînes d'exploitation (notamment l'inscription ouverte).
    *   Surveiller les mises à jour et appliquer les correctifs de sécurité dès leur publication.
    *   Appliquer le principe du moindre privilège pour les utilisateurs et les intégrations OAuth2.

---
[Source](https://dustri.org/b/carrot-disclosure-forgejo.html){:target="_blank"}
