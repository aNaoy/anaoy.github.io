---
title: 'Making HTTP header injection critical with one prompt'
date: 2026-11-04
permalink: /posts/2026/11/04/making-http-header-injection-critical-with-one-prompt/
tags:
- veille-cyber
- zerodaysfans
---
### Automatisation de l'exploitation des vulnérabilités CRLF-Powered Desync

L'injection d'en-têtes HTTP peut désormais être escaladée de manière automatisée en une attaque de désynchronisation de requêtes (HTTP Request Smuggling), permettant de détourner des utilisateurs vers des serveurs externes. PortSwigger a intégré cette méthodologie de recherche complexe directement dans Burp AT pour permettre une exploitation autonome via une simple commande.

**Points clés de la méthodologie :**
*   **Identification :** Détection de l'emplacement d'injection amont, notamment en analysant si l'injection de CRLF (`%0d%0a`) dans le chemin déplace les en-têtes (ex: `Host`).
*   **Validation :** Construction de charges utiles de découpage de requêtes (*request splitting*) pour induire une désynchronisation et observer des codes d'état uniques.
*   **Recherche de gadgets :** Crawl ciblé pour identifier des redirections ouvertes exploitables via les en-têtes `Host` ou `X-Forwarded-Host`.
*   **Exploitation :** Combinaison des phases précédentes pour orchestrer une redirection malveillante vers un domaine tiers (ex: Collaborator).

**Vulnérabilités associées :**
*   **HTTP Request Smuggling** : Bien qu'aucune CVE spécifique ne soit mentionnée, cette technique repose sur l'exploitation des faiblesses de traitement des en-têtes HTTP par les serveurs front-end et back-end (désynchronisation).

**Recommandations :**
*   **Utilisation de l'automatisation :** Exploiter Burp AT pour tester systématiquement les injections d'en-têtes, même si le scanner initial ne rapporte qu'une injection simple.
*   **Prudence opérationnelle :** La méthode automatisée privilégie des exploits ciblés (redirections) pour éviter des effets de bord critiques sur la production, tout en offrant la base nécessaire pour des attaques plus complexes comme l'empoisonnement de cache (*Web Cache Poisoning*).
*   **Gestion des échecs :** En cas d'impossibilité de désynchronisation complète, basculer sur les techniques de *CRLF-Powered Tunnelling* pour rechercher des contournements de contrôle d'accès ou effectuer des tests manuels via des sessions Intruder pré-configurées.

---
[Source](https://portswigger.net/research/making-http-header-injection-critical-with-one-prompt){:target="_blank"}
