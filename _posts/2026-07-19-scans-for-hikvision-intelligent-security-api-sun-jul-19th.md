---
title: 'Scans for Hikvision Intelligent Security API, (Sun, Jul 19th)'
date: 2026-07-19
permalink: /posts/2026/07/19/scans-for-hikvision-intelligent-security-api-sun-jul-19th/
tags:
- veille-cyber
- sans-isc
---
### Recrudescence des scans malveillants sur l'API ISAPI de Hikvision

Les caméras Hikvision font l'objet de nouvelles campagnes de reconnaissance ciblant l'API *Intelligent Security API* (ISAPI). Cette interface REST, bien que puissante pour la gestion et le contrôle total des dispositifs, devient un vecteur d'attaque privilégié par les cybercriminels pour identifier et profiler les équipements exposés sur Internet.

**Points clés :**
*   **Ciblage :** L'endpoint `/ISAPI/System/status` est activement scanné pour confirmer la présence de l'API et potentiellement faciliter des attaques par force brute.
*   **Risques liés au chiffrement :** Bien que l'API supporte le chiffrement AES, la méthode de dérivation des clés basée sur le mot de passe et l'exposition du vecteur d'initialisation (IV) dans l'URL rendent cette protection inefficace si l'authentification de base est utilisée sans HTTPS.
*   **Accessibilité :** L'API permet un contrôle étendu des caméras (paramétrages, gestion), ce qui en fait une cible critique si elle n'est pas sécurisée.

**Vulnérabilités :**
*   L'article souligne une vulnérabilité conceptuelle dans l'implémentation du chiffrement (AES en mode CBC avec IV exposé) et l'utilisation généralisée d'authentifications faibles (Basic/Digest) sans HTTPS systématique. Aucune CVE spécifique n'est mentionnée pour cette campagne de scan récente, mais l'historique des produits Hikvision est marqué par de nombreuses vulnérabilités passées.

**Recommandations :**
*   **Isolation réseau :** Ne jamais exposer directement les caméras sur Internet. Utilisez un VPN ou un tunnel sécurisé pour accéder aux interfaces de gestion.
*   **Segmentation :** Éviter de placer ces dispositifs dans des zones réseau sensibles.
*   **Sécurisation HTTPS :** Configurer systématiquement le HTTPS avec des certificats valides pour renforcer la protection des flux, plutôt que de se fier au chiffrement natif de l'API.
*   **Mise à jour :** Veiller à ce que les firmwares soient à jour pour limiter l'exploitation de failles connues.

---
[Source](https://isc.sans.edu/diary/rss/33164){:target="_blank"}
