---
title: 'Blind trust: stealing credentials through CSP'
date: 2026-11-11
permalink: /posts/2026/11/11/blind-trust-stealing-credentials-through-csp/
tags:
- veille-cyber
- zerodaysfans
---
### Contourner la Content Security Policy (CSP) : Risques et Automatisation

La **Content Security Policy (CSP)** est une couche de sécurité conçue pour prévenir les injections HTML et le XSS. Cependant, elle est souvent contournée en raison de configurations permissives ou de mécanismes oubliés par les développeurs.

#### Points clés
*   **Faiblesses des listes blanches (Allow-lists) :** L'inclusion de domaines tiers dans une CSP peut introduire des « gadgets » (ex: points de terminaison JSONP ou anciennes versions d'AngularJS) permettant d'exécuter du code arbitraire malgré les restrictions.
*   **Exploitation via `form-action` :** Même avec une directive `default-src 'none'` bloquant tout JavaScript, une politique autorisant `form-action 'self'` permet d'exfiltrer des identifiants. Un formulaire injecté peut rediriger les données de saisie vers une URL contrôlée par l'attaquant via l'en-tête `Referer` (après une réflexion HTML et une redirection par `meta refresh`).
*   **Automatisation :** L'outil *Burp AT* automatise désormais la détection de ces vulnérabilités en analysant les directives CSP, en identifiant les gadgets connus et en générant des preuves de concept (PoC) exploitant les formulaires auto-soumis.

#### Vulnérabilités ciblées
*   **Injection HTML (XSS via CSP bypass) :** Exploitation de gadgets tiers autorisés dans la directive `script-src`.
*   **Exfiltration de données (Form-jacking) :** Utilisation abusive de la directive `form-action` pour voler des informations d'authentification sans exécution de script.

#### Recommandations de sécurité
1.  **Restreindre les sources :** Éviter d'ajouter des domaines tiers non maîtrisés dans les directives de script. Privilégier les **nonces** ou les **hachages** (hashes) pour valider les scripts.
2.  **Verrouiller `form-action` :** Ne pas omettre cette directive. Si aucune soumission de formulaire n'est requise, définir `form-action 'none'`. Si nécessaire, limiter strictement aux domaines de confiance.
3.  **Auditer la hiérarchie :** Vérifier l'ordre de priorité des directives (fallback vers `default-src`) et s'assurer que `strict-dynamic` est utilisé pour moderniser la sécurité et ignorer les listes blanches de domaines moins fiables.
4.  **Tests automatisés :** Utiliser des outils d'analyse statique et dynamique pour tester la robustesse réelle de la CSP face à des scénarios d'injection et d'exfiltration.

---
[Source](https://portswigger.net/research/blind-trust-stealing-credentials-through-csp){:target="_blank"}
