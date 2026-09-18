---
title: 'An Abandoned CDN Domain Was Re-Registered. Thousands of Sites Still Call It.'
date: 2026-09-18
permalink: /posts/2026/09/18/an-abandoned-cdn-domain-was-re-registered-thousands-of-sites-still-call-it/
tags:
- veille-cyber
- hackernews
---
### Risques liés aux scripts tiers et aux domaines expirés : L'importance du CSP

La récupération de noms de domaines expirés ayant appartenu à des CDN (Content Delivery Networks) constitue une menace critique. Des milliers de sites web conservent des références statiques vers ces domaines, permettant au nouveau propriétaire de prendre le contrôle de l'exécution de code sur ces pages, à l'insu des propriétaires et des outils de sécurité traditionnels.

**Points clés :**
*   **Vulnérabilité des scripts tiers :** Les outils d'analyse statique et les scanners de dépendances ignorent les scripts chargés dynamiquement dans le navigateur de l'utilisateur. Ces scripts possèdent les mêmes privilèges que le code propriétaire (accès aux cookies, aux formulaires et au DOM).
*   **Évasion des scanners :** Les attaques peuvent être ciblées géographiquement ou basées sur l'utilisateur, rendant les scanners de sécurité classiques inefficaces car ils ne voient qu'une version "propre" du site.
*   **Conformité réglementaire :** La norme PCI DSS v4.0.1 (exigences 6.4.3 et 11.6.1) impose désormais la gestion d'un inventaire autorisé, le contrôle de l'intégrité et la mise en place d'alertes en cas de modification non autorisée des scripts sur les pages de paiement.

**Vulnérabilités :**
*   **Supply Chain Attack (Client-side) :** Exploitation de scripts tiers (ex: *polyfill.io* ou domaines CDN abandonnés) pour injecter du code malveillant sans compromettre le serveur source.
*   **Absence de contrôle CSP :** L'incapacité à surveiller et restreindre les sources de scripts exécutés par le navigateur permet des attaques de type Magecart ou ClickFix.
*   *Note : Bien qu'aucune CVE spécifique ne soit mentionnée, ces vecteurs correspondent aux failles de sécurité de la chaîne d'approvisionnement logicielle.*

**Recommandations :**
*   **Mise en place du CSP (Content Security Policy) :** Déployer une politique CSP en mode `report-only` pour auditer le code réellement exécuté sur les navigateurs des utilisateurs sans risquer de casser le site.
*   **Inventaire continu :** Maintenir une liste exhaustive des scripts tiers avec justification métier.
*   **Surveillance côté client :** Utiliser des solutions capables de capturer les rapports CSP envoyés par les navigateurs pour détecter les changements de comportement des scripts tiers en temps réel.
*   **Révision des dépendances :** Identifier et supprimer systématiquement les références obsolètes vers des domaines ou bibliothèques externes non maintenus.

---
[Source](https://thehackernews.com/2026/09/an-abandoned-cdn-domain-was-re.html){:target="_blank"}
